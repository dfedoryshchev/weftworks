---
name: commit-discipline
description: small, single-purpose commits with honest messages
---

# commit-discipline

- one logical change per commit.
- the message says what changed and why, not how.
- never commit code you can't explain.
- stage explicit paths, not everything at once.

## atomic vs batch

default to atomic - one change, one commit. batch only when the pieces are meaningless apart
(a rename across ten files, a mechanical format pass). if a reviewer would want to look at one
piece on its own, it is its own commit.
