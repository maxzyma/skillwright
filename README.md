# skillwright

Agent skills built to one method — and the method itself.

A `-wright` is someone who makes things: shipwright, playwright, wheelwright. Everything here
was **designed**, not collected. That distinction is the whole point, so it is made checkable:
every skill in this repository ships a **design record** stating the four decisions behind it.

## The four questions

Answered before a skill's body is written, and answerable of any skill that already exists:

1. **Which case is the name in?**
   - ① the sense you need is the term's only sense → borrow it; the body then only removes the
     side effect and pins the form
   - ② the sense is among its senses but not the dominant one → borrow it and narrow it in one
     clause
   - ③ no term, or none of its senses is the one you need → write decidable criteria, and do not
     assume activation. Then recurse once: the criteria you write have vocabulary of their own,
     and it may be ①
2. **What does the borrowed name drag in that you do not want?** Remove it in one clause.
3. **Is the artefact easier to describe than the behaviour?** Then constrain the artefact.
4. **Which costs more, one false trigger or one missed trigger?** Default narrow.

A name that already carries a practice does the work a long body would otherwise have to do.
Anthropic's `eli5` is the clearest published instance: 321 bytes, because `ELI5` names an
explanation genre the model already knows, and the body only detaches the literal reading of
"five" and pins the output form.

## What a design record looks like

Each skill's `README.md` states, in four lines:

| | |
|---|---|
| **Case** | ①, ②, or ③ — and why it is not one of the other two |
| **Side effect removed** | what the borrowed name brings that the body cancels |
| **Output form pinned** | the artefact the skill must produce |
| **Trigger width** | narrow or wide, and which error that choice accepts |

If a skill here cannot fill those four lines, it does not belong here.

## Admission criteria

- The body is addressed to a model that already knows the domain. No argument, no confidence
  ledgers, no notes-to-self.
- Where a borrowed protocol assumes conditions a single agent cannot meet — evaluator counts,
  independent passes, a panel — the skill says so in its own output rather than pretending.
- Constraints are added after watching one fail, not in anticipation.
- Criteria are stated with their evidence strength. Thin is allowed; silent is not.

## Layout

```
skills/<name>/SKILL.md     the skill
skills/<name>/README.md    its design record and usage notes
```

Skills are plain directories, so they work outside Claude Code too: copy
`skills/<name>/` into whatever your agent reads skills from.

## Status

Early. Skills are being moved in one at a time; each arrives with its design record or not at
all. Nothing is published to a plugin marketplace yet — until it is, copy the directory.

## License

MIT.
