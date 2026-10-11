---
name: incident-review
description: find why something broke with an agent doing the reading, without letting it write the story
---

# incident-review

after something breaks, the agent is fast at the reading and too quick with the cause. its
theory arrives fluent and mostly right, and mostly is the problem. so:

1. **read-only first.** no fixes during the review. the scope fence (patterns/guardrails.md)
   is empty: it reads logs, diffs and the run journal, and touches nothing.
2. **timeline from evidence.** every line points at a log entry, a commit or a trace. a line
   it can't point at is a guess - mark it and keep going.
3. **reproduce before you name a cause.** a red test that fails the way it failed live
   (test-first). until then the cause is a lead.
4. **split trigger, cause and gap.** what set it off, why that broke things, and which check
   should have caught it. then who else calls the broken path (dependency-check).
5. **close the gap, not just the bug.** the fix goes through the loop like any change; the gap
   becomes an invariant in a spec or a line in eval-before-merge's bar.

the review ends with two artifacts: the red test, and the check that was missing. a write-up
with neither is a story about the incident.
