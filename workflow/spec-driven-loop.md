# the spec-driven loop

four steps, in order, no skipping:

1. **spec** - what should be true when this is done. inputs, outputs, the invariants that must
   hold. written down, not in my head.
2. **plan** - the steps to get there and the files each touches (see the plan-first skill).
3. **execute** - the agent does the work, one plan step at a time.
4. **verify** - check the result against the spec's invariants. if it fails, go back to spec
   or plan, not a patch on top.

the agent is only as good as the spec and the check. i've been writing specs and tests for a
decade; this just points that habit at an agent.
