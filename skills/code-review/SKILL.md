---
name: code-review
description: a review pass before merge - review the diff against the spec, not the intent
---

# code-review pass

read the diff as if someone else wrote it:

- does it do what the spec said, and only that?
- what breaks if the input is empty, huge, or concurrent?
- is there a simpler version?

the agent that wrote the code doesn't get to approve it without this pass.
