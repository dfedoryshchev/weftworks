---
name: eval-before-merge
description: check agent output against a fixed bar before merging, not just eyeball it
---

# eval-before-merge

output that changes behaviour doesn't merge on vibes:

- **a fixed set of checks.** for code: the tests plus the verify step. for generated text or
  config: a small rubric you run every time, same inputs.
- **compare against the last known-good**, not against your mood today.
- **record the result** next to the change, so "it passed" is a fact you can point at later.

evals are just tests for things you used to check by feel. write the bar down, run it every
time.
