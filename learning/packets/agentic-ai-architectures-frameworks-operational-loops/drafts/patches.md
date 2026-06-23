---
type: suggested-patches
packet: "[[learning/packets/agentic-ai-architectures-frameworks-operational-loops/packet]]"
status: pending-human-contact
created: 2026-06-23
---

# Suggested Patches

## Patch: [[wiki/synthesis/llm-wiki-pattern]]

Rationale:
This packet adds an operational layer to the LLM Wiki Pattern: a wiki-maintaining LLM is not just a responder, but can become an agent that acts through bounded loops.

Suggested addition:

```markdown
When an LLM maintains a wiki through tools, the system should be understood as an agentic loop rather than a single response. The agent observes the current Markdown state, plans a change, edits files, validates links or tests, and records the outcome. That loop needs explicit boundaries: tool permissions, stop conditions, human review points, and logs that keep maintenance accountable.
```

## Patch: [[wiki/concepts/self-evaluating-rule]]

Rationale:
The packet connects self-evaluating rules to modern agent guardrails, loop termination conditions, and escalation policies.

Suggested addition:

```markdown
In agentic AI systems, guardrails and loop termination policies can be read as self-evaluating rules. They are not merely external checks; they participate in deciding whether an agent may continue, retry, call a tool, escalate to a human, or stop.
```

## Patch: [[wiki/concepts/note-titles-as-apis]]

Rationale:
The packet suggests a link between durable note titles and agent memory or tool targets.

Suggested addition:

```markdown
For agentic workflows, note titles become even more API-like because they can act as durable handles in prompts, tool calls, memory references, and maintenance logs. A title that is stable for humans is also easier for agents to retrieve and update safely.
```

## Protocol Design Questions

- Should `Human Oversight Boundary` become a protocol concept before more agent automation is built?
- Should agent actions have a dedicated log shape beyond ordinary `log.md` entries?
- Which autonomous actions are allowed in the learning area but forbidden in the trusted wiki without approval?
- Should source-heavy NotebookLM packet exports with many unknown URLs trigger a source-manifest diagnostic by default, or only when the user cares about provenance?
