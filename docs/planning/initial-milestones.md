# Initial Milestones

## Milestone 1: Protocol-Only Proof

Prove the Markdown protocol manually with Codex as the first automation agent.

Target flow:

```text
create one sample learning packet
-> draft one synthesis note
-> review it
-> promote it
-> update index and log
```

Success means the packet anatomy, packet export contract, templates, review file, trusted wiki structure, index, and log are coherent before any bridge implementation exists.

## Milestone 2: End-to-End Thin Slice

Build the smallest automated path through the protocol.

Target flow:

```text
Google Doc packet export
-> import
-> normalize into learning packet
-> draft trusted wiki output
-> review
-> promote one synthesis note
```

Success means the first Google Docs bridge works against a known-good packet export without changing the core Markdown protocol.

## Deferred

- Drive folder watching or batch imports.
- NotebookLM UI automation.
- CLI syntax and packaging.
- Rich UI or Obsidian plugin.
- Automatic edits to existing trusted notes.

