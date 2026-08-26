# 09 — Downloads as registry jobs

**What to build:** A model download is visible, reconnectable work rather than fire-and-forget progress, and no job ever silently delivers less than it was asked for.

**Blocked by:** 06, 07, 08

**Status:** ready-for-agent

- [ ] A download appears as a registry job with progress, errors and the same reconnect guarantees
- [ ] Downloads run in a lane exempt from the single-runner rule, so fetching 1.7B does not block transcribing with 0.6B
- [ ] A job requesting an absent feature asset is refused at submit with the download offered as an explicit action
- [ ] No job completes having silently skipped a requested feature
