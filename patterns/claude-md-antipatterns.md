# claude.md anti-patterns

things i've put in a claude.md that made agents worse, not better:

- **a wall of prose.** the agent skims it. rules it can't find, it won't follow.
- **contradictions left in.** "always X" in one section, "never X" in another, and the agent
  picks one at random.
- **stale status.** "currently working on Y" from three weeks ago, now a lie it trusts.
- **inlined code that drifts.** the sample in the doc and the real code disagree; the agent
  believes the doc.
- **politeness.** "please try to". rules are rules; hedging reads as optional.

the fix for most of these: shorter, linked, and stale things deleted.
