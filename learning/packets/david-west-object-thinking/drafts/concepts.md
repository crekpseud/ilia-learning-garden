---
type: draft-concepts
packet: "[[learning/packets/david-west-object-thinking/packet]]"
status: partially-promoted
created: 2026-06-22
---

# Candidate Concepts

## Object Thinking

- Status: promoted to [[wiki/concepts/object-thinking]]
- Definition: A philosophical and behavioral approach to software development that models software as a community of autonomous, collaborating objects rather than passive data manipulated by procedures.
- Why it matters: It may become the garden's root software-design concept for behavior, responsibility, metaphor, and domain modeling.
- Possible aliases: Behavioral OOP, hermeneutic software design, object-oriented mindset
- Related existing notes: [[wiki/synthesis/digital-garden-ethos]], [[wiki/synthesis/technopastoral-synthesis]], [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: yes, pending human-contact review
- If existing, suggested patch: N/A

## Null Object Pattern

- Status: deferred
- Definition: A design pattern where absence is represented by an object with neutral or default behavior instead of by a NULL reference.
- Why it matters: It is a concrete pressure point where Object Thinking challenges procedural null checks and preserves polymorphic message-sending.
- Possible aliases: Active Nothing, stub object, null object
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: maybe
- If existing, suggested patch: N/A

## Software-as-Theater Metaphor

- Status: promoted to [[wiki/concepts/software-as-theater-metaphor]]
- Definition: A metaphor where objects are actors with talents, applications provide roles and scripts, and the environment acts as a stage.
- Why it matters: It helps separate an object's intrinsic capabilities from its situational role in a particular application.
- Possible aliases: Actor metaphor, dramaturgical software design, All the World's a Stage
- Related existing notes: [[wiki/synthesis/digital-garden-ethos]], [[wiki/concepts/digital-garden]]
- Promotion recommendation: yes, pending human-contact review
- If existing, suggested patch: N/A

## Self-Evaluating Rule

- Status: promoted to [[wiki/concepts/self-evaluating-rule]]
- Definition: A rule represented as a first-class object capable of evaluating, modifying, or participating in behavior rather than being hard-coded into a controller or object method.
- Why it matters: It tests the Object Thinking claim that even rules can be objects, not merely external constraints.
- Possible aliases: Executable rule, first-class rule, first-class constraint
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: maybe
- If existing, suggested patch: N/A

## Formalism vs Hermeneutics

- Status: deferred
- Definition: A contrast between tools-led, formal, machine-like software engineering and people-led, interpretive, domain-centered software development.
- Why it matters: It names the philosophical split behind many disagreements about Object Thinking.
- Possible aliases: formalist versus hermeneutic software design, scientific management versus interpretation
- Related existing notes: [[wiki/synthesis/technopastoral-synthesis]], [[wiki/synthesis/digital-garden-ethos]]
- Promotion recommendation: maybe
- If existing, suggested patch: N/A

## Procedural Habit

- Status: new candidate
- Definition: A programming habit that preserves procedural control flow or data manipulation inside code that appears object-oriented.
- Why it matters: It may help describe the practical failure mode Object Thinking critiques, including null checks, managers, and data-centric objects.
- Possible aliases: procedural thinking, procedural residue, procedural inheritance
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: not yet
- If existing, suggested patch: N/A

## Option/Maybe Pattern

- Status: promoted to [[wiki/concepts/option-maybe-pattern]]
- Definition: A way to represent absence or possible failure as an explicit value, often through Option, Maybe, Result, nullable-aware APIs, or related monadic patterns.
- Why it matters: The user's reflection challenges a direct Null Object promotion by asking whether modern C#/.NET practice is better served by Option/Maybe-style absence handling, nullable reference types, or fail-fast exceptions.
- Possible aliases: Option type, Maybe type, optional value, Result type
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: maybe, but only after comparing it with Null Object in a C#/.NET-focused packet
- If existing, suggested patch: N/A

## Actor Model

- Status: user-originated future candidate
- Definition: A concurrency and system-design model where autonomous actors communicate by passing messages and encapsulate their own state and behavior.
- Why it matters: The user's reflection connects Object Thinking's distribution of responsibilities to autonomous actors and even intelligent agents.
- Possible aliases: message-passing actors, autonomous actors
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]], [[wiki/synthesis/digital-garden-ethos]]
- Promotion recommendation: not yet; better as a future learning packet
- If existing, suggested patch: N/A
