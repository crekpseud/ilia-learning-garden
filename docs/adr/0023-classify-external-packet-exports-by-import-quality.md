# Classify external packet exports by import quality

External packet exports will be classified as `strict-valid`, `repairable`, or `rejected` before normalization.

**Context**

NotebookLM can detect the packet contract and vault context during preflight, but still produce an answer that renames required headings, omits required sections, or repeats context-slice concepts as if they were new output.

This means source-grounded LLMs are useful synthesis engines, but not reliable schema emitters. The garden should preserve their raw output and let the local protocol decide whether it can be normalized.

**Considered Options**

- Keep tightening prompts until external exports are always valid.
- Reject every malformed export.
- Best-effort normalize malformed exports silently.
- Classify exports by import quality and require explicit repair records for malformed-but-useful output.

**Decision**

Use import quality tiers:

- `strict-valid`: normalize directly after preserving the raw export.
- `repairable`: preserve the raw export, document contract failures in `artifacts/import-repair.md`, then normalize locally.
- `rejected`: preserve only for diagnosis if useful, and ask for repair or rerun instead of creating packet drafts.

**Consequences**

NotebookLM and similar tools remain replaceable bridge inputs, not protocol authorities. The vault can benefit from useful synthesis even when formatting fails, while preserving a clear audit trail of what was repaired locally.

Future tools should automate this classification and generate the repair record, but they should not silently turn malformed external output into trusted packet state.
