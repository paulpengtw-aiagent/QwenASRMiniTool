# 11 — Local app session coordination

**What to build:** Launching twice reuses one healthy local app session rather than fighting over a port, and a stale session is replaced safely.

**Blocked by:** 03, 10

**Status:** ready-for-agent

- [ ] An Ubuntu-only session file records the loopback URL, a pid identity and an access key
- [ ] A launcher reuses a healthy existing session via a keyed health check
- [ ] A stale session is taken over only after verifying pid identity
- [ ] Quit is authorized by the access key
- [ ] Connected clients receive a stopping broadcast within the exit deadline
- [ ] The session file is deleted on clean exit
- [ ] Windows launch and shutdown behaviour is unchanged
