# skillwright

**English** · [简体中文](README.zh-CN.md)

Agent skills built to one method — and the method itself.

|  |  |
|---|---|
| **Core idea** | Context is not storage — it is the solution space the model would otherwise search. Only two kinds of line earn space: its blind spot, and its prior |
| **The bet** | A borrowed term appreciates as the model improves; a hand-built taxonomy becomes a liability that overrides what the model later learned |
| **Clearest instance** | A published skill that does real work in 321 bytes, because its name is a term that already carries a practice |
| **What follows** | Borrow the term; spend the body cancelling what it drags in and pinning the output form |
| **Two conditions** | The term must be one the model has seen, *and* the sense you need must be the one it points at |
| **Where it stops** | Skills that produce a judgement rather than an artefact do not get to be two clauses long |
| **What makes this repo different** | Name and trigger are decided before the body exists — the body is the remainder. All four decisions are recorded per skill; cannot fill the record, does not go in |

## What this is

A `-wright` is someone who makes things — shipwright, playwright. But every skill is designed by
someone; *designed* on its own claims nothing.

**Here the design does not happen in the body. It happens above it — at the name and the trigger.**
That layer is settled first and the body is its remainder, rather than rules written first and a
label fitted afterwards.

The questions that settle it are below, which is enough to audit this repository against itself.

## The core idea

**Context is not storage. It is the solution space the model would otherwise search.**

Every line you write narrows a range it would have explored on its own. So the length of a prompt was
never a cost question — it is a measure of **how much you decided on its behalf**.

A shorter prompt wins at equal quality not because it saved room, but because **the judgement stayed
on the model's side**. One rule fewer is one more decision left to it.

And this is the only way of writing that **grows as the model grows**. A borrowed term is worth more
next year: every level the model gains in understanding that genre, your prompt gains for free. A
hand-built taxonomy is a liability next year: it welds your current understanding into the body and
then **overrides** the better answer the model has since learned.

**If you are betting the models get stronger, do not write today's understanding down as a rule.**

So what to pursue is not fewer words. It is that **every line is spent on something the model cannot
know, or knows but will not do unprompted**. The first is its blind spot; the second is its prior.
Only those two earn space. Every other line is a judgement you took out of its hands.

LLM-native is not doing the work and handing it over. It is **leaving the work to it**.

## The clearest instance

Anthropic's `eli5` skill is **321 bytes** — frontmatter and two lines of body. No audience taxonomy,
no analogy library, no tone rules, no examples, no checklist, no code. It produces good explanations
anyway.

Often misreported as officially curated: it is by an Anthropic engineer on the Claude Code
team, distributed through `anthropics/claude-plugins-community`, a **community** marketplace
Anthropic hosts. It is in neither curated catalogue (`anthropics/skills`,
`anthropics/claude-plugins-official`). Employee-authored, community-distributed — which affects what
support you can expect, not what the artefact demonstrates.

## What follows: borrow before you rebuild

**`ELI5` is not a description. It is a genre.** It has communities, conventions and an enormous
number of worked examples on the open internet. Naming it pulls all of that in at once, and the
pretrained knowledge of what the genre looks like done well outweighs any audience taxonomy someone
could write by hand.

So the body does not explain how to explain. It does two other things:

1. **Cancels the name's side effect.** Read literally, ELI5 produces baby talk — you do not want
   "imagine you have a box of crayons" about your auth module. The body restates the audience as
   someone who knows nothing about the *topic*: the compression is kept, the age is dropped.
2. **Pins the output form.** An HTML artifact, big pictures, few words. The form then does the rest
   — you cannot stack jargon inside that constraint.

**The leverage and its correction live in different places.** The genre activation sits in `name` and
`description`, which is also where trigger routing and the user's own reading happen; the correction
and the form constraint sit in the body. Neither dilutes the other.

The commit history shows the author tuning exactly these two things and nothing else: `an idiot that
knows nothing` → `someone who knows nothing`, and `in a HTML page` → `a HTML artifact`. The
`description` was never changed.

## Two conditions, and they are independent

| Axis | Question | Fails when |
|---|---|---|
| **Signal strength** | Has the model seen this term at all? | In-house names, personal coinages, team jargon |
| **Sense alignment** | Of its senses, is the one you need the dominant one? | `design tree` reads as a CAD feature tree, not a hierarchy of design decisions |

A term can be very strong on the first axis and wrong on the second. **That combination is the one
people miss** — it produces skills whose bodies assume an activation that is going somewhere else.

## Where the method stops

**Judgement does not compress like execution.** ELI5 produces a thing, so one name mobilises the
whole practice. A skill that produces a *conclusion* — is this page usable, is this name doing its
job — activates at best one criterion per term, and the **combination** of criteria is the judgement.
Composites of several decisions rarely have names of their own, so those bodies do not get short.

Two moves keep them from getting long by default:

- **Recurse once.** The composite may have no name, but the criteria you write have vocabulary of
  their own, and it is often borrowable. `skill-design` is the case in point: the whole has no name,
  yet `precising definition`, `stipulative definition` and `false trigger / missed trigger` each
  carry a concept the body would otherwise have to spell out.
- **Split when the decisions need not be made together.** Several skills that each borrow a name beat
  one that borrows none.

**A borrowed name also brings preconditions you may not be able to meet.** Heuristic evaluation
assumes three to five independent evaluators; Nielsen's own figures put one evaluator at roughly 35%
of the problems present. One agent is one evaluator. When that happens, the skill says so **in its
own output** — otherwise a short findings list reads as a clean bill of health.

## The method, as four questions

Answered before a body is written, and answerable of any skill that already exists:

1. **Which case is the name in?**
   - ① the sense you need is the term's only sense → borrow it; the body then only removes the side
     effect and pins the form
   - ② the sense is among its senses but not the dominant one → borrow it and narrow it in one clause
   - ③ no term, or none of its senses is the one you need → write decidable criteria, and do not
     assume activation. Then recurse once
2. **What does the borrowed name drag in that you do not want?** Remove it in one clause.
3. **Is the artefact easier to describe than the behaviour?** Then constrain the artefact.
4. **Which costs more, one false trigger or one missed trigger?** Default narrow.

Then: add constraints only after watching one fail.

## The design record

Each skill's `README.md` answers the same four, about itself:

| | |
|---|---|
| **Case** | ①, ②, or ③ — and why it is not one of the other two |
| **Side effect removed** | what the borrowed name brings that the body cancels |
| **Output form pinned** | the artefact the skill must produce |
| **Trigger width** | narrow or wide, and which error that choice accepts |

**A skill that cannot fill those four lines does not belong here.**

## Admission criteria

- **The body is addressed to a model that already knows the domain.** No argument, no confidence
  ledgers, no notes to self. The one justification that earns space in a body is a reason that keeps
  an instruction from losing to a prior — which is what a `Gotcha` section is for.
- **Preconditions that do not hold get stated in the output**, not in a footnote.
- **Constraints are added after watching one fail**, not in anticipation.
- **Criteria are stated with their evidence strength.** Thin is allowed; silent is not.
- **No invented methodology names.** A fabricated term activates nothing while reading as though it
  carries authority, so nobody can tell the body is doing all the work.

## The skills

| Skill | What it does | Trigger |
|---|---|---|
| [`skill-design`](skills/skill-design) | Decides a skill's name, its body's job and its trigger width before it is written — or diagnoses one that exists. Hands off to `skill-creator` for the build. | explicit only |
| [`heuristic-evaluation`](skills/heuristic-evaluation) | Reviews a page that exists against Nielsen's ten heuristics and WCAG 2.2 AA, reporting only violations found — and stating that one agent is one evaluator. | model-invocable |

Each `README.md` also states how to tell the skill is working, and how to tell it is not.

## Evidence standing

How much each claim rests on:

| Claim | Support | Weight |
|---|---|---|
| Context as solution space (the core idea) | argued, not measured here; the attention dilution and position effects it leans on are documented in the literature but not reproduced in this repository | argued |
| Borrowing beats rebuilding | 321 B against a same-named community implementation of ~8 KB doing comparable work | reasonable |
| The three name cases | one term worked through in full; the cases are asserted, not sampled | thin |
| Form-pinning saves words | one instance, and it may hold only for single-shot artefacts | thin |
| Default-narrow triggers | four skills binding to explicit invocation, two authors, one counter-sample | moderate |
| Judgement vs execution limit | two samples | weak |

Where you hold contrary evidence, prefer it.

## Install

Nothing is published to a plugin marketplace yet. Until it is, copy the directory:

```bash
git clone https://github.com/maxzyma/skillwright
cp -R skillwright/skills/skill-design ~/.claude/skills/
```

Use `.claude/skills/` in a project for project scope, or `~/.claude/skills/` for every project.

Skills here are plain directories with a `SKILL.md`, so they are not Claude-Code-only — copy
`skills/<name>/` into whatever your agent reads skills from. The frontmatter key
`disable-model-invocation` is Claude Code's; other runtimes ignore it and you invoke the skill
explicitly, which is what that key asks for anyway.

## Scope

Skills only. Standing instructions — `CLAUDE.md`, `.claude/rules/` — are deliberately out: they are
not an installable plugin component, so they cannot be versioned or updated through a marketplace,
and most of their value is in specifics that do not survive leaving the machine they were written on.

## License

MIT. The name is not part of the grant.
