# 10 — Cancellation and bounded shutdown

**What to build:** Any long-running operation can be stopped without losing work already done, and no exit path leaves a process behind.

**Blocked by:** 03, 08, 09

**Status:** ready-for-agent

- [ ] Transcription cancels at chunk boundaries and retains already-transcribed segments
- [ ] Any trusted client may cancel any job
- [ ] Cancelled downloads keep resumable partials, model loads are atomic, endpoint requests are connection-bound, and tunnel startup is bounded at thirty seconds
- [ ] Shutdown escalates from cancel events to subprocess termination to a forced exit within ten seconds
- [ ] No orphaned FFmpeg or cloudflared process remains after any exit path on Ubuntu
