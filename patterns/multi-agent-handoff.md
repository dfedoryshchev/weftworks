# multi-agent handoff notes

when one agent's output feeds another (planner -> worker, worker -> reviewer):

- **hand off artifacts, not chat.** a written spec or a diff, not "as we discussed". the next
  agent didn't see the conversation.
- **each role gets the smallest context it needs.** the reviewer doesn't need the planning
  back-and-forth, just the spec and the diff.
- **the handoff is a checkpoint.** if the artifact is wrong, stop here, cheaper than letting
  the next role build on it.
- **name who owns the decision.** roles that disagree catch more than roles that rubber-stamp,
  but someone breaks the tie, and it's usually me.

most multi-agent messes i've made were really handoff messes - too much context, or too little.
