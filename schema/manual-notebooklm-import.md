# Manual NotebookLM Import

Manual NotebookLM import is a first-class experimental bridge. It lets the user copy NotebookLM source manifests or packet exports into the vault before any Google Docs or Drive automation exists.

Prepared context slices and other NotebookLM inputs belong in `learning/bridge/notebooklm/`. Imported NotebookLM outputs belong in `learning/inbox/notebooklm/`.

The preferred mode is Source-Manifest-First: NotebookLM provides source provenance and learning media, while the local agent creates the garden-aware packet after checking relevant sources against the whole vault.

Direct copy-paste from NotebookLM is currently the preferred manual transport mode because it preserves literal Markdown heading markers better than Google Docs export.

## Source Manifest Location

Paste a source manifest into:

```text
learning/inbox/notebooklm/<slug>/source-manifest.md
```

The source manifest is preserved as the source-facing NotebookLM output. It is not edited during local packet creation.

## Packet Export Location

Paste the external export into:

```text
learning/inbox/notebooklm/<slug>/packet-export.md
```

The packet export file is preserved as the source export. It is not edited during normalization.

## Preferred Flow: Source Manifest First

1. The user shares a NotebookLM screenshot, notebook title, or notebook summary.
2. The local agent prepares a short NotebookLM source-manifest prompt.
3. The user asks NotebookLM for a Source Manifest and optionally generates podcast, quiz, or flashcards.
4. The user pastes the Source Manifest into `learning/inbox/notebooklm/<slug>/source-manifest.md` or gives it to the agent to preserve.
5. The local agent performs a Codex Source Pass over the relevant public or provided sources.
6. The local agent creates the learning packet directly from the source manifest, source pass, whole-garden context, and any human-contact artifact.
7. The local agent runs local reconciliation, concept recognition, suggested patches, and gardening review.
8. The packet remains pending human contact until the human-contact gate is complete.
9. Promotion happens only after explicit review and approval.

## Full Packet Export Fallback

Use a full NotebookLM Packet Export only when NotebookLM has a meaningful source advantage:

- the notebook contains YouTube videos and NotebookLM has useful transcripts
- the notebook contains private Google Drive files the local agent cannot access
- the notebook contains uploaded audio, images, PDFs, or other files that NotebookLM can parse more easily
- the source set is large enough that NotebookLM's source organization is valuable
- the Codex Source Pass finds that NotebookLM captured important cross-source structure that should be reflected in the packet
- the user explicitly wants NotebookLM's learning-guide, podcast, or quiz framing reflected in the packet draft

When fallback is used, preserve the packet export and classify it by import quality.

## Packet Export Flow

1. Copy the NotebookLM answer directly and paste it into the inbox path.
2. Validate the export against [[packet-export-contract]].
3. Assign an import quality tier.
4. Preserve a source record in `raw/sources/`.
5. Normalize the export into `learning/packets/<slug>/` only if the tier is `strict-valid` or `repairable`.
6. Run local reconciliation against the current vault.
7. Run a gardening review using [[schema/gardening-review]].
8. Mark the packet pending human contact if the export lacks a valid human-contact artifact.
9. Promote only after explicit review and approval.

## Import Quality Tiers

NotebookLM can understand the contract and still produce output that fails strict structural compliance. Treat the output as advisory synthesis, not authoritative schema.

Assign one of these tiers after validation:

**strict-valid**:
The export satisfies [[packet-export-contract]] exactly enough to normalize directly. Preserve the raw inbox export and proceed with local reconciliation.

**repairable**:
The export fails strict validation, but satisfies the minimum repairability contract in [[packet-export-contract]]. Preserve the raw inbox export, create `artifacts/import-repair.md`, document the contract failures, then normalize locally.

**rejected**:
The export lacks enough structure or substance for safe repair. Preserve the raw export if useful for diagnosis, but do not normalize it into packet drafts. Ask NotebookLM for explicit repair or rerun the packet export prompt.

## Local Reconciliation

NotebookLM knows the notebook sources, but it does not know the current vault unless context was supplied in the prompt. Its output is advisory.

During reconciliation, the local agent should:

- recognize existing trusted concepts and avoid duplicate concept promotion
- turn references to existing concepts into suggested patches when needed
- keep new concepts as candidates until approved
- de-duplicate sources and flag placeholder or unknown URLs
- preserve the original export separately from normalized artifacts
- document any contract failures and repairs in `artifacts/import-repair.md`
- create or update `artifacts/gardening-review.md`
- record missing human contact as a promotion blocker

## Why This Exists

Manual import keeps the bridge small while the protocol is still changing. It gives us real learning loops and real packet artifacts before committing to sync automation.

Later bridges, including Google Docs or Drive-based import, should preserve the same provenance artifacts, produce the same packet artifacts, and use the same reconciliation step.
