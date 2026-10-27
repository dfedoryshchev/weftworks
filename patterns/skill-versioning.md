# versioning skills as they change

a skill is a prompt the agent follows, so it changes the way code does: in git, one change per
commit, and the subject's prefix says what kind of change it was. the kinds i use:

- **refine** adds to a skill without changing what it already says. `refine plan-first: add
  failure-exit criteria` appended a "when to abort" section and left the three steps above it
  alone. `refine commit-discipline: atomic vs batch guidance` did the same.
- **fix** is for a skill that was wrong. test-first told you to keep the test in
  workflow/specs/, a folder this repo never had, from its first commit on 2025-11-04 until
  `fix: test-first skill referenced wrong file layout` on 2025-11-25. 21 days of a wrong
  instruction that an agent would have followed. a fix goes in alone, and the message says
  what was wrong.
- **a new skill** when the change is a different job, not a sharper version of the same one.
  if the new text needs its own description line to say when it applies, it gets its own
  folder instead of a section in someone else's.

keeping them prompt-sized:

- frontmatter is name and description, then a short body. a refine changes the body; a
  different name is a different skill.
- the longest one here is 31 lines. when a refine would push a skill past a screen, or a new
  section has its own trigger, split it. none has needed splitting yet.

which version you have: there's no number on a skill. the version is the commit.
`git log --oneline -- skills/<name>/SKILL.md` lists every change to it, and the prefixes tell
you which were refines and which were fixes. if you copied a folder out, write down the commit
you copied from and diff against it when you pull again.
