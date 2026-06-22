# NotebookLM Run Prompt

Use this short chat prompt after adding these NotebookLM sources:

- `Learning Packet Export Contract`
- `Vault Context Slice - <Topic>`
- the actual learning sources for the topic

```markdown
Create a Learning Packet Export in Markdown.

Use the source named "Learning Packet Export Contract" as the required output contract.
Use the source named "Vault Context Slice - <Topic>" as vault context.
Use the remaining notebook sources as the learning material.

Topic: <Topic Title>

Focus on:
- <focus point 1>
- <focus point 2>
- <focus point 3>

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list "Learning Packet Export Contract" or "Vault Context Slice - <Topic>" as learning sources in the Source List.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
```

## Evergreen Notes Example

```markdown
Create a Learning Packet Export in Markdown.

Use the source named "Learning Packet Export Contract" as the required output contract.
Use the source named "Vault Context Slice - Evergreen Notes" as vault context.
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
Do not list "Learning Packet Export Contract" or "Vault Context Slice - Evergreen Notes" as learning sources in the Source List.
Do not create wikilinks for suggested new synthesis notes or new candidate concepts.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
```
