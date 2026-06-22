GARDEN_META_SOURCE_ID: vault-context-slice:david-west-object-thinking
GARDEN_META_SOURCE_KIND: vault-context-slice
GARDEN_META_SOURCE_TITLE: Vault Context Slice - David West Object Thinking

# Vault Context Slice - David West Object Thinking

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

- [[wiki/synthesis/llm-wiki-pattern|LLM Wiki Pattern]] - Persistent Markdown wiki pattern where LLMs maintain a compounding synthesis layer between raw sources and future queries.

- [[wiki/synthesis/digital-garden-ethos|Digital Garden Ethos]] - Human-facing metaphor for linked, evolving, personally owned knowledge spaces organized by relationships rather than chronology.

- [[wiki/synthesis/technopastoral-synthesis|The Technopastoral Synthesis]] - Garden/Stream framing for reclaiming topographical knowledge work from timeline-first information architecture.

- [[wiki/concepts/digital-garden|Digital Garden]] - Personal knowledge space where notes are linked, evolving, contextual, and owned by the author. Aliases: personal knowledge garden, gardened knowledge space, digital gardening.

- [[wiki/concepts/the-stream|The Stream]] - Timeline-first information architecture that serializes relationships into chronological feeds. Aliases: chronological feed, event stream, timeline-first architecture.

- [[docs/adr/0016-use-topographical-reading-with-append-only-process-history|Topographical reading with append-only process history]] - Process history is chronological and append-only, but trusted knowledge is navigated through meaning, links, and concepts.

## Current Protocol Decisions Relevant To This Packet

- [[docs/adr/0019-reconcile-external-packet-exports-locally|Reconcile external packet exports locally]] - Treat NotebookLM output as advisory until local validation and reconciliation.
- [[docs/adr/0023-classify-external-packet-exports-by-import-quality|Classify external packet exports by import quality]] - Classify the output as strict-valid, repairable, or rejected before normalization.
- [[docs/adr/0024-use-embedded-meta-source-ids-for-notebooklm-copy-text|Use embedded meta-source IDs for NotebookLM copy-text sources]] - Identify copied meta-sources by `GARDEN_META_SOURCE_ID`, not by NotebookLM filename.

## Deferred Candidate Concepts

These are not trusted notes yet. Do not use wikilinks for them.

- First-Principles Reasoning - A reasoning practice that breaks complex problems into fundamental truths and rebuilds solutions from those foundations.
- Active Reconstruction - Rebuilding understanding through output-side practices such as summarizing from memory, self-testing, synthesis, and explanation.
- The Ritualization Trap - The failure mode where knowledge practices become self-optimizing maintenance rituals that distract from thinking and learning.

No trusted software-design concept notes currently exist in this vault. Treat Object Thinking, Null Object, procedural habits, software metaphor, and technical pragmatism as candidate territory unless the notebook sources justify more precise concepts.

If recommending promotion, keep new software-design concepts as new candidates. Use `NEW CANDIDATE: <title>` outside the concept heading instead of a wikilink.

## Topic Guidance

This packet should explore David West's Object Thinking and its practical tension with day-to-day software engineering.

Focus on:

- What David West means by Object Thinking as a philosophical and behavioral approach to software development.
- How Object Thinking differs from class-first, data-structure-first, procedural, or code-example-driven views of object-oriented programming.
- The role of metaphor and abstract conceptualization in software design.
- The critique of procedural habits, especially around null references, null objects, exceptions, and behavioral objects.
- The tension between philosophical depth and ruthless technical pragmatism.
- Whether Object Thinking can help modern developers reason better about models, boundaries, responsibility, behavior, and collaboration.
- Where Object Thinking risks becoming too abstract, postmodern, or hard to translate into real implementation guidance.
- How this topic connects to this garden's interest in knowledge, metaphor, living systems, and software as something that grows.

Pay special attention to tensions:

- When does metaphor deepen software design, and when does it obscure implementation reality?
- When does procedural pragmatism protect delivery, and when does it flatten the domain model?
- Is Null Object a deep modeling move, a tactical pattern, or a workaround for language/tool limitations?
- Which ideas should become durable concepts in this garden, and which should stay as source-specific observations?

## Human-Contact Artifact

MISSING: human-contact artifact required before promotion.
