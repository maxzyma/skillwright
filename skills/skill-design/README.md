# skill-design

## What it does

Works through four decisions about a skill before its body gets written: which case its term falls into, what the borrowed term drags in that you have to remove, whether the artefact is easier to constrain than the behaviour, and how wide the trigger should be. Then hands off to `skill-creator`.

It also runs backwards: ask the same four of a skill that already exists, plus three checks that need an artefact to exist (name against body, size against case, sense drift).

It produces a decision, not a file. Nothing is built here.

## When to reach for it

Type `/skill-design`. It is model-invocation-disabled, so it never fires on its own — deliberately, because a skill about skills would otherwise trigger in every conversation that mentions one.

Reach for it when about to write a skill and you have not yet decided what its name is doing, or when an existing skill misfires and you want to know whether the cause is in its design rather than its wording.

Do not reach for it for file layout, progressive disclosure, bundled resources, test cases or evals. Those are `skill-creator`.

## It's working if

- You can name which of the three cases the skill falls into, and say why it is not one of the other two.
- The body gets **shorter** as you work through the steps, not longer. Steps 1–3 are subtractions; if your body is growing, you are answering a question that was not asked.
- You can state what the trigger width costs — which error you chose to make — rather than only that you chose narrow or wide.
- On a diagnosis, at least one finding points at the name or the description, not only at the body. A design review that only ever finds wording problems is not reaching the design.

## It's not working if

- Every step produces a new paragraph in the skill body. That is the failure this whole thing was written against.
- You reach case ③ and immediately coin a term for it.

## Where it fits

| Skill | Owns |
|---|---|
| **skill-design** | the design decisions: which term, what leverage, how wide the trigger |
| `skill-creator` | the build: file layout, progressive disclosure, resources, test cases, evals, description optimisation |

Hand-off runs one way, design → build, and is a question rather than an automatic call: the design conclusions are frequently the whole of what was wanted.

## Design record

| | |
|---|---|
| **Case** | Not one case throughout. **③ for the practice** — "designing an agent skill" has no widely practised name; it is roughly a year old. **② for the name** — `design` is borrowed in its design-phase sense, against implementation. **① at step level** — precising / stipulative definition for the ②/③ split, false-positive / false-negative for trigger width, `recurse` for the ③ exit (which carries its own base case, so the stop costs one word: *once*). The step-level borrows are what keep the body from having to explain those four concepts. |
| **Side effect removed** | From the ② borrow: `design` also reads as visual design, and as a whole activity that includes building the thing. The description narrows it in one clause — assembling files and running evals belong to `skill-creator` — which is why the boundary comes out as a handoff rather than a disclaimer. |
| **Output form pinned** | A four-line design summary: case, what was removed or written in its place, the pinned form, the trigger width and its cost. |
| **Trigger width** | Explicit invocation only, via `disable-model-invocation: true`. The skill is meta, so a false trigger is near-certain in any conversation about skills, while a missed trigger costs little — its subject is a deliberate act, so whoever needs it will ask. |

## Evidence standing

Per-criterion weights are in the [repository README](../../README.md#evidence-standing), alongside
the samples they rest on. The body states only that the criteria are thin, because a body addressed
to an executing model is the wrong place for a ledger.

One entry belongs here rather than there, because it is about this skill and not about the method:
it has produced two skills, both by its author, in one sitting, and its diagnostic mode has been run
three times — twice on that author's own fresh work. **Untested by anyone else; self-assessment bias
unaddressed.**
