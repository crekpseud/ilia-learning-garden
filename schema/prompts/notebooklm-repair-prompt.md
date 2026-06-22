# NotebookLM Repair Prompt

Use this when NotebookLM produced useful content but failed the packet export contract.

```markdown
Repair the previous answer into strict Markdown packet-export format.

Rules:
- Output only Markdown.
- Do not wrap the whole answer in a code block.
- Use literal Markdown heading markers.
- The first line must start with "# " and contain the topic title.
- Each required section heading must start with "## ".
- Under "## Candidate Concept Notes", each concept must start with "### <Concept Title>".
- Do not create wikilinks for notes that were not supplied in Vault Context.
- Do not wrap wikilinks in backticks.
- Suggested new synthesis notes must be plain text, not wikilinks.
- New concept notes must be written as NEW CANDIDATE: <title> outside the concept heading.
- Keep the exact human-contact marker if no artifact was supplied:
MISSING: human-contact artifact required before promotion.

Required topic title:
# <Topic Title>
```
