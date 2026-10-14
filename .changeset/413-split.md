---
"sessionpipe": patch
---

A receiver's 413 no longer wedges a sink. HTTP.md §2 says halve the batch and retry, and drop a single event over the limit; the worker instead stopped the sink for the run, and the next worker built the same batch from the same cursor and got the same answer, so every session behind an oversized batch never arrived (two 413s in one day's log). The batch is now halved and read again from the cursors; one event the receiver won't take is dropped, logged with its id, and passed.
