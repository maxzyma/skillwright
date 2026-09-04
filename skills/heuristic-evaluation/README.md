# heuristic-evaluation

## What it does

Reviews a web page or site that already exists against Nielsen's ten usability heuristics and WCAG 2.2 AA, and reports only what it actually found violated. Output is one table ordered by severity — location, what is violated, severity on Nielsen's 0–4 scale, how to fix it — closed by a statement of what could not be evaluated.

It reviews. It does not design, restyle or rebuild.

## When to reach for it

Ask for a review, audit or critique of a page or site, or for an accessibility check. The skill is model-invocable: a missed trigger means a review silently does not happen, which costs more than an unwanted one.

Generating or restyling UI belongs to whichever UI-building skill or tool this project uses, which holds the broad trigger for it.

## It's working if

- Findings are anchored. Every row names an element or region you can go look at. A row you cannot point at means the review was done against markup or memory rather than the rendered page.
- Fewer than ten heuristics appear. Ten means it walked the list instead of reviewing the page.
- The report opens by saying it is one evaluator's single pass. Without that line a short findings list reads as a clean bill of health, which it is not.
- Heuristic findings and WCAG findings stay distinguishable — the first is an argued judgement, the second a pass/fail against a written criterion.

## It's not working if

- Severity ratings appear as bare numbers with no basis stated.
- The report was produced without the page having been opened in a browser.

## Coverage, and why the report has to admit it

Heuristic evaluation assumes three to five independent evaluators. Nielsen's own figures put a single evaluator at roughly 35% of the problems present — about 42% of the major ones, 32% of the minor — with five evaluators reaching roughly 75%.

One agent is one evaluator. So a clean-looking report from this skill means "one pass found little", not "the page is sound", and the skill is required to say so in its own output. Treat its results as a first pass that narrows where to look, not as an audit.

## Where it fits

| Skill | Owns |
|---|---|
| **heuristic-evaluation** | finding problems in a page that exists |
| whichever UI-building skill or tool you have | building and restyling pages |

## Design record

| | |
|---|---|
| **Case** | ① — `heuristic evaluation` is the established name of the method (Nielsen & Molich, 1990) and, as a fixed phrase, carries that sense. The competing sense in software is "heuristic evaluation **function**" in game search, which normally appears with the noun and in an algorithmic context. |
| **Side effect removed** | Two. The method's ceremony — walking all ten heuristics whether or not they apply — is cut by requiring only violations found. Its assumption of three to five evaluators cannot be met by one agent, so the coverage limit is pushed into the skill's own output rather than left in these notes. |
| **Output form pinned** | One severity-ordered table with four named columns, followed by a statement of what went unevaluated. |
| **Trigger width** | Model-invocable. A missed review costs more than an unwanted one, and the description carves the boundary against UI-building by naming the role rather than a product — the neighbour is not guaranteed to be installed. |
| **Deliberate extension** | WCAG conformance is not heuristic evaluation — one is expert judgement against heuristics, the other line-by-line checking against a specification. Both are in scope here; the body requires them to stay distinguishable in the table. |
