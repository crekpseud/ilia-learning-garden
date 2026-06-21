---
type: human-contact
packet: "[[learning/packets/knowledge-gardening/packet]]"
status: accepted
contact_types:
  - notebooklm-podcast
  - draft-review
  - protocol-reflection
created: 2026-06-21
---

# Human Contact

This packet was imported from a NotebookLM packet export. At import time it was not ready for promotion; the reflection below later satisfied the human-contact gate.

## Packet Export Status

The original export contained a missing-human-contact marker. That original marker is preserved in [[learning/inbox/notebooklm/knowledge-gardening/packet-export]]; this file records the later accepted contact artifact.

## Reflection Prompt

Answer this before promotion:

```text
What did this NotebookLM synthesis teach or change about your understanding of knowledge gardening, especially compared with the already-promoted Digital Garden concept?
```

## Reflection

The user made the earlier digital garden notes in one continuous learning stretch: first reading Maggie Appleton's article, then listening to a NotebookLM-generated podcast while cooking. For this packet, the user also read [[learning/packets/knowledge-gardening/drafts/synthesis]].

The main idea of this loop was to feel how NotebookLM could be gently brought into the picture. The workflow feels promising so far. The user is comfortable deferring synchronization and trying a few more manual copy-paste rounds before automating the bridge.

The main concern is how to provide vault context to an external LLM like NotebookLM. Prompting with context is useful, but the whole vault should not be pasted into every prompt, especially as it grows. Too much context may be harmful for learning a specific topic. The better direction is to provide only context related to the topic at hand.

## Design Implications

- Manual NotebookLM copy-paste remains acceptable for a few more experiments.
- Google Docs synchronization can be deferred until the packet export workflow stabilizes.
- Prompt templates need a way to inject a topic-specific slice of vault context.
- More context is not always better; context should be relevant to the current learning material.
