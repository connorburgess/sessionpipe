---
"sessionpipe-core": patch
"sessionpipe": patch
---

A hooks file that starts with a UTF-8 byte-order mark (PowerShell 5's UTF8 encoding, older Windows editors) is read like any other and written back with the mark, so `install` hooks it instead of reporting "not plain JSON; not touched", and `uninstall` leaves it byte-identical. The harnesses read such a file themselves.
