# Use source-manifest-first NotebookLM bridge

NotebookLM should usually produce a compact source manifest, not a full learning packet. Codex should then inspect the relevant sources and create the garden-aware packet locally, using the whole vault for reconciliation, linking, candidate concepts, suggested patches, and gardening review.

**Context**

NotebookLM is valuable as a source workspace, source search helper, YouTube transcript importer, podcast generator, and quiz/flashcard generator. But recent packet experiments showed that full NotebookLM packet exports often need local repair, and NotebookLM only knows the vault slice that was supplied to it.

Codex knows the whole garden and can optimize packet creation against current trusted notes, deferred candidates, protocol decisions, logs, and promotion rules.

**Considered Options**

- Keep asking NotebookLM for full packet exports by default.
- Stop using NotebookLM except for podcasts.
- Use NotebookLM for source manifests and learning media by default, with full packet export as fallback.

**Decision**

Adopt Source-Manifest-First NotebookLM Bridge as the preferred flow:

```text
notebook screenshot -> Codex prompt -> NotebookLM source manifest -> Codex source pass -> garden-aware packet
```

Use Full NotebookLM Packet Fallback only when NotebookLM has a meaningful source advantage, such as YouTube transcripts, private Drive files, uploaded audio, uploaded PDFs/images, a very large source set, or source organization that Codex cannot reproduce locally.

**Consequences**

This reduces prompt ceremony and malformed packet repair while preserving NotebookLM's strongest value in the user's learning loop: source gathering, audio overviews, quizzes, and transcript-backed exploration.

The local agent remains responsible for source checking, reconciliation, packet drafting, and promotion boundaries. NotebookLM remains a replaceable bridge input, not a trusted wiki authority.
