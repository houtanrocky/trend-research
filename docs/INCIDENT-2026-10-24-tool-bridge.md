# Incident Record — DSH Tool Bridge Failure

**Date:** 2026-10-24
**Session workspace:** `S:\Repos`
**Reporter:** DSH assistant session (trend-research / Modares faculty research task)
**Severity:** High (task fully blocked for ~5 turns; no user data lost)

---

## 1. Summary

During a two-part research task (read `houtanrocky/trend-research`, then research TMU ISE faculty), the tool bridge repeatedly rejected or silently dropped tool calls. The session stalled in a loop of parse errors and empty results, and the harness stopped. Root causes are layered: (a) a protocol misuse on my side, (b) an enforced 3-call cap that my multi-call blocks exceeded, and (c) **a missing `DEEPSEEK_API_KEY`, which made `dsh_handoff` fail deterministically**.

No files were corrupted. The repo was already cloned and intact.

---

## 2. Timeline (evidence-based)

| # | Event | Evidence | Verdict |
|---|---|---|---|
| 1 | First response sent 3 `dsh_*` calls in one block | Turn 1 tool_calls array had 3 entries | Legal at the boundary, but fragile |
| 2 | `parse-error`: "Too many calls; the maximum is 3 per response" | System message after turn 1 | **My fault** — 3 is the max, but the block was framed such that the parser counted it as malformed |
| 3 | Retried with a single `dsh_handoff` | `dsh_handoff` result: `ok:false`, `E_HANDOFF_FAILED`, exitCode 1, durationMs 8103 | Handoff subsystem failed fast, not a timeout |
| 4 | Several `dsh_bash` calls returned empty stdout/stderr | `ok:true, exitCode:255, stdout:"", stderr:""` | Misread by me as "bridge dead"; actually `cmd.exe` rejecting POSIX commands |
| 5 | Tried `Get-ChildItem` | stderr: `'Get-ChildItem' is not recognized...` | **Confirmed shell is `cmd.exe`, not PowerShell** |
| 6 | `dir /b` + `type` on the handoff stderr file | exitCode 0, full directory listing returned | Bridge was healthy the whole time |
| 7 | Root cause of handoff failure found | stderr file contents: `dsh: MISSING_CREDENTIAL: llm-deepseek: no API key for provider route "deepseek-official"; store DEEPSEEK_API_KEY ...` | **`dsh_handoff` cannot work without `DEEPSEEK_API_KEY`** |
| 8 | Repo read successfully via `dsh_tree` + `dsh_read` | 11 files, 4 docs read with sha256 hashes | Work resumed normally once shell semantics were fixed |
| 9 | Sent 3 `dsh_read` calls; block was truncated mid-JSON | `content` ended with `⟦DSH⟧{"tool":"dsh_read","` | **My fault** — output truncation while emitting a multi-call block |
| 10 | Harness stopped | Last assistant turn was literally `"Safe"` with no content | Degenerate completion after repeated framing failures |

---

## 3. Root Causes

### RC-1 — Multi-call blocks are brittle in this harness (primary, mine)
The 3-call maximum is a ceiling, not a target. Every failure in this session that was under my control happened while emitting **more than one** tool call per response. The parser appears to stream-parse the block and abort the whole response if anything is off — a truncated JSON string, a missing closing marker, or a miscount. Single-call responses never failed.

**Contributing factor:** I emitted a fenced code block containing three full JSON tool calls. Any truncation of my own output (token limit, stream cut) lands mid-string and destroys the entire block.

### RC-2 — `dsh_handoff` is unusable without `DEEPSEEK_API_KEY` (environment)
The handoff agent spawns a `dsh headless` subprocess that needs its own LLM credential. It reads `deepseek-official` and fails immediately with `MISSING_CREDENTIAL`. This is not retryable and not detectable from the tool schema — the tool is listed as available but is silently non-functional. It cost one full turn and produced a misleading "Handoff failed" with empty stdout.

**Fix:** set `DEEPSEEK_API_KEY` via the credentials service, or remove/disable `dsh_handoff` from the catalog when the key is absent so the model does not plan around it.

### RC-3 — Shell is `cmd.exe`, but the tool description says "normal shell syntax" (protocol/doc mismatch)
`dsh_bash` advertises pipes, chains, and redirection — which I read as POSIX. In reality it is `cmd.exe`: no `ls`, `cat`, `find`, `head`, `grep`, no `Get-ChildItem`. Failures returned `exitCode:255` with **empty stderr** for `cat` (because `cat` produced no error text before failing) and a real error only for `Get-ChildItem`. I misdiagnosed this as a dead bridge for ~3 turns.

**Fix:** state the actual shell in the tool description (e.g. "Windows `cmd.exe`; use `dir`, `type`, `findstr`"), or route through a POSIX shell.

### RC-4 — Empty success payloads are indistinguishable from bridge failure
`{ok:true, exitCode:255, stdout:"", stderr:""}` looks identical to a dropped call. A non-zero exit with no diagnostics should be surfaced as an error, not a successful result.

---

## 4. Impact

- **~5 wasted turns** out of a 100-iteration budget, plus one full handoff attempt.
- Task progress: repo located and read (11 files, 4 docs consumed) — **Part 1 ~60% done**. Part 2 (ISE faculty research) **not started**.
- No data loss, no bad writes, no corrupted repo state.
- User-visible effect: one incorrect "bridge is dead, task blocked" report that was later contradicted by the evidence.

---

## 5. Corrective Actions

**For me (immediate, this session and onward):**
1. **One tool call per response.** Never batch, even though 3 are permitted. This alone eliminates RC-1.
2. Probe the shell once per session with a known-good native command (`dir /b`) before assuming POSIX.
3. Never report "tool bridge dead" without first checking the log/stderr file for a real error string.

**For the harness (recommended):**
4. Disable `dsh_handoff` in the catalog when `DEEPSEEK_API_KEY` is missing, or surface `E_MISSING_CREDENTIAL` in the tool description.
5. Include the shell name and dialect in the `dsh_bash` description.
6. Treat `exitCode != 0` with empty stderr as an error payload, not `ok:true`.
6b. On `parse-error`, echo back the offending block so the model can see where truncation occurred.
7. Cap response size per tool block, or encourage single-call blocks in the system prompt the way this incident shows is necessary.

---

## 6. Unresolved

The original task is **incomplete**:

- `trend-research/docs/t1-research-plan.md`, `docs/alternatives.md`, `data/site-notes.md`, `data/profile-snapshot.json`, `data/repos-snapshot.tsv`, `README.md` lines 300-324 — **not yet read**.
- `https://ise.modares.ac.ir/departments` and `/it%20engineering` — **not fetched**. Network reachability unverified.
- Faculty table, feasibility report, thesis directions — **not produced**.

Resume from: read the 3 remaining docs one call at a time, then test outbound HTTP with `curl` (Windows 10+ ships it).
