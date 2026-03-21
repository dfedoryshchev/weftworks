# spec-review checklist

run this over a spec before the agent executes it. a bad spec is cheaper to fix than a bad
execution.

- [ ] is "done" stated as checkable invariants, not intentions?
- [ ] is anything out of scope named explicitly?
- [ ] can each invariant actually be checked (test, command, eyeball)?
- [ ] would a stranger read the same meaning of "done" as me?
- [ ] is there a failure exit - what happens when an invariant can't be met?

if two or more are no, the spec isn't ready. don't start.
