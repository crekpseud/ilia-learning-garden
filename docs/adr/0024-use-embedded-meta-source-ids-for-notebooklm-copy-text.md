# Use embedded meta-source IDs for NotebookLM copy-text sources

NotebookLM copy-text sources will identify themselves with `GARDEN_META_SOURCE_ID` marker lines. Run prompts will refer to those markers instead of NotebookLM-generated filenames.

**Context**

Adding the packet export contract and vault context slice as copied text is often more convenient than uploading files. In that mode, NotebookLM may generate its own source filenames, so filename-based prompts are brittle.

The protocol needs a stable way to tell NotebookLM which copied text is the packet export contract and which copied text is the vault context slice.

**Considered Options**

- Keep using NotebookLM-generated filenames.
- Ask the user to manually rename copied-text sources.
- Use uploaded files only.
- Embed stable source identity markers inside the copied text.

**Decision**

Use embedded Garden Meta-Source IDs:

```markdown
GARDEN_META_SOURCE_ID: learning-packet-export-contract
```

and:

```markdown
GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>
```

When preparing a NotebookLM packet from a screenshot or notebook text, provide three copyable texts:

- `learning-packet-export-contract`
- `vault-context-slice`
- `prompt`

The prompt must check for the required Garden Meta-Source IDs. If either is missing, it should return a `NOT READY` preflight response instead of generating a packet. If both are found, it should generate only the packet export.

**Consequences**

NotebookLM filenames become irrelevant. The copy-text workflow stays convenient while the local protocol can still require explicit context awareness before generation.

This does not make NotebookLM a schema authority. Imported exports are still classified by import quality and reconciled locally before promotion.
