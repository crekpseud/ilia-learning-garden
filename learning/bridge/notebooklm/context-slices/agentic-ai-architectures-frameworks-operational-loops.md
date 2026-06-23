GARDEN_META_SOURCE_ID: vault-context-slice:agentic-ai-architectures-frameworks-operational-loops
GARDEN_META_SOURCE_KIND: vault-context-slice
GARDEN_META_SOURCE_TITLE: Vault Context Slice - Agentic AI Architectures Frameworks Operational Loops

# Vault Context Slice - Agentic AI Architectures Frameworks Operational Loops

## Protocol Summary

- Markdown is the durable protocol.
- The vault is read topographically through links, concepts, maps, and synthesis notes.
- Workflow history is append-only in logs, packet reviews, and Git.
- Trusted notes change through reviewed patches, not silent rewrites.
- Candidate concepts are suggestions only. Concept promotion requires human approval.
- A packet normally promotes one synthesis note by default, plus zero or more approved reusable concept notes.
- The external LLM produces advisory packet output only. Local reconciliation, review, and promotion happen later.
- The human-contact gate is essential: knowledge must pass through the learner's own attention before it enters the trusted wiki.

## Existing Trusted Notes And Concepts

- [[wiki/synthesis/llm-wiki-pattern|LLM Wiki Pattern]] - Persistent Markdown wiki pattern where LLMs maintain a compounding synthesis layer between raw sources and future queries. This is the closest existing trusted note to agentic AI because it frames an LLM as a maintainer of durable Markdown artifacts, not just a responder.

- [[wiki/synthesis/object-thinking-and-the-digital-garden|Object Thinking And The Digital Garden]] - Software-design synthesis connecting Object Thinking, metaphor, responsibility, and garden-like systems. This may help compare agents, objects, actors, tools, and responsibilities.

- [[wiki/concepts/object-thinking|Object Thinking]] - Software-design lens that models systems as communities of collaborating behavioral objects rather than passive data manipulated by procedures.

- [[wiki/concepts/self-evaluating-rule|Self-Evaluating Rule]] - Rule modeled as a first-class behavioral object rather than controller logic. This may connect to agentic guardrails, policies, feedback mechanisms, and autonomous loop constraints.

- [[wiki/concepts/note-titles-as-apis|Note Titles as APIs]] - Naming practice where note titles become stable handles for humans, links, and agents. This may connect to agent memory, tool calls, and durable knowledge interfaces.

- [[wiki/concepts/the-ritualization-trap|The Ritualization Trap]] - Failure mode where a knowledge practice becomes self-optimizing maintenance instead of learning. This may connect to infinite loops, automation theater, and overbuilt agent workflows.

- [[wiki/concepts/digital-garden|Digital Garden]] - Personal knowledge space where notes are linked, evolving, contextual, and owned by the author.

## Current Protocol Decisions Relevant To This Packet

- [[docs/adr/0018-use-topic-specific-vault-context-slices|Use topic-specific vault context slices]] - Supply only relevant current vault context to external LLMs.
- [[docs/adr/0019-reconcile-external-packet-exports-locally|Reconcile external packet exports locally]] - Treat NotebookLM output as advisory until local validation and reconciliation.
- [[docs/adr/0023-classify-external-packet-exports-by-import-quality|Classify external packet exports by import quality]] - Classify the output as strict-valid, repairable, or rejected before normalization.
- [[docs/adr/0024-use-embedded-meta-source-ids-for-notebooklm-copy-text|Use embedded meta-source IDs for NotebookLM copy-text sources]] - Identify copied meta-sources by `GARDEN_META_SOURCE_ID`, not by NotebookLM filename.
- [[docs/adr/0025-require-active-gardening-review|Require active gardening review]] - The local agent should ask what each packet means for the whole garden.
- [[docs/adr/0029-use-notebooklm-packet-export-as-default-source-heavy-bridge|Use NotebookLM packet export as default source-heavy bridge]] - Let NotebookLM digest source-heavy notebooks; local agents validate, reconcile, and garden.

## Deferred Candidate Concepts

These are not trusted notes yet. Do not use wikilinks for them.

- Active Reconstruction - Rebuilding understanding through output-side practices such as summarizing from memory, self-testing, synthesis, and explanation.
- Cognitive Offloading - Delegating mental work to an external tool or environment; useful as scaffolding, risky as substitution.
- Desirable Difficulties - Learning conditions that slow short-term performance but improve long-term retention, retrieval, and transfer.
- First-Principles Reasoning - A reasoning practice that breaks complex problems into fundamental truths and rebuilds solutions from those foundations.
- Agentic Loop - A repeated observe-plan-act-evaluate cycle where an AI system uses tools and feedback to move toward a goal.
- Tool Use - The ability of an AI system to call external capabilities rather than only emit text.
- Agent Memory - Durable or session-level context an agent uses to carry state across steps.
- Loop Engineering - Designing, bounding, observing, and correcting autonomous or semi-autonomous AI loops.
- Human Oversight Boundary - The line between useful autonomy and work that must return to human review.
- Prompt Injection Risk - The risk that tool-accessible or source-provided text manipulates the agent away from the user's intent or protocol.

If recommending promotion, keep new agentic-AI concepts as new candidates. Use `NEW CANDIDATE: <title>` outside the concept heading instead of a wikilink.

## Topic Guidance

This packet should explore agentic AI as architectures, frameworks, and operational loops.

Focus on:

- the shift from static chatbots to agentic systems that use autonomous or semi-autonomous loops
- core architecture elements such as planning, reasoning, memory, tools, feedback, and execution
- orchestration frameworks such as LangChain, CrewAI, Claude Agent SDK, and other source-mentioned systems
- ReAct, reflection, planning patterns, feedback mechanisms, and loop engineering
- token costs, latency, infinite loops, prompt injection, tool misuse, security boundaries, and observability
- where agentic AI helps software engineering and where it creates operational or cognitive risk
- what this teaches the learning garden about Codex as a local automation agent and NotebookLM as a source-heavy synthesis server
- whether "agent" should become a trusted concept, or whether more precise concepts such as Agentic Loop, Tool Use, Agent Memory, Loop Engineering, or Human Oversight Boundary are better handles

Pay special attention to tensions:

- When does an agentic loop create real leverage, and when does it become automation theater?
- How should autonomous loops be bounded so they do not drift, loop indefinitely, or silently corrupt trusted knowledge?
- How does agent memory differ from a persistent Markdown wiki?
- How do tool calls change the trust boundary compared with ordinary chat completion?
- How should a Markdown-first garden record agent actions so they remain reviewable?

## Human-Contact Artifact

MISSING: human-contact artifact required before promotion.
