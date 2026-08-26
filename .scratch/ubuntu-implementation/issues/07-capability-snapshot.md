# 07 — Backend capability snapshot

**What to build:** Every browser client renders platform capability, setup state and remedies from one backend-provided snapshot, in the user's own language, and never guesses.

**Blocked by:** 03, 04

**Status:** ready-for-agent

- [ ] The backend serves one canonical snapshot and the frontend never infers capability from labels or filenames
- [ ] Each backend and feature carries ready, setup required, machine unavailable or platform unsupported, plus a separate model state
- [ ] Reasons and remedies are a code plus parameters, rendered through the existing i18n dictionary
- [ ] Platform-unsupported choices do not appear in selectors, and machine-unavailable choices appear disabled with a remedy
- [ ] Ubuntu derives OpenVINO CPU with the 0.6B model without overwriting an unsupported Windows backend preference
- [ ] Windows-only integrations appear only in a collapsed not-supported section and never count toward health
- [ ] A missing or failed preferred model never causes a silent model switch
