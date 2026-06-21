---
type: human-contact
packet: "[[learning/packets/llm-wiki-pattern/packet]]"
status: accepted
contact_types:
  - discussion
  - reflection
  - architecture-decision
created: 2026-06-21
---

# Human Contact

The user brought Karpathy's LLM Wiki article into the design conversation because it touched the core of the intended system: persistent, compounding Markdown knowledge maintained with LLM help.

During the grilling session, the user discussed and approved several architecture decisions derived from or sharpened by the article:

- Markdown should be the durable protocol and codebase.
- Obsidian is the first IDE, but not the product boundary.
- Codex is the first local automation client, but not required by the protocol.
- NotebookLM is a replaceable remote synthesis engine.
- Google Drive is a replaceable bridge.
- This repository should become the seed vault.
- The trusted wiki should receive reviewed knowledge through promotion, not raw generated output.

This packet therefore uses a conversation-derived human-contact artifact: the material was not only read or imported, but actively reflected into project decisions.

