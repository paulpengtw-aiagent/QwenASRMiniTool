# 05 — Launcher and preflight

**What to build:** Launching on Ubuntu either starts a working app or explains precisely what to run, before the server ever starts.

**Blocked by:** 01, 03

**Status:** ready-for-agent

- [ ] The launcher runs `uv sync --check` before starting and performs no network I/O
- [ ] A missing environment and a drifted lock each produce a distinct message naming the command that fixes it
- [ ] Fatal failures exit non-zero
- [ ] A missing FFmpeg does not prevent launch
- [ ] No runnable browser does not prevent launch, and the loopback URL is printed for manual opening
- [ ] Every fatal message prints in English and Chinese
