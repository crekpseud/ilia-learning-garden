# NotebookLM Run Prompt - Emoji Education AI Communication

Paste this into the NotebookLM chat after adding:

- a source containing `GARDEN_META_SOURCE_ID: learning-packet-export-contract`
- a source containing `GARDEN_META_SOURCE_ID: vault-context-slice:emoji-education-ai-communication`
- the notebook's learning sources

```markdown
Create a Learning Packet Export in Markdown.

Before generating, silently check whether you can access the required garden meta-sources by content marker, not by NotebookLM filename.

Required markers:
- GARDEN_META_SOURCE_ID: learning-packet-export-contract
- GARDEN_META_SOURCE_ID: vault-context-slice:emoji-education-ai-communication

If either marker is missing, do not create the packet. Return only:

# Packet Export Preflight

## Meta-Sources Detected

- FOUND or MISSING: learning-packet-export-contract
- FOUND or MISSING: vault-context-slice:emoji-education-ai-communication

## Readiness

NOT READY: One or more required meta-sources are missing.

If both markers are found, do not include the preflight in your answer. Continue and generate the packet export only.

Use the source containing "GARDEN_META_SOURCE_ID: learning-packet-export-contract" as the required output contract.
Use the source containing "GARDEN_META_SOURCE_ID: vault-context-slice:emoji-education-ai-communication" as vault context.
Use the remaining notebook sources as the learning material.

Topic: Decoding Digital Symbols: Emojis in Education and AI Communication

Focus on:
- emojis as contextual digital symbols, visual language, paralanguage, and emotional punctuation
- education uses such as emotional fluency, history narration, literacy practice, social-emotional check-ins, and feedback
- how emojis may support playful knowledge practice, memory, and lightweight gamification
- the risk that emojis become ritualized clutter, emotional oversimplification, or protocol theater
- LLM difficulty with emoji disambiguation, pragmatic reasoning, culture, timing, sarcasm, and implicit social intent
- what this packet should teach a Markdown-first learning garden about visual symbols and optional human expression layers

Output only Markdown.
Do not wrap the answer in a code block.
Use literal Markdown heading markers. The first line must start with "# ". Required section headings must start with "## ". Candidate concept titles must start with "### ".
Do not list the garden meta-sources as learning sources in the Source List.
Do not create wikilinks for suggested new synthesis notes or new candidate concepts.
Do not wrap wikilinks in backticks.
If no human-contact artifact is supplied, use the missing-human-contact marker from the contract.
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```
