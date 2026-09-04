---
name: heuristic-evaluation
description: Review an existing web page or site against Nielsen's 10 usability heuristics and WCAG 2.2 AA, reporting only the violations actually found. Use when the user asks to review, audit, critique, or find problems in a page or site that already exists — including accessibility checks. NOT for generating, restyling, or beautifying UI — that belongs to whichever UI-building skill or tool you have.
---

# Heuristic Evaluation

Run a heuristic evaluation of the target page against **Nielsen's 10 usability heuristics** and **WCAG 2.2 AA**.

**Report only what is actually violated.** Do not walk all ten heuristics. A heuristic with nothing to say is omitted, not filled in with a paragraph saying it looks fine.

**Every finding must be anchored** to the element or region it is about. A problem you cannot point at does not go in the report.

Rate severity on Nielsen's 0–4 scale, and give the basis in one clause (frequency × impact × persistence) rather than the bare number.

Deliver one table, most severe first:

| 位置 | 违反项 | 严重度 | 怎么改 |
|---|---|---|---|

Close with what you could not evaluate and why — states you could not reach, viewports you did not check, flows requiring credentials.

## Coverage — say this in the report

**One pass by one evaluator is not an audit.** Heuristic evaluation assumes 3–5 independent evaluators; Nielsen's own figures put a single evaluator at roughly 35% of the problems present (about 42% of major ones, 32% of minor). You are one evaluator. State this at the top of the report so the reader does not read a short findings list as a clean bill of health.

**WCAG is an addition, not part of the method.** Heuristic evaluation is expert judgement against heuristics; WCAG conformance is line-by-line checking against a specification. Both are in scope here, but keep them distinguishable in the table — a heuristic finding is an argued judgement, a WCAG finding is a pass/fail against a stated criterion.

## Gotcha

**Look at the rendered page.** Open it in a real browser and observe it. Contrast, truncation, overlap, spacing and visual hierarchy are not present in markup — evaluating from the URL, the HTML source, or recollection of the site produces findings that are confidently wrong. If the page will not load, say so and stop; do not fall back to static analysis and present it as a review.
