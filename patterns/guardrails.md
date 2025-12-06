# guardrails for autonomous runs

before letting an agent run without me watching each step:

- **a spend cap.** a hard ceiling per run. it stops, it doesn't ask forgiveness.
- **a scope fence.** the files and dirs it may touch, named up front. outside that = stop.
- **a check it can't skip.** the verify step from the loop, run before anything is called done.
- **a journal.** one line per run: what it did, pass or fail, cost. so i can see what happened
  without re-reading everything.

autonomy is earned per flow, not switched on globally.
