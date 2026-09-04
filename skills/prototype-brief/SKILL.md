---
name: prototype-brief
description: Decide what a prototype has to contain before anyone draws it — which screens, which state of each, and which assumption the prototype exists to falsify. Use this whenever someone is about to mock up, wireframe, sketch or "just quickly put together" a prototype, screen, flow or demo and no screens-against-states inventory exists yet, including when they ask only for the drawing. The drawing itself belongs to whichever UI-building skill or tool is at hand, which this hands the table to.
---

# Prototype Brief

Produce the brief. Draw nothing.

## The table

Walk the user's task once and list what they see. Screens come from the flow, not from the sitemap — a screen no path reaches does not belong in this prototype.

| Screen | Empty | Loading | Partial | Error | Ideal |
|---|---|---|---|---|---|

Mark ✓ where the state can occur and — where it cannot. Where "cannot" is a design decision rather than a fact of the data, say so in one clause.

Empty and error are where products are actually judged, and they are the states that surface late — after the layout has hardened around the ideal case. Filling the whole row is the cheap moment to find that out.

## The hypotheses

Number them, and for each say what would count as failing.

1. *what you believe* — falsifiable by this prototype? yes / no, and by what observation

If nothing in the table can falsify a hypothesis, either a screen is missing or that hypothesis belongs to a later round.

## Out of scope

One line naming what this prototype deliberately leaves out. Without it every absence reads as an oversight and review spends itself on the wrong thing.

## Then hand off

Ask whether to build it, and with what — whichever UI-building skill or tool this project uses. The table carries over unchanged: screens and their states are the build list.

## Gotcha: a prototype that cannot fail is a picture

Drawing is the pull here: a plausible screen is quick and looks like progress. But the artefact earns its cost by making one belief cheap to test, and a prototype nobody can be wrong about has bought the drawing and returned nothing. When the hypothesis list comes out empty, say that plainly — this is a picture, and a picture is the right thing when the decision has already been made.

## Gotcha: the previous version's decisions are not yours to drop

Where a prototype already exists, its layout encodes choices someone agreed to. Redesigning from scratch is easier than reading it, and the new version will look better while quietly discarding them. Read the previous brief and prototype first; where the new flow contradicts a confirmed decision, name the conflict and what reversing it costs before anything changes.
