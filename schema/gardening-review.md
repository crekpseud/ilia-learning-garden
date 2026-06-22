# Gardening Review

Gardening review is the active sense-making step that keeps the agent from behaving like a passive importer.

## Purpose

After a packet arrives or trusted knowledge is promoted, the agent should ask what the new material means in the context of the whole garden.

This is different from validation. Validation asks whether the packet obeys the protocol. Gardening review asks whether the garden itself is learning something, drifting, overfitting, or developing a narrative the user may not yet see.

## Triggers

Run gardening review:

- after a learning packet is imported and locally reconciled
- before or after promotion into the trusted wiki
- after a major protocol decision
- when the user asks for garden maintenance, direction, next learning ideas, or "what are we missing?"

## Output Location

For packet-specific review, write:

```text
learning/packets/<slug>/artifacts/gardening-review.md
```

For whole-garden review, write under a packet only if the review belongs to that packet. Otherwise, record the outcome in `log.md` and propose a future `wiki` or `docs` artifact only after discussion.

## Review Questions

The agent should consider:

- What does this knowledge mean in the context of the whole garden?
- Does it pressure the protocol itself?
- Does it create unexpected links to existing trusted notes or user knowledge?
- Is a larger narrative forming that the user may not be aware of?
- What nearby learning paths would compound this knowledge?
- Is the garden losing track, moving in an unhelpful direction, or obsessing over low-value mechanics?
- Are there useful proposals: patches, maps, next packets, concept promotions, pruning, or deferred questions?
- What should remain unresolved until the user has human contact with the material?

## Boundaries

The agent may propose, warn, connect, and question.

The agent must not:

- promote trusted notes without approval
- convert speculation into trusted knowledge
- treat every interesting connection as a required task
- turn gardening into ritual overhead that blocks learning
- overfit the garden to protocol mechanics at the expense of the user's curiosity

## Tone

Gardening review should be opinionated but humble. It should surface possibilities and risks, not pretend to know the user's final interpretation before human contact.
