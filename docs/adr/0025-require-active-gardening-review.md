# Require active gardening review

Agents operating this garden should actively participate in gardening, not only validate imports and perform promotions.

**Context**

The protocol has become good at importing, repairing, reconciling, and gating learning packets. That is necessary, but it risks making the agent a clerk: it can move Markdown around while missing the meaning of the new knowledge in the context of the whole garden.

The user wants the agent to notice unexpected links, emerging narratives, protocol pressure, next learning paths, drift, over-optimization, and moments where the garden may be moving in an unhelpful direction.

**Considered Options**

- Keep the agent limited to mechanical validation and promotion.
- Let the agent give informal advice in chat without recording it.
- Require a gardening review step at packet and promotion boundaries.
- Promote all agent insights directly into trusted wiki notes.

**Decision**

Add `garden.review` as a first-class operation. After packet import and around promotion, the agent should write or update a gardening review when there is meaningful sense-making to record.

For packet-specific reviews, use:

```text
learning/packets/<slug>/artifacts/gardening-review.md
```

The review may include unexpected links, emerging narratives, protocol design pressure, next learning ideas, risks, warnings, and proposals. It remains advisory and untrusted until the user approves any resulting promotion or patch.

**Consequences**

The garden gets an active steward, not just an import pipeline. This should help the user see compounding themes and avoid blind drift.

The cost is more agent judgment and more potential noise, so gardening review must stay lightweight and optional when there is nothing meaningful to say. It should not become a ritual that blocks learning.
