# 04 — Versioned cross-platform settings schema

**What to build:** One settings document serves both platforms without either overwriting the other's meaning, and a corrupt or unknown value never costs a user their configuration.

**Blocked by:** 01

**Status:** ready-for-agent

- [ ] A file with no `schema_version` is treated as v1 authored by Windows
- [ ] `shared`, `platforms.<os>` and `backends.<name>` sit beside the untouched legacy flat keys
- [ ] Resolution order is platform, then shared, then legacy flat, then derived default
- [ ] Only a Windows process writes the flat block; Ubuntu writes only `shared` and `platforms.linux`
- [ ] Paths under the checkout are stored relative with forward slashes; paths outside it are stored per platform
- [ ] `ui_scale_percent` is canonical, legacy `ui_scale` is mirrored on Windows writes, and a stored value below 10 reads as a multiplier
- [ ] First run no longer persists a backend; every reader derives its own default
- [ ] Writes are atomic via temp file, fsync and replace
- [ ] A value this build cannot honour is ignored for the session and left on disk untouched
- [ ] Unknown keys and namespaces round-trip untouched
