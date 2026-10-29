---
"sessionpipe-core": patch
"sessionpipe": patch
---

Codex's config.toml keeps its CRLF line ends through `install` and `uninstall`: the notify line goes in with the file's own line end, and `uninstall` leaves the file byte-identical, as it already did for an LF file.
