---
name: dependency-check
description: map what depends on a file before editing it so a change doesn't surprise you
---

# dependency-check

before editing anything load-bearing:

- who imports this, and what does it import?
- is it called in a hot path or a loop?
- does anything rely on its current (maybe wrong) behaviour?

the agent reads the callers before it touches the callee. understand what you're standing on
before you move it.
