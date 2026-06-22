GARDEN_META_SOURCE_ID: vault-context-slice:{{TOPIC_SLUG}}
GARDEN_META_SOURCE_KIND: vault-context-slice
GARDEN_META_SOURCE_TITLE: Vault Context Slice - {{TOPIC_TITLE}}

# Vault Context Slice Template

Create one copy of this text per NotebookLM packet topic and add it to NotebookLM as a copied-text source.

Replace `{{TOPIC_SLUG}}` and `{{TOPIC_TITLE}}` before using it. Prompts should identify this source by the `GARDEN_META_SOURCE_ID` marker, not by NotebookLM's generated filename.

The slice should be small. Include only context that helps NotebookLM avoid duplicate concepts, target suggested patches, and relate the notebook to the current garden.

## Protocol Summary

- Markdown is the durable protocol.
- The vault is read topographically through links, concepts, maps, and synthesis notes.
- Workflow history is append-only in logs, packet reviews, and Git.
- Trusted notes change through reviewed patches, not silent rewrites.
- Candidate concepts are suggestions only. Concept promotion requires human approval.
- A packet normally promotes one synthesis note by default, plus zero or more approved reusable concept notes.

## Existing Trusted Notes And Concepts

List only notes relevant to this packet.

Example:

- [[wiki/synthesis/llm-wiki-pattern|LLM Wiki Pattern]] - Persistent Markdown wiki pattern where LLMs maintain a compounding synthesis layer between raw sources and future queries.
- [[wiki/synthesis/digital-garden-ethos|Digital Garden Ethos]] - Human-facing metaphor for linked, evolving, personally owned knowledge spaces organized by relationships rather than chronology.
- [[wiki/concepts/digital-garden|Digital Garden]] - Personal knowledge space where notes are linked, evolving, contextual, and owned by the author. Aliases: personal knowledge garden, gardened knowledge space, digital gardening.

## Deferred Candidate Concepts

List relevant untrusted concepts as plain text, not wikilinks.

Example:

- Evergreen Note - A note constantly edited and refined to remain relevant as a reusable building block for thought.

If the external LLM recommends promoting a deferred candidate concept, it should keep the concept as `Status: new candidate` and use `NEW CANDIDATE: <title>` outside the candidate concept heading.

## Topic Guidance

State what this packet should focus on.

## Human-Contact Artifact

If the user has already produced a reflection, quiz result, correction, or teach-back, include it here.

If not, write:

```text
MISSING: human-contact artifact required before promotion.
```
