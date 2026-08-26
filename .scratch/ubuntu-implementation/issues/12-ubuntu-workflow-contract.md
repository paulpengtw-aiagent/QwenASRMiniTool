# 12 — Ubuntu workflow contract

**What to build:** Every workflow either works on Ubuntu or explains honestly why it cannot, with no path that leads a user into a silent failure.

**Blocked by:** 06, 07

**Status:** ready-for-agent

- [ ] Exact forced alignment is not offered on Ubuntu, and word timing is presented as proportional estimation
- [ ] Existing alignment settings are preserved but inert, retaining their Windows meaning
- [ ] The aligner model is never downloaded on Linux
- [ ] Starting the endpoint displays the reachable LAN URL and states plainly that other machines on the network can reach it
- [ ] cloudflared is discovered on PATH, and when absent the control is disabled with install instructions and never downloads anything
- [ ] Video conversion and microphone recording show a machine-unavailable state with an apt remedy when FFmpeg is absent
