# 15 — Clean-VM checklist and Ubuntu documentation

**What to build:** A person following only the documentation on a fresh Ubuntu machine reaches a working transcription, and the support claim is backed by a repeatable manual walk.

**Blocked by:** 05, 09, 10, 11, 12

**Status:** ready-for-agent

- [ ] A committed checklist walks a fresh Ubuntu 24.04 VM using documentation only
- [ ] It covers apt and uv install, environment sync, first launch with no models, explicit 0.6B download, transcription, video conversion, microphone recording, an endpoint call from a second machine, and quit
- [ ] The final step confirms no orphaned FFmpeg or cloudflared processes remain
- [ ] The README gains an Ubuntu section matching the checklist exactly
- [ ] Every fatal preflight message has a troubleshooting entry
