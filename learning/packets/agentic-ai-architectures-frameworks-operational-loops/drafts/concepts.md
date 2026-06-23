---
type: draft-concepts
packet: "[[learning/packets/agentic-ai-architectures-frameworks-operational-loops/packet]]"
status: pending-human-contact
created: 2026-06-23
---

# Candidate Concepts

## Agentic Loop

- Status: new candidate
- Definition: A repeating observe-plan-act-evaluate cycle where an AI system uses tools and feedback to move toward a goal.
- Why it matters: It names the architectural element that separates agentic systems from ordinary chatbots and single-pass completions.
- Possible aliases: operational loop, agent loop, iteration loop, observe-plan-act loop
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]], [[wiki/concepts/self-evaluating-rule]], [[wiki/concepts/digital-garden]]
- Promotion recommendation: yes, pending human-contact review
- If existing, suggested patch: N/A

## Loop Engineering

- Status: new candidate
- Definition: The design practice of building, bounding, observing, and correcting autonomous or semi-autonomous AI loops.
- Why it matters: It shifts attention from crafting one prompt to designing triggers, tool access, stop conditions, feedback paths, and repair mechanisms.
- Possible aliases: flow engineering, agent loop design, operational loop design
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]], [[wiki/concepts/the-ritualization-trap]], [[wiki/concepts/desirable-difficulties]]
- Promotion recommendation: yes, pending human-contact review
- If existing, suggested patch: N/A

## Tool Use

- Status: new candidate
- Definition: The ability of an AI system to call external capabilities such as APIs, code execution, search, files, or domain tools rather than only emit text.
- Why it matters: Tool use changes the trust boundary because the model's output can affect external state.
- Possible aliases: function calling, tool calling, external action
- Related existing notes: [[wiki/concepts/object-thinking]], [[wiki/concepts/self-evaluating-rule]]
- Promotion recommendation: maybe
- If existing, suggested patch: N/A

## Agent Memory

- Status: new candidate
- Definition: The durable or session-level context an agent uses to carry state across turns, steps, or tasks.
- Why it matters: It helps distinguish short-term context windows, vector memory, knowledge graphs, logs, and this garden's Markdown wiki as possible memory substrates.
- Possible aliases: agent context, long-term agent memory, working memory
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]], [[wiki/concepts/note-titles-as-apis]], [[wiki/concepts/digital-garden]]
- Promotion recommendation: maybe
- If existing, suggested patch: N/A

## Human Oversight Boundary

- Status: new candidate
- Definition: The threshold, failure condition, or policy boundary where an autonomous loop must pause and request human review or approval.
- Why it matters: It names the control surface that prevents useful autonomy from becoming silent drift, security risk, runaway cost, or trusted-wiki corruption.
- Possible aliases: human-in-the-loop, approval boundary, review boundary, escalation boundary
- Related existing notes: [[CONTEXT|Human-Contact Gate]], [[wiki/concepts/the-ritualization-trap]], [[wiki/synthesis/original-thought-as-active-reconstruction]]
- Promotion recommendation: yes, pending human-contact review
- If existing, suggested patch: N/A

## Prompt Injection Risk

- Status: new candidate
- Definition: The risk that text encountered through tools, sources, websites, or documents manipulates an agent away from the user's intent, policy, or protocol.
- Why it matters: It becomes sharper in agentic systems because the model may act on malicious instructions through tools or repeated loops.
- Possible aliases: tool-context injection, instruction injection, poisoned context
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]]
- Promotion recommendation: maybe, likely after a dedicated security packet
- If existing, suggested patch: N/A

## Model Context Protocol

- Status: new candidate
- Definition: A protocol for connecting AI systems to tools and data sources through standardized context and tool interfaces.
- Why it matters: The export frames MCP as a standardization layer for agent tool access, but this garden should verify details before promotion.
- Possible aliases: MCP
- Related existing notes: [[wiki/synthesis/llm-wiki-pattern]], [[wiki/concepts/note-titles-as-apis]]
- Promotion recommendation: not yet
- If existing, suggested patch: N/A

## Reconciliation Notes

The raw export recommended `Agentic Loop`, `Loop Engineering`, and `Human Oversight Boundary` most strongly. Local reconciliation keeps `Tool Use` and `Agent Memory` as candidate concepts but does not recommend automatic promotion before human contact.

The numeric claims around 15x-200x token costs and 60% production failures are retained as source claims, not promoted facts.
