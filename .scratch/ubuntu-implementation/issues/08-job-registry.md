# 08 — Reconnectable job registry

**What to build:** The local app session owns all transcription work, so any browser client can close, reopen and recover progress, results, errors and history.

**Blocked by:** 01

**Status:** ready-for-agent

- [ ] States are queued, running, then completed, failed or cancelled, with one inference job running at a time
- [ ] A batch is one job containing items, each with its own state, and a failing item does not stop the rest
- [ ] Recording adds a capturing state bound to its capture client, and a client closing mid-recording completes the job with an explicit early-end note while retaining transcribed segments
- [ ] Segment edits are server-owned, visible to every connected client, and survive the editing tab closing
- [ ] A reconnecting client renders job kind, state, progress, per-item states, segments, errors, notes and saved paths purely from the snapshot
- [ ] Process restart wipes the registry while saved output files survive
