# 06 — Download integrity and retry

**What to build:** An interrupted or failed model download can never be mistaken for a complete one, and a flaky connection no longer costs the user their progress.

**Blocked by:** 03

**Status:** ready-for-agent

- [ ] Downloads write to a `.part` sibling and atomically rename on completion
- [ ] A file at its final name is complete by construction, and an interrupted download is never reported ready
- [ ] Resume continues from the partial using a byte range request
- [ ] A transient mid-stream failure retries three times with backoff, keeping the existing primary-to-fallback source switch
- [ ] A connect or DNS failure stops immediately without retrying
- [ ] A failed download keeps its partial and offers an explicit resume
- [ ] On Linux the TLS chain ends at system trust with a `ca-certificates` remedy, and the Windows chain is unchanged
- [ ] Linux never downloads the Windows FFmpeg archive or the Windows cloudflared binary
- [ ] Silero VAD is ensured for both the 0.6B and the 1.7B selection
