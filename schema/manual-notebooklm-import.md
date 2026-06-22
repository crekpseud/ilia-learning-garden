# Manual NotebookLM Import

Manual NotebookLM import is a first-class experimental bridge. It lets the user copy a NotebookLM packet export into the vault before any Google Docs or Drive automation exists.

Prepared context slices and other NotebookLM inputs belong in `learning/bridge/notebooklm/`. Imported NotebookLM outputs belong in `learning/inbox/notebooklm/`.

Direct copy-paste from NotebookLM is currently the preferred manual import mode because it preserves literal Markdown heading markers better than Google Docs export.

## Inbox Location

Paste the external export into:

```text
learning/inbox/notebooklm/<slug>/packet-export.md
```

The inbox file is preserved as the source export. It is not edited during normalization.

## Flow

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

Later bridges, including Google Docs or Drive-based import, should produce the same packet artifacts and use the same reconciliation step.
