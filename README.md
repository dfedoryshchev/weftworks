# weftworks

conventions for working with coding agents (claude code specifically), extracted and sanitized
from a private production setup where i've run agents on real code since 2025.

not a framework. a small set of skills, a workflow, and pattern notes - the habits that make an
agent safe to point at code you care about.

## the idea

two things run through all of it:

- **spec before code.** decide what "done" means, as checkable invariants, before the agent
  touches anything. this is TDD and design-by-contract aimed at an agent.
- **understand before you change.** map what depends on a thing before you move it.

## what's here

- **workflow/** - the spec-driven loop (spec -> plan -> execute -> verify) and its templates.
  the spine; start here.
- **skills/** - small SKILL.md conventions: plan-first, test-first, safe-refactor,
  dependency-check, code-review, commit-discipline, eval-before-merge.
- **patterns/** - longer notes: a claude.md that survives long sessions, guardrails for
  autonomous runs, multi-agent handoffs, agents.md.
- **notes/** - honest retros.

## using them

copy the skill folders into your project's skills setup, or read the workflow and adopt the
loop by hand. take the few that fit how you already work; a convention you won't follow is just
noise the agent has to ignore.
