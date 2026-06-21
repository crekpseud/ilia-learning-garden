# Manual NotebookLM Import

Manual NotebookLM import is a first-class experimental bridge. It lets the user copy a NotebookLM packet export into the vault before any Google Docs or Drive automation exists.

## Inbox Location

Paste the external export into:

```text
learning/inbox/notebooklm/<slug>/packet-export.md
```

The inbox file is preserved as the source export. It is not edited during normalization.

## Flow

1. Paste the NotebookLM export into the inbox path.
2. Validate the export against [[packet-export-contract]].
3. Preserve a source record in `raw/sources/`.
4. Normalize the export into `learning/packets/<slug>/`.
5. Run local reconciliation against the current vault.
6. Mark the packet pending human contact if the export lacks a valid human-contact artifact.
7. Promote only after explicit review and approval.

## Local Reconciliation

NotebookLM knows the notebook sources, but it does not know the current vault unless context was supplied in the prompt. Its output is advisory.

During reconciliation, the local agent should:

- recognize existing trusted concepts and avoid duplicate concept promotion
- turn references to existing concepts into suggested patches when needed
- keep new concepts as candidates until approved
- de-duplicate sources and flag placeholder or unknown URLs
- preserve the original export separately from normalized artifacts
- record missing human contact as a promotion blocker

## Why This Exists

Manual import keeps the bridge small while the protocol is still changing. It gives us real learning loops and real packet artifacts before committing to sync automation.

Later bridges, including Google Docs or Drive-based import, should produce the same packet artifacts and use the same reconciliation step.