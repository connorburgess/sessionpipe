---
"sessionpipe": patch
---

`sink add` and `sink remove` rewrite the hooks when a sink crosses tier 0, as `install`'s own message says they will; before, the hooks stayed the lean set, `status` read `stale`, and `doctor` blamed an old node or script path. `doctor` now says which set the hooks are and why that no longer matches, when that is the cause.
