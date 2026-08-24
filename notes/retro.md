# retro

## nov 2025 - what didnt work

- tried keeping specs in my head for "small" changes. every time i skipped the spec, verify
  turned into arguing with the agent about what "done" meant. write the spec even when it
  feels like overkill.
- the test-first skill had a wrong path in it for two weeks before i caught it. skills need
  the same review as code.
- too many skills too fast, some overlap. wants a cleanup pass at some point.

## may 2026 - what stuck

- the loop is the thing. the individual skills are just its steps written down.
- safe-refactor gets reached for more than any other skill. most of my work is changing code
  i didn't write.
- unified the skill files this month - they'd drifted into three slightly different shapes.

## aug 2026 - coming back cold

a few weeks away from this, then read it back like someone else wrote it. that is the only
honest test of whether a convention carries, and three things did not.

- three of these claim the slot before a merge and nothing puts them in order. code-review
  reads the diff, eval-before-merge checks against a fixed bar, and step 4 of the loop
  verifies the invariants. every doc lists all three. no doc says which runs first, or
  whether the review sits inside verify or ahead of it.
- plan-first and the spec template ask for the same answers. the loop sends you to plan-first
  for step 2, but plan-first also wants the goal in one sentence and how you'll know it
  worked, and that is what the spec template is for. two front doors into one room.
- the skills that name other skills are the ones that survived. safe-refactor sends you to
  dependency-check at step 2 and to a red test at step 4, so it re-reads as a route you can
  follow. the flat ones are one idea each with no exits, and cold i had to hold three of them
  side by side to work out what order they went in.

not fixing any of it here. writing it down while it still looks strange, because give it a
week and i'll have re-learned the order and stop being able to see the gap.
