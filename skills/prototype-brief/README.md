# prototype-brief

## What it does

Turns "let's make a prototype" into a brief: every screen the flow touches, the state each of them can be
in, and the numbered assumptions the prototype exists to falsify — plus one line saying what it
deliberately leaves out. Then it offers to hand the table to whatever builds the screens here.

It produces a decision about scope. Nothing is drawn here.

## When to reach for it

It is model-invocable and fires on the way into prototyping work, including when the request is only
for the drawing. That is deliberate: whoever skips the states usually does not know they skipped them,
so a missed trigger costs more than an unwanted one.

Do not reach for it to build, restyle or review a page. Building belongs to whichever UI-building skill
or tool this project uses; reviewing what already exists is `heuristic-evaluation`, which ships beside
this one.

## It's working if

- The table has more `✓` outside the Ideal column than inside it. A prototype specified only in its
  ideal state is the failure this was written against.
- At least one hypothesis is marked *not* falsifiable by this prototype. If everything is testable, the
  hypotheses were probably written to match the screens already drawn in someone's head.
- The out-of-scope line names something a reviewer would otherwise have asked about.
- On a second round, the report names a conflict with the previous version — or states there is none.

## It's not working if

- It draws something.
- The states come out as a generic five-row checklist applied identically to every screen, rather than a
  judgement per cell.

## Where it fits

| Skill | Owns |
|---|---|
| **prototype-brief** | what the prototype must contain, and what it is for |
| whichever UI-building skill or tool you have | building and restyling the screens |
| `heuristic-evaluation` | finding problems in a page that already exists |

Hand-off runs one way and is a question, not an automatic call — the brief is often the whole of what
was wanted.

## Design record

| | |
|---|---|
| **Case** | ③ for the practice — "decide a prototype's screens, states and hypothesis" has no single established name. ② for the name: `brief` is borrowed in its design-brief sense, the document written before the work that states what is to be made and why. ① at step level — `empty / loading / partial / error / ideal` states, `user flow`, and falsifiability each carry a concept the body would otherwise have to teach. |
| **Side effect removed** | A design brief drags in client-agency ceremony: background, brand values, deliverable lists, timeline, budget. The body admits only the table, the hypotheses and the out-of-scope line. One inherited property is kept on purpose — a brief is agreed against what was already settled, which is what the second Gotcha enforces. |
| **Output form pinned** | One screens-against-states table, a numbered hypothesis list each marked falsifiable-or-not with the observation that would settle it, and a single out-of-scope line. |
| **Trigger width** | Model-invocable, and the description binds to the moment before drawing. The asymmetry runs the other way from most meta skills: skipping the state inventory is invisible to whoever skipped it, so a missed trigger costs more than a false one. The boundary against whatever holds the broad trigger for building UI is written as a handoff rather than a disclaimer, and by role rather than by product name — the neighbour is not guaranteed to be installed. |

## Evidence standing

Per-criterion weights for the method are in the [repository README](../../README.md#evidence-standing).

Specific to this skill: the five-state axis is a long-standing product-design practice rather than a
measured result here, and the claim that filling the non-ideal states early is cheaper than discovering
them late is **argued, not measured**. Untested against real prototyping sessions at the time of
writing.
