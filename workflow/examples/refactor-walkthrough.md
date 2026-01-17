# worked example: the loop on a refactor

a real one: a module that had grown to do three jobs (load, validate, report) in one file,
where every change to one broke the others.

**spec.** three concerns split into three units. same public function, same output for the
same input, no caller changes. filled in from the template.

**plan.** move validate and report into their own files, leave load as the entry point that
calls them. one commit per move so each stays reviewable.

**execute.** agent moves validate first, runs tests, then report. i watch the diffs, not the
keystrokes.

**verify.** every invariant from the spec, checked: same output on the existing fixtures, no
caller touched, three files where there was one. two held; the report split had quietly
changed an error message, caught at verify and fixed before merge.

the changed error message is the point. without the written invariant "same output", that
slips through as close enough.
