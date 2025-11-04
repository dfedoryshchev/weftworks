---
name: test-first
description: red before fix - write the failing test first, watch it fail, then fix
---

# test-first

for any bug or new behaviour:

1. write the test that captures it.
2. run it, confirm it FAILS for the right reason (red).
3. make it pass, and don't touch anything else.

a fix without a red test first is a guess. keep the test next to the spec in workflow/specs/.
