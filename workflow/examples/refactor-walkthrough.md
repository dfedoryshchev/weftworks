# worked example: the loop on a small refactor

the four steps on a real-ish task: splitting a function that does two jobs into two.

**spec.** the function parses and formats in one blob. done = parse and format are separate,
same output for the same input, existing callers unchanged.

**plan.** one file. add parse() and format(), have the old function call both. no behaviour
change.

**execute.** agent makes the split.

**verify.** run the existing tests, same output. no caller touched. done.

nothing clever here. the value is that "same output for the same input" was written down
before the agent started, so verify was a yes or no, not a vibe.
