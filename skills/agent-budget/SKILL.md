---
name: agent-budget
description: size a delegated task before you start it, and read the signals that say you sized it wrong
---

# agent-budget

every delegated task gets a budget whether or not i set one. sizing it up front:

1. **name the artifact it hands back.** one diff, one file, one answer. a task that returns
   "an understanding" has no ceiling and will use all of it.
2. **count what it must read, not what it writes.** a one-line fix in code nobody has mapped
   is the expensive one; the reading is the spend.
3. **give the first attempt the smallest budget that could plausibly work.** it's a probe -
   its job is to tell me the real size, not to finish.
4. **write the stop down before it starts**: how many attempts, and what happens after the last.

plan-first already asks for the files you expect to touch and the check for "done". that answer
is the budget - if the plan can't name them, sizing is guesswork.

## reading the miss

- **too small:** output truncates, it re-derives what it already established, the same file gets
  read three times. don't top it up mid-run - the run is the wrong shape. re-scope and restart.
- **too big:** it did the ask then kept going. room left over gets spent, so treat gold-plating
  as a sizing symptom and let eval-before-merge separate the ask from what arrived with it.
- **raise once.** still short means it's two tasks: split when half is survey and half is
  change, and hand the reading on as an artifact (patterns/multi-agent-handoff.md).

guardrails caps an autonomous run; this is that ceiling scoped to one handed-over task. a budget
is a claim about how big the task is - when the run breaks it, fix the claim.
