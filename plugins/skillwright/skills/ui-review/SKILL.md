---
name: ui-review
description: Review an interface you can point at — a live page, a prototype, a design mock — against a usability and accessibility standard, reporting only the violations actually found. Use when an interface is being assessed for problems, including accessibility checks. NOT for deciding which screens and states a prototype needs, which is `prototype-brief`, and NOT for generating or restyling UI — that belongs to whichever UI-building skill or tool you have.
---

# UI Review

Review the target interface against a **stated standard**. Default: **Nielsen's 10 usability heuristics** and **WCAG 2.2 AA**. Where the caller names another — a design system, a brand guide, a different WCAG level — use that and say which you used.

The interface has to be something you can point at: a live page, a running prototype, a mock. Where there is nothing to point at yet, the question is which screens and states a prototype needs, and `prototype-brief` holds it.

**Report only what is actually violated.** Do not walk the standard end to end. A criterion with nothing to say is omitted, not filled in with a paragraph saying it looks fine.

**Every finding must be anchored** to the element or region it is about. A problem you cannot point at does not go in the report.

Rate severity on Nielsen's 0–4 scale, and give the basis in one clause (frequency × impact × persistence) rather than the bare number.

Deliver one table, most severe first:

| 位置 | 违反项 | 严重度 | 怎么改 |
|---|---|---|---|

Keep argued judgements and specification failures distinguishable in it — the reader's options differ. A WCAG criterion is pass/fail and not negotiable; a heuristic finding can be argued down.

Close with what you could not evaluate and why — states you could not reach, viewports you did not check, flows requiring credentials.

## Coverage — say this in the report

**One pass by one evaluator is not an audit.** Heuristic evaluation assumes 3–5 independent evaluators; Nielsen's figures put a single evaluator at roughly 35% of the problems present (about 42% of major ones, 32% of minor). You are one evaluator. State this at the top of the report so the reader does not read a short findings list as a clean bill of health.

## Gotcha

**Look at the thing, not at a description of it.** Contrast, truncation, overlap, spacing and visual hierarchy are not in the markup, and not in your recollection of the site. A live page has to be opened in a real browser and observed; a mock has to be viewed as an image. If neither is possible, say so and stop — do not fall back to reading source or working from memory and present that as a review.
