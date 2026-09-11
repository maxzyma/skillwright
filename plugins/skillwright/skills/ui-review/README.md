# ui-review

## What it does

Reviews an interface you can point at — a live page, a running prototype, a design mock — against a stated standard, and reports only what it actually found violated. The default standard is Nielsen's ten usability heuristics plus WCAG 2.2 AA; a caller can name another and the skill says which it used.

Output is one table ordered by severity — location, what is violated, severity on Nielsen's 0–4 scale, how to fix it — closed by a statement of what could not be evaluated.

It reviews. It does not design, restyle or rebuild, and it does not decide what an interface should contain.

## When to reach for it

Ask for a review, audit or critique of an interface, or for an accessibility check. The skill is model-invocable: a missed trigger means a review silently does not happen, which costs more than an unwanted one.

## It's working if

- Findings are anchored. Every row names an element or region you can go look at. A row you cannot point at means the review was done against markup or memory rather than the interface.
- The report names the standard it used, and does not walk that standard end to end. A row per criterion means it worked through the list instead of looking at the interface.
- The report opens by saying it is one evaluator's single pass. Without that line a short findings list reads as a clean bill of health, which it is not.
- Argued judgements and specification failures stay distinguishable — you can tell which rows you may push back on and which are pass/fail.

## It's not working if

- Severity ratings appear as bare numbers with no basis stated.
- The report was produced without the interface having been looked at — a live page not opened in a browser, a mock not viewed.

## What it is measured to add

Against the same markup with no skill in play, a frontier model finds the same defects — in one controlled run it found slightly more. What separates the two is not detection: it is that the reviewed output says which judgements it could not make, says that one pass by one evaluator is not an audit, and puts the findings in a form you can compare across pages.

So the thing to expect from it is a report you can trust the shape of, not a longer list of problems. Measured 2026-09-11 at n=2 with the same person writing the skill, the cases and the grading.

## Coverage, and why the report has to admit it

Heuristic evaluation assumes three to five independent evaluators. Nielsen's figures put a single evaluator at roughly 35% of the problems present — about 42% of the major ones, 32% of the minor — with five evaluators reaching roughly 75%.

One agent is one evaluator. So a clean-looking report from this skill means "one pass found little", not "the interface is sound", and the skill is required to say so in its own output. Treat its results as a first pass that narrows where to look, not as an audit.

## Where it fits

The dividing line is whether there is something to point at — which is also the precondition for the skill's own rule that every finding be anchored.

| | Input | Output |
|---|---|---|
| [`prototype-brief`](../prototype-brief) | nothing drawn yet | which screens and states are needed |
| whichever UI-building skill or tool you have | a brief | the interface |
| **ui-review** | an interface you can point at | the list of violations |

## Design record

| | |
|---|---|
| **Case** | ③, then ① on the recursion. The activity — examine an interface that exists and report what is wrong with it, without changing it — has no established name, so the name is plain description and the body carries the criteria. The body then borrows two established practices by name: Nielsen's usability heuristics (Nielsen & Molich, 1990) and WCAG 2.2 AA conformance. Those are the default standard, not the skill's identity, which is why swapping the standard costs one clause. |
| **Side effect removed** | Two. The method's ceremony — walking the whole standard whether or not it applies — is cut by requiring only violations found. Its assumption of three to five evaluators cannot be met by one agent, so the coverage limit is pushed into the skill's own output rather than left in these notes. |
| **Output form pinned** | One severity-ordered table with four named columns, followed by a statement of what went unevaluated. |
| **Trigger width** | Model-invocable. A missed review costs more than an unwanted one. Both boundaries are expressed as scope, not as disclaimers: `prototype-brief` is named because it ships in the same plugin and is copied along with this one, while the UI-building neighbour is named by role because it is not guaranteed to be installed. |
| **Generation** | Checked against the 2026-09 frontier generation (Claude Opus 5 / Fable 5.1, GPT-5.5). Untested on smaller models, where activation by named practice is unreliable and the body has to be spelled out regardless. **Re-ask every criterion here at the next release** — the answer to "is this line still needed" expires with the prior it was written against. The Nielsen figures it cites are from NN/g's own studies and are not generation-dependent. |

### Scope, corrected 2026-09-11

It shipped as `heuristic-evaluation`, scoped to "an existing web page or site". Both were wrong, from the same mistake: the scope was drawn around a **method** rather than around the activity.

Every failure the body prevents — reading markup instead of looking, a short list read as a clean bill of health, restyling instead of reporting, findings you cannot point at, working through the list — holds for any standard. The method is a parameter. Drawing the scope at the method's level meant WCAG could only arrive as an appendix ("WCAG is an addition, not part of the method") and the name could not stretch to cover it.

The object was also narrower than the borrowed method's own. NN/g: "Heuristic evaluations are useful for identifying glaring problems in an interface. That interface can be just about anything that users will interact with — including prototypes… The method can be particularly helpful early in the design process." A prototype or a mock qualifies; only the remedy ("open it in a real browser") is specific to live pages, and it is now conditional.

That quote widens the object, not the activity. The same page states the output is a list of identified problems — the method never generates a design, so nothing here reaches back before there is something to point at.
