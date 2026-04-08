---
name: safe-refactor
description: change legacy code you don't fully trust without breaking it - characterize first
---

# safe-refactor

for code that has no tests and no one remembers:

1. **characterize.** write tests that capture what it does NOW, bugs and all. you're not
   fixing yet, you're pinning behaviour.
2. **map the blast radius** (dependency-check skill) - who calls this, what breaks if it moves.
3. **change in small reversible steps**, running the characterization tests each time.
4. **only then** fix the behaviour you actually meant to, with a red test first.

the order matters: make it safe to change before you change it. most "risky refactors" are
just refactors done without step 1.
