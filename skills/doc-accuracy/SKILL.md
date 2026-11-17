---
name: doc-accuracy
description: check what a doc claims against the source it describes, before the agent trusts a stale line
---

# doc-accuracy

the agent reads the doc before the code, and when they disagree it believes the doc. so every
line in a doc that can be wrong is a claim, and claims get checked like code:

1. **list the claims.** paths, names, counts, defaults, "X does Y". the prose around them
   can't be wrong in the same way; these can.
2. **check each one at its source.** open the file the path names, read the function the
   sentence describes. a type that allows a value doesn't mean the code ever produces it -
   follow the call that actually runs, not the neighbour that looks the same.
3. **can't check it, narrow it.** keep what you verified, drop the rest. an under-claim costs
   the reader a second look; an over-claim sends them, or the agent, the wrong way.
4. **one wrong claim, re-check its neighbours.** whatever let it through wrote the lines
   next to it too.
5. **the other direction.** a rename or a delete greps the docs for the old name in the same
   change (dependency-check, aimed at prose).

the ones that got through here were the plain kind: test-first pointed at a folder that never
existed (notes/retro.md), and the readme's list of what's here fell behind the tree. a count
is cheapest to keep right by not writing one. runs alongside code-review on any diff that
touches a doc.
