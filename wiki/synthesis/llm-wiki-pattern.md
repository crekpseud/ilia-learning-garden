---
type: synthesis
status: trusted
source_packet: "[[learning/packets/llm-wiki-pattern/packet]]"
created: 2026-06-21
aliases:
  - LLM Wiki
  - persistent LLM-maintained wiki
  - Markdown wiki pattern
---

# LLM Wiki Pattern

## Core Understanding

The LLM Wiki pattern uses an LLM to incrementally build and maintain a persistent Markdown wiki between raw sources and future queries. Instead of asking an LLM to rediscover knowledge from raw documents every time, the system compiles understanding into durable, interlinked notes that can be updated, searched, linted, and reused.

The important shift is from retrieval as a repeated runtime behavior to knowledge maintenance as an accumulating artifact. The wiki becomes a living synthesis layer, not just a pile of source chunks.

## Why It Matters

This pattern explains why a personal learning system should not stop at source collection or chat history. The durable value is in the maintained Markdown layer: links, summaries, contradictions, indexes, and logs that compound over time.

For this project, the pattern validates treating the vault as a Markdown codebase. Obsidian can be the IDE, Codex can be the first automation client, NotebookLM can be a synthesis server, and Google Drive can be a bridge, but the Markdown protocol remains the durable system boundary.

An LLM-maintained wiki should not optimize only for frictionless synthesis. If the system removes all cognitive effort, it can produce an illusion of competence: the learner can navigate polished notes without being able to retrieve, explain, or apply the underlying ideas. The wiki should therefore preserve human-contact artifacts that show active reconstruction.

## Key Ideas

- A persistent wiki can accumulate synthesized knowledge instead of forcing every query to reconstruct context from raw sources.
- Raw sources should remain available and immutable; the wiki is the maintained synthesis layer.
- A schema or agent instruction file makes the LLM behave like a disciplined wiki maintainer instead of a generic chatbot.
- Index and log files give both humans and LLMs navigable structure.
- Linting is a first-class maintenance operation: the system can look for contradictions, stale claims, orphan pages, missing concepts, and weak links.
- Good answers generated during query time can be filed back into the wiki so exploration compounds.

## Connections

- Supports [[docs/adr/0005-treat-markdown-as-the-codebase]].
- Supports [[docs/adr/0006-use-this-repository-as-the-seed-vault]].
- Supports [[docs/adr/0007-use-protocol-first-top-level-structure]].
- Related to [[wiki/synthesis/digital-garden-ethos]], which frames maintained linked knowledge as a personal, evolving, topographical space.
- Complements this project's [[CONTEXT|Human-Contact Gate]] by adding a trust boundary missing from the original LLM Wiki pattern.

## Questions

- How often should the wiki be linted once real learning packets accumulate?
- Which generated query answers deserve promotion into trusted notes?
- When should a synthesis note split into separate concept notes?
- How should future tools search the wiki when the index is no longer enough?

## Sources

- [[docs/research/karpathy-llm-wiki]]
- [[learning/packets/architecture-of-original-thought/packet]]
- https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
