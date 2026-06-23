# NotebookLM Run Prompt - Agentic AI Architectures Frameworks Operational Loops

Paste this into the NotebookLM chat after adding:

- a source containing `GARDEN_META_SOURCE_ID: learning-packet-export-contract`
- a source containing `GARDEN_META_SOURCE_ID: vault-context-slice:agentic-ai-architectures-frameworks-operational-loops`
- the notebook's learning sources

```markdown
Create a Learning Packet Export in Markdown.

Before generating, silently check whether you can access the required garden meta-sources by content marker, not by NotebookLM filename.

Required markers:
- GARDEN_META_SOURCE_ID: learning-packet-export-contract
- GARDEN_META_SOURCE_ID: vault-context-slice:agentic-ai-architectures-frameworks-operational-loops

If either marker is missing, do not create the packet. Return only:

# Packet Export Preflight

## Meta-Sources Detected

- FOUND or MISSING: learning-packet-export-contract
- FOUND or MISSING: vault-context-slice:agentic-ai-architectures-frameworks-operational-loops

## Readiness

NOT READY: One or more required meta-sources are missing.

If both markers are found, do not include the preflight in your answer. Continue and generate the packet export only.

Use the source containing "GARDEN_META_SOURCE_ID: learning-packet-export-contract" as the required output contract.
Use the source containing "GARDEN_META_SOURCE_ID: vault-context-slice:agentic-ai-architectures-frameworks-operational-loops" as vault context.
Use the remaining notebook sources as the learning material.

Topic: Agentic AI: Architectures, Frameworks, and Operational Loops

Focus on:
- the shift from static chatbots to agentic AI systems that use autonomous or semi-autonomous loops
- core architecture elements such as planning, reasoning, memory management, tool use, feedback, and execution
- orchestration frameworks and SDKs mentioned in the sources, including LangChain, CrewAI, Claude Agent SDK, and comparable systems
- ReAct, reflection, planning patterns, feedback mechanisms, and loop engineering
- token costs, latency, infinite loops, prompt injection, tool misuse, security boundaries, and observability
- what this packet should teach a Markdown-first learning garden about Codex as a local automation agent, NotebookLM as a source-heavy synthesis server, and the need for human oversight boundaries

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list the garden meta-sources as learning sources in the Source List.
Do not create wikilinks for suggested new synthesis notes or new candidate concepts.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```
