# skillwright

**English** · [简体中文](README.zh-CN.md)

Agent skills built to one method — and the method itself.

A `-wright` is someone who makes things: shipwright, playwright, wheelwright. Everything here was
**designed**, not collected. That distinction is the whole point, so it is made checkable: every
skill ships a **design record** stating the four decisions behind it.

Skills in this repository: [`skill-design`](skills/skill-design) ·
[`heuristic-evaluation`](skills/heuristic-evaluation). What follows is why they look the way they do.

## What 321 bytes buys

Anthropic's `eli5` skill is **321 bytes**: frontmatter and two lines of body. No audience taxonomy,
no analogy library, no tone rules, no examples, no checklist, no code.

It works because `ELI5` is not a description — it is an established explanation genre with its own
communities, its own conventions and an enormous number of worked examples on the open internet.
Naming it pulls all of that in at once, and the pretrained knowledge of "what this genre looks like
done well" outweighs any audience taxonomy someone could write by hand.

Provenance, stated precisely because it is often reported wrong: it is by an Anthropic engineer on
the Claude Code team, distributed through `anthropics/claude-plugins-community` — a **community**
marketplace Anthropic hosts. It is in neither curated catalogue (`anthropics/skills`,
`anthropics/claude-plugins-official`). Employee-authored, community-distributed. That distinction
matters for what support you can expect, not for what the artefact demonstrates.

Its two body clauses spend themselves on something other than explaining how to explain:

1. **It cancels the name's side effect.** Taken literally, ELI5 produces baby talk — you do not want
   "imagine you have a box of crayons" about your auth module. So the body restates the audience as
   someone who knows nothing about the *topic*: the genre's compression is kept, the age is dropped.
2. **It pins the output form.** An HTML artifact with big pictures and few words. The form then does
   the rest of the work — you cannot stack jargon inside that constraint.

The commit history shows the author tuning exactly these two things and nothing else: `an idiot that
knows nothing` → `someone who knows nothing`, and `in a HTML page` → `a HTML artifact`. The
frontmatter `description` was never changed.

So the leverage sits in the name and the description — which is also where trigger routing looks —
while the correction and the form constraint sit in the body. The two do not dilute each other.

## The lever, and where it stops

**Borrow before you rebuild.** If the behaviour you want already has a widely practised name, use the
name and spend the body cancelling what it drags in.

Two things have to be true, and they are independent axes:

- **Signal strength** — has the model seen this term at all? In-house and personal names carry nothing.
- **Sense alignment** — a term can be extremely common and still point elsewhere. `design tree` reads
  as a CAD feature tree far more often than as a hierarchy of design decisions.

A term can be very strong on the first axis and wrong on the second. That combination is the one
people miss, and it produces skills whose bodies assume an activation that is going to the wrong
sense.

**The lever is also weaker for judgement than for execution.** ELI5 produces a thing; one name
mobilises the whole practice, so the body can be two clauses. A skill that produces a *conclusion* —
is this page usable, is this name doing its job — activates at best one criterion per term, and the
**combination** of criteria is the judgement. Composites of several decisions rarely have names of
their own, so those bodies do not get short.

That is not a licence to write long ones. Two moves keep them honest:

- **Recurse once.** The composite may have no name, but the criteria you write have vocabulary of
  their own, and it is often borrowable. `skill-design` is a case in point: the whole has no name,
  yet `precising definition`, `stipulative definition` and `false trigger / missed trigger` each
  carry a concept the body would otherwise have to explain.
- **Split if the decisions do not have to be made together.** Several skills that each borrow a name
  beat one that borrows none.

## Where a borrowed protocol over-promises

A method's name brings its whole protocol, including preconditions a single agent cannot meet.
Heuristic evaluation assumes three to five independent evaluators; Nielsen's own figures put one
evaluator at roughly 35% of the problems present. One agent is one evaluator.

The rule here: when the borrowed protocol assumes conditions that do not hold, the skill says so **in
its own output**, not in a note beside it. Otherwise a short findings list reads as a clean bill of
health.

## The four questions

Answered before a skill's body is written, and answerable of any skill that already exists:

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

## What a design record looks like

| | |
|---|---|
| **Case** | ①, ②, or ③ — and why it is not one of the other two |
| **Side effect removed** | what the borrowed name brings that the body cancels |
| **Output form pinned** | the artefact the skill must produce |
| **Trigger width** | narrow or wide, and which error that choice accepts |

If a skill here cannot fill those four lines, it does not belong here.

## The skills

| Skill | What it does | Trigger |
|---|---|---|
| [`skill-design`](skills/skill-design) | Decides a skill's name, its body's job and its trigger width before it is written — or diagnoses one that exists. Hands off to `skill-creator` for the build. | explicit only |
| [`heuristic-evaluation`](skills/heuristic-evaluation) | Reviews a page that exists against Nielsen's ten heuristics and WCAG 2.2 AA, reporting only violations found — and stating that one agent is one evaluator. | model-invocable |

Each has a `README.md` beside it carrying its design record, how to tell it is working, and how to
tell it is not.

## Admission criteria

- **The body is addressed to a model that already knows the domain.** No argument, no confidence
  ledgers, no notes to self. The one justification that earns space in a body is a reason that keeps
  an instruction from losing to a prior — which is what a `Gotcha` section is for.
- **Preconditions that do not hold get stated in the output**, not in a footnote.
- **Constraints are added after watching one fail**, not in anticipation.
- **Criteria are stated with their evidence strength.** Thin is allowed; silent is not.
- **No invented methodology names.** A fabricated term activates nothing while reading as though it
  carries authority, so nobody can tell the body is doing all the work.

## Evidence standing

Stated so you can weigh the method rather than take it:

| Claim | Support | Weight |
|---|---|---|
| Borrowing beats rebuilding | 321 B against a same-named community implementation of ~8 KB doing comparable work | reasonable |
| The three name cases | one term worked through in full; the cases are asserted, not sampled | thin |
| Form-pinning saves words | one instance, and it may hold only for single-shot artefacts | thin |
| Default-narrow triggers | four skills binding to explicit invocation, two authors, one counter-sample | moderate |
| Execution vs judgement limit | two samples | weak |

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
