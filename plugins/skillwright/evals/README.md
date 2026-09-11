# evals

Cases for `claude plugin eval`. One directory per skill, one per case below that;
each case is a `prompt.md` plus a `graders/` directory.

The eval directory sits beside `skills/`, not inside any one of them — the runner
takes a plugin, not a skill, and reads a single eval directory for the whole
plugin. Copying one skill's directory therefore does not carry its cases; that is
intended, since the cases are for whoever maintains the skill.

Two standing rules, both bought with defects found the hard way:

- **Whoever writes a grader works from the failure, not from the skill body.**
  Graders written against the wording measure whether the body was restated. Three
  of the four defects in the first round came from this.
- **A grader that contradicts its own case is a defect in the grader.** Demanding
  the full pinned form in a case that exists to test the honest exit fails a
  correct answer.

`results/` is git-ignored. Anything worth keeping gets picked out by hand — copying
the run directory wholesale once dragged an 84 MB browser profile in with it.
