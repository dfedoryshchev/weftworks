# rolling these out to a team

i wrote these for one person - me - and none of it has been run on a team. so this is how i
would introduce them, reasoned from what breaks alone, not from it going well somewhere.

## the order i'd go in

1. **the loop first, the skills second.** workflow/spec-driven-loop.md is the thing worth
   agreeing on up front; the skills are its steps. a team sharing spec -> plan -> execute ->
   verify has settled the argument that actually costs time.
2. **one skill, picked from their pain.** legacy nobody trusts -> safe-refactor. bugs coming
   back -> test-first. delegated runs sized wrong -> agent-budget. all eight at once is a docs
   site nobody opens.
3. **settle the pre-merge order first.** notes/retro.md found three things claiming that slot -
   code-review, eval-before-merge, step 4 of the loop - and nothing saying which runs first.
   alone i re-derive it each time; shared, it is three people doing three defensible things.
4. **one source of truth.** shared conventions in agents.md, tool-specific bits in the tool's
   own file, one pointing at the other (patterns/agents-md.md). keep it under a screen
   (patterns/claude-md-structure.md) or it gets skimmed.
5. **give each convention an owner.** the test-first skill carried a wrong path for two weeks
   before i caught it, in a file only i read. a skill is code; it needs a review and a name.
6. **measure it by what leaves a record.** stated adoption is cheap; guardrails' journal line
   per run - what it did, pass or fail, cost - and eval-before-merge's result recorded next to
   the change are the two traces these conventions already produce. and read plan-first's
   aborts the right way up: work handed back before execution is the loop working, not failing.

## where i'd expect the resistance

- **it reads as ceremony.** the loop says four steps, in order, no skipping, and someone
  holding a one-line fix will say so out loud.
- **characterizing is the expensive ask.** safe-refactor puts tests on the exact code nobody
  wants to touch, before anything visible moves.
- **copied, not adopted.** it lands in the repo, nobody opens it. docs/usage.md has the test:
  a convention you don't follow is worse than none, just noise the agent has to ignore.

the spec-review checklist already carries the team question: would a stranger read the same
meaning of "done" as me? alone that is a discipline i can fudge; shared it is the whole point.
