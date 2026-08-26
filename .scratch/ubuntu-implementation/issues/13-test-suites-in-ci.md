# 13 — Automated test suites in per-PR CI

**What to build:** The behaviours most likely to regress silently are covered by fast automated tests on every change.

**Blocked by:** 02, 03, 04, 06

**Status:** ready-for-agent

- [ ] Seam function tests run on each platform where they apply
- [ ] Settings tests cover v1 to v2 migration, unknown-key round trip, and the interface scale disambiguation heuristic
- [ ] A local HTTP fixture server exercises byte-range resume, partial-file rename, and the truncated-file case
- [ ] The suite runs in per-PR CI and contacts no third-party host
