---
name: skill-design
description: Decide a skill's name, its body's job, and its trigger width before writing it — or diagnose an existing skill against the same questions. Assembling files and running evals belong to skill-creator, which this hands off to.
disable-model-invocation: true
---

# Skill Design

Answer these questions, then hand off to `skill-creator`.

**1. Which case is the name in?**

- ① the sense you need is the term's only sense → borrow it; the body then only removes the side effect and pins the form
- ② the sense is among its senses but not the dominant one → borrow it and narrow it in one clause (a precising definition)
- ③ no term, or none of its senses is the one you need → write decidable criteria (a stipulative definition). Do not assume activation. Then recurse once: the criteria you write have vocabulary of their own, and it may be ①

**2. What does the borrowed name drag in that you do not want?** Remove it in one clause. Where the borrowed protocol assumes conditions a single agent cannot meet — evaluator counts, independent passes, a panel — state that limit in the skill's own output.

**3. Is the artefact easier to describe than the behaviour?** Then constrain the artefact instead.

**4. Which costs more, one false trigger or one missed trigger?** Default narrow; the lever is `disable-model-invocation: true`. Narrow when the skill overlaps a broader one, when its subject recurs during ordinary work, or when it is meta. Where a neighbour holds the same phrases, name it as a handoff rather than writing a disclaimer.

Add constraints only after watching one fail.

## Diagnosis

Ask the same questions of an existing artefact. Further checks need an artefact to exist:

- **Name against body** — a description forced to retract scope means the name over-claimed. Change the name.
- **Size against case** — ① should be short. A long body under a ① name means something borrowable was rebuilt.
- **Sense drift** — where the body defines a term the name also uses, check the two still agree.

## Output, then hand off

Report:

- the case — and on ③, the case of the criteria's own vocabulary
- the side effect removed and the sense selected — or, on ③, the criteria written in place of a name
- the pinned output form
- the trigger width and the asymmetry that set it

Cut the body back against the exclusions under *the body has one reader* before handing off.

Then ask whether to invoke `skill-creator` to build it.

## Gotcha: the body has one reader

Write the body for a model that already knows the domain, and for nothing else.

Keep the following out of the body, and route rather than delete it:

- to whatever study produced the criteria — why a criterion holds; what was tried and rejected; how confident you are
- to a `README.md` beside the skill — what the skill is for; how to tell it is working

The one justification that earns space is a reason that keeps an instruction from losing to a prior.

## Gotcha: do not invent a name on case ③

Write the criteria out instead. A fabricated term activates nothing while reading as though it carries authority, so neither you nor a later reader can tell the body is doing all the work.

