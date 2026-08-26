# 02 — CI skeleton and uv export guard

**What to build:** Every pull request gets an automated Ubuntu 24.04 check that the documented setup path still works and that the generated requirements file has not drifted from the lock.

**Blocked by:** 01

**Status:** ready-for-agent

- [ ] A workflow runs on `ubuntu-24.04` for every pull request
- [ ] It installs the documented apt prerequisites and runs `uv sync`
- [ ] It fails when `requirements.txt` differs from `uv export` output
- [ ] The job completes without contacting Hugging Face
- [ ] Total runtime stays within a few minutes
