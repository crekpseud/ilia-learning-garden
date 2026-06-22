# NotebookLM Run Prompt - Architecture of Original Thought

Paste this into the NotebookLM chat after adding:

- a source containing `GARDEN_META_SOURCE_ID: learning-packet-export-contract`
- a source containing `GARDEN_META_SOURCE_ID: vault-context-slice:architecture-of-original-thought`
- the notebook's learning sources

```markdown
Create a Learning Packet Export in Markdown.

Before generating, silently check whether you can access the required garden meta-sources by content marker, not by NotebookLM filename.

Required markers:
- GARDEN_META_SOURCE_ID: learning-packet-export-contract
- GARDEN_META_SOURCE_ID: vault-context-slice:architecture-of-original-thought

If either marker is missing, do not create the packet. Return only:

# Packet Export Preflight

## Meta-Sources Detected

- FOUND or MISSING: learning-packet-export-contract
- FOUND or MISSING: vault-context-slice:architecture-of-original-thought

## Readiness

NOT READY: One or more required meta-sources are missing.

If both markers are found, do not include the preflight in your answer. Continue and generate the packet export only.

Use the source containing "GARDEN_META_SOURCE_ID: learning-packet-export-contract" as the required output contract.
Use the source containing "GARDEN_META_SOURCE_ID: vault-context-slice:architecture-of-original-thought" as vault context.
Use the remaining notebook sources as the learning material.

Topic: Mastering the Architecture of Original Thought

Focus on:
- how original thought is built through active reconstruction rather than passive consumption
- Bloom's taxonomy, Adler's levels of reading, and first-principles reasoning
- desirable difficulties, testing, active recall, and spaced repetition
- the risk of outsourcing intellectual effort to AI assistants or external tools
- how this should influence the human-contact gate in a Markdown-first learning garden

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list the garden meta-sources as learning sources in the Source List.
Do not create wikilinks for suggested new synthesis notes or new candidate concepts.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```
