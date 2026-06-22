# NotebookLM Run Prompt

Use this short chat prompt after adding these NotebookLM copied-text sources:

- a source containing `GARDEN_META_SOURCE_ID: learning-packet-export-contract`
- a source containing `GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>`
- the actual learning sources for the topic

```markdown
Create a Learning Packet Export in Markdown.

Before generating, silently check whether you can access the required garden meta-sources by content marker, not by NotebookLM filename.

Required markers:
- GARDEN_META_SOURCE_ID: learning-packet-export-contract
- GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>

If either marker is missing, do not create the packet. Return only:

# Packet Export Preflight

## Meta-Sources Detected

- FOUND or MISSING: learning-packet-export-contract
- FOUND or MISSING: vault-context-slice:<topic-slug>

## Readiness

NOT READY: One or more required meta-sources are missing.

If both markers are found, do not include the preflight in your answer. Continue and generate the packet export only.

Use the source containing "GARDEN_META_SOURCE_ID: learning-packet-export-contract" as the required output contract.
Use the source containing "GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>" as vault context.
Use the remaining notebook sources as the learning material.

Topic: <Topic Title>

Focus on:
- <focus point 1>
- <focus point 2>
- <focus point 3>

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list the garden meta-sources as learning sources in the Source List.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```

## Evergreen Notes Example

```markdown
Create a Learning Packet Export in Markdown.

Before generating, silently check whether you can access the required garden meta-sources by content marker, not by NotebookLM filename.

Required markers:
- GARDEN_META_SOURCE_ID: learning-packet-export-contract
- GARDEN_META_SOURCE_ID: vault-context-slice:evergreen-notes

If either marker is missing, do not create the packet. Return only:

# Packet Export Preflight

## Meta-Sources Detected

- FOUND or MISSING: learning-packet-export-contract
- FOUND or MISSING: vault-context-slice:evergreen-notes

## Readiness

NOT READY: One or more required meta-sources are missing.

If both markers are found, do not include the preflight in your answer. Continue and generate the packet export only.

Use the source containing "GARDEN_META_SOURCE_ID: learning-packet-export-contract" as the required output contract.
Use the source containing "GARDEN_META_SOURCE_ID: vault-context-slice:evergreen-notes" as vault context.
Use the remaining notebook sources as the learning material.

Topic: Evergreen Notes: A System for Evolving Insight

Focus on:
- what evergreen notes are
- how they differ from conventional note-taking
- how they relate to Digital Garden
- whether Evergreen Note should become a trusted concept
- tensions around ritual, maintenance, and over-optimization

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list the garden meta-sources as learning sources in the Source List.
Do not create wikilinks for suggested new synthesis notes or new candidate concepts.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```
