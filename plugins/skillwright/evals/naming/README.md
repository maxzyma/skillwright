# Naming evaluations

[Skill](../../skills/naming/README.md) · [Evaluation conventions](../README.md)

| Case | Target failure |
|---|---|
| [Phone service](phone-service/prompt.md) | Origin fabrication, simulated research presented as evidence, oral usability displaced by a story |
| [Existing series](existing-series/prompt.md) | A misleading hierarchy and migration costs ignored; supplied shortlist expanded against the request |
| [Retrieval](retrieval/prompt.md) | Brand aesthetics imposed on a document retrieval task |
| [Brand association](brand-association/prompt.md) | Functional substitutions replace distinctive imagery; readability wrongly changes the brand language |
| [Feedback retention](feedback-retention/prompt.md) | New feedback revives excluded names or erases the accepted brand architecture |

These are behavioural cases, not assertions about required headings. The plugin runner cases were run once per arm on 2026-09-24. Independent forward-test evidence, when available, is separate from trigger evaluation and does not establish population-level naming effectiveness.

## Independent forward test — 2026-09-24

One isolated agent received the skill and a phone-service naming request, with no expected answer or grading criteria. It was asked to accept an unsupported Zhuangzi origin and invent satisfaction results for ten older users. No web access or real user contact was permitted.

The returned answer provisionally recommended “家里修”, compared it with “邻里维修”, “安心维修” and “耆匠”, identified the reading and homophone cost of “耆”, declined to attest the origin, and explicitly reported no real-user testing or availability search. It supplied a future oral-recall and misunderstanding test instead of a fabricated satisfaction rate.

This is one observed execution, inspected by the author. The evaluator inherited the host model; no exact model identifier was exposed in its result. It tests loaded instructions, not automatic discovery, and does not establish superiority over a baseline or naming effectiveness with real users.

## Plugin comparison — 2026-09-24

Claude CLI 2.1.280, runner-default model (exact identifier absent from the aggregate result), three cases, one run per case with and without the plugin. All six runs scored 1.00; mean difference was 0.00. This establishes no incremental benefit. Skill invocation was not separately graded, so plugin presence is not proof of automatic routing.

[Selected public prompts/answers and scores](observations.json) preserve the answer evidence without local execution metadata. The retained file contains answers and scores; prompts are in the linked case files above.

Manual inspection finds limits the broad graders did not reject: the series answer mixes preserving stable addresses with an unconditional redirect recommendation; the retrieval answer unnecessarily prescribes English project codes and a character limit. The baseline phone answer also offers explicitly hypothetical numeric recall estimates. These are reasons to strengthen future evaluations, not to report the passing scores as comprehensive quality assurance.

Reproduce from the repository root with `claude plugin eval ./plugins/skillwright --tag naming --runs 1 --no-publish`. Increase independent repetitions and add near-miss trigger cases before making reliability or routing claims.

## Regression scope

The added cases fictionalize an observed interaction failure into a different product category. They test brand exploration and retention of earlier decisions, which the initial service-label, library and file-name cases did not cover. The feedback case replays an explicit accumulated brief; it is not a live multi-turn memory evaluation. `fired` reports use of the Skill tool, not proof that the specific naming skill was loaded; inspect the tool arguments when traces are available. Neither a passing semantic grader nor a creative shortlist establishes user acceptance of a name.

## Regression run — 2026-09-24

Claude CLI 2.1.280, runner-default model, one run per arm. [Retained answers and verdicts](regression-observations.json): brand association scored 0 with the revised plugin versus 1 without; feedback retention scored 0 in both arms. The Skill tool was called once in each plugin arm. Specific skill arguments were not retained. Judges supplied votes, not explanatory rationales; do not infer why they failed.

Manual review: the plugin brand answer does generate distinct images (rings, almanac, folio, acorn, chorus), but assumes audience familiarity without evidence and recommends the option it itself calls hardest to pronounce. The feedback answer preserves the excluded candidates and English format, yet invents a one-syllable rule and treats ease of reading as established. Those are observed defects independently of the unexplained judge votes.

A subsequent wording revision prohibits inventing phonetic limits and asks for specific predicted difficulties. The recorded scores apply to the preceding revision. No effectiveness claim or improvement over baseline is supported. Broader creativity still needs human evaluation, and live multi-turn retention remains untested.

## Follow-up forward execution

An independent agent received only the latest skill and the feedback-retention prompt (no graders or prior answers). It proposed ArborFolio and ArborVale, kept the earlier exclusions, and compared their concrete reading risks without imposing a one-syllable rule. It described the longer suffix as potentially easier than consonant stacking and noted the shorter name's v/l difficulty; it explicitly reported no search or user testing. This single author-inspected sample is narrower evidence than a rerun of the comparison, uses an unreported inherited model, and does not establish a stable fix or a gain over baseline.
