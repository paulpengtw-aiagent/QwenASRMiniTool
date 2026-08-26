# 03 — Platform seams module

**What to build:** All platform difference for the shared code paths lives in one module, and Ubuntu gains the child-process cleanup it has never had. Opening an output folder stops raising on Ubuntu.

**Blocked by:** 01

**Status:** ready-for-agent

- [ ] A single module exposes `app_dir`, `open_path`, `find_executable`, `spawn`, `guard_children` and `open_browser`
- [ ] `open_path` uses `xdg-open` on Linux, and the output-folder action works on Ubuntu where it previously raised
- [ ] `guard_children` keeps the existing Windows Job Object behaviour unchanged
- [ ] On Linux children start in their own session and shutdown kills the whole group
- [ ] A child survives neither a graceful parent exit nor a parent force-kill
- [ ] Windows-only engine modules keep their existing subprocess flags untouched
