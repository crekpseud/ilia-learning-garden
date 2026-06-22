---
type: concept
status: trusted
created: 2026-06-22
aliases:
  - executable rule
  - first-class rule
  - first-class constraint
derived_from:
  - "[[learning/packets/david-west-object-thinking/packet]]"
---

# Self-Evaluating Rule

## Definition

A Self-Evaluating Rule is a rule represented as a first-class object capable of evaluating, modifying, or participating in behavior rather than being hard-coded into a controller or object method.

## Why It Matters

Self-evaluating rules test a strong [[wiki/concepts/object-thinking]] claim: even rules can become behavioral participants in a system instead of external procedural checks.

This matters when a rule has identity, variation, history, configuration, composition, or domain meaning. Treating the rule as an object can make the design more explicit and movable. Treating every condition as a self-evaluating rule, however, can over-objectify simple logic.

For this garden, the concept is useful because it sits at the boundary between metaphor and implementation. It asks when "make it an object" clarifies responsibility, and when it merely adds ceremony.

## Related Concepts

- [[wiki/concepts/object-thinking]]
- [[wiki/concepts/software-as-theater-metaphor]]
- [[wiki/synthesis/object-thinking-and-the-digital-garden]]
- [[wiki/concepts/the-ritualization-trap]]

## Sources

- [[learning/packets/david-west-object-thinking/packet]]
- [[learning/packets/david-west-object-thinking/sources]]
- [[raw/sources/david-west-object-thinking-notebook]]
