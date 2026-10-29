---
"sessionpipe-core": patch
"sessionpipe": patch
---

`install`, `status` and `doctor` read Gemini CLI's version on Windows, where the CLI is npm's `gemini.cmd` shim; before, every Windows install said "could not run `gemini --version`" and the 0.46 check never happened.
