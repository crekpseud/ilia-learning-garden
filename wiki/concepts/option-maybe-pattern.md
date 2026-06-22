---
type: concept
status: trusted
created: 2026-06-22
aliases:
  - Option type
  - Maybe type
  - optional value
  - Result type
derived_from:
  - "[[learning/packets/david-west-object-thinking/packet]]"
---

# Option/Maybe Pattern

## Definition

Option/Maybe Pattern represents absence or possible failure as an explicit value, often through Option, Maybe, Result, nullable-aware APIs, or related monadic patterns.

## Why It Matters

This concept entered the garden through the user's reflection on Null Object, null references, exceptions, and modern C#/.NET direction. It gives the garden a way to compare absence-handling strategies without assuming that every absence should become a Null Object.

Option/Maybe can make uncertainty visible in a type or value shape. It can also move error and absence handling toward explicit composition instead of scattered null checks.

The concept is trusted as a reusable design handle, but its detailed .NET implications still need future learning. It should be compared with Null Object, nullable reference types, exceptions, Result types, and fail-fast design before becoming a strong local doctrine.

## Related Concepts

- [[wiki/concepts/object-thinking]]
- [[wiki/synthesis/object-thinking-and-the-digital-garden]]
- [[wiki/synthesis/llm-wiki-pattern]]
- [[wiki/concepts/the-ritualization-trap]]

## Sources

- [[learning/packets/david-west-object-thinking/packet]]
- [[learning/packets/david-west-object-thinking/human-contact]]
