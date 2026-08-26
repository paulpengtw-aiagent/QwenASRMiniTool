# 14 — Scheduled real-path CI and Windows regression CI

**What to build:** The real download-and-transcribe path is proven automatically without blocking merges, and the Windows invariants this effort promised to preserve are checked continuously.

**Blocked by:** 02, 04, 06

**Status:** ready-for-agent

- [ ] A scheduled job downloads the 0.6B model with caching, transcribes a committed fixture clip, and asserts segments were returned
- [ ] A Windows job runs the settings schema round trip, imports the platform seams module, and asserts the generated requirements file matches the lock export
- [ ] Neither job blocks pull-request merges
- [ ] GPU engines and the frozen executable remain a documented manual checklist
