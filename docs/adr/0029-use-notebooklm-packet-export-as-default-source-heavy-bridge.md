# Use NotebookLM packet export as default source-heavy bridge

NotebookLM should produce a full Packet Export by default for source-heavy notebooks after receiving the packet export contract, a topic-specific vault context slice, and a short run prompt. The local garden agent should validate, repair, reconcile, and garden the export instead of trying to reproduce NotebookLM's source digestion.

This supersedes [[0028-use-source-manifest-first-notebooklm-bridge]] as the default flow. Source Manifest remains available as a diagnostic and provenance audit tool.

**Context**

The Source-Manifest-First experiment improved provenance awareness and made weak URLs visible. It also exposed a trade-off: asking the local agent to create the packet from a manifest shifts too much heavy source digestion away from NotebookLM.

NotebookLM can ingest and synthesize large PDFs, books, YouTube transcripts, uploaded files, private Drive material, and large mixed source sets. That is a real bridge advantage. The user explicitly does not want the local agent to do that heavy lifting when NotebookLM is already the source workspace and podcast generator.

At the same time, NotebookLM still does not know the whole vault, cannot promote trusted notes, and may produce malformed packet exports. The local protocol remains responsible for validation, import quality classification, local reconciliation, gardening review, human-contact gates, and promotion boundaries.

**Considered Options**

- Keep Source-Manifest-First as the default and ask the local agent to draft packets from source manifests.
- Use NotebookLM only for podcasts and quizzes, while Codex creates all packet material from sources.
- Return to full NotebookLM packet exports by default, with Source Manifest as a diagnostic tool.

**Decision**

Use NotebookLM Packet Export Bridge as the default for source-heavy notebooks:

```text
notebook screenshot -> local agent prepares three texts -> NotebookLM packet export -> local validation and reconciliation -> human contact -> promotion review
```

The three texts are:

- `learning-packet-export-contract`
- a topic-specific `vault-context-slice`
- a short `notebooklm-run-prompt`

Use Source Manifest only when provenance or quality needs investigation:

- source URLs are unknown, weak, duplicated, or suspicious
- sources are access blockers or login walls
- the packet export is too malformed to trust or repair cleanly
- the local agent needs source clues for targeted checking
- the user explicitly asks whether Codex can create the packet locally

**Consequences**

NotebookLM keeps the source-heavy work it is good at. The local agent keeps the garden-heavy work it is good at: validation, import repair, concept recognition, link reconciliation, suggested patches, gardening review, and promotion boundaries.

This restores the original low-friction learning loop while preserving the useful lesson from the source-manifest experiment: provenance problems should become visible through a diagnostic Source Manifest, not hidden inside local repair.
