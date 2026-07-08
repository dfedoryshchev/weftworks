# worked example: the loop on a bugfix

a date-window filter quietly missed items dated on the last day of the range.

**spec.** done = items on the final day of the window are included; every other window result
stays identical. one invariant, one regression guard.

**plan.** reproduce with a failing test first (test-first skill), then the smallest fix.

**execute.** wrote the red test - a fixture with an item on the last day, asserting it comes
back. it failed, confirming the off-by-one. the fix was a less-than that should have been
less-than-or-equal on the upper bound.

**verify.** red test green, all existing filter tests still green. done.

the spec here is almost nothing - one invariant. that's fine, the loop scales down. the win is
that the red test existed before the fix, so "fixed" wasn't a guess.
