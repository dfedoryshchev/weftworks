# objections and answers

docs/team-rollout.md names three places i'd expect pushback, one sentence each. this is the
longer version: the objection the way someone would actually say it, and an answer that rests
on what's already true of this repo, not on it going well somewhere. none of this has run on a
team either.

## the objections

- **"this is ceremony for a one-line fix."** the loop doesn't ask for a heavy spec on a small
  change, it asks for one invariant. workflow/examples/bugfix-walkthrough.md is a real
  off-by-one fix with exactly one, and the honest note that "the loop scales down." a plan that
  can't name any check at all is plan-first's own abort condition, not a reason to skip it.
- **"characterizing legacy code first is the expensive part."** it is - safe-refactor puts
  tests on code nobody wants to touch before anything visible moves. the honest answer isn't
  that it's cheap, it's that i still reach for it more than any other skill (notes/retro.md),
  which is a bet on the cost being worth paying repeatedly, not a pitch taken on faith once.
- **"it'll get copied in and nobody opens it."** that's the failure mode this repo names for
  itself: "a convention you don't follow is worse than none" (docs/usage.md). the skills that
  held up cold are the ones that name an exit - safe-refactor points at dependency-check and a
  red test, so it reads as a route (notes/retro.md). one with no exits is the one left unread.
- **"this is just tdd with a new name."** mostly, yes - the README says so directly: "this is
  TDD and design-by-contract aimed at an agent." it isn't sold as new; the only addition is
  aiming the same discipline at something that will confidently guess if the check isn't
  written down first.
- **"who reviews the skill file itself when it's wrong."** nobody did, once - a wrong path sat
  in test-first for two weeks in a file only i read (notes/retro.md). that's the actual case
  for team-rollout.md's "give each convention an owner": a skill is a few lines of prose an
  agent follows literally, which makes it code.
- **"three things already fight over the pre-merge slot."** true, and unresolved here too -
  code-review, eval-before-merge and step 4 of the loop all claim it and nothing says which
  runs first (notes/retro.md). team-rollout.md's answer is to settle that order before rolling
  anything out, not to add a fourth process on top of the argument.

not a complete list, just the ones i'd expect to actually hear, answered with what's true of
this repo right now rather than with how it went somewhere else.
