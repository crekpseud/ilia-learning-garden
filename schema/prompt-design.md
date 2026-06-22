# Prompt Design

Prompts are bridge artifacts. They teach external LLMs how to produce packet exports that fit this vault's protocol.

## Principle

Keep prompt templates stable and inject current context at use time.

NotebookLM knows the notebook sources, but does not know the vault. The vault knows the protocol and trusted notes, but does not know the NotebookLM source structure. A packet export prompt bridges that gap by combining:

- stable packet export requirements
- current vault context
- topic-specific guidance
- human-contact material

## Prompt Template Rule

Prompt templates should live in:

```text
schema/prompts/
```

They should define placeholders for variable context instead of hard-coding one packet.

Examples:

- `{{TOPIC_TITLE}}`
- `{{TOPIC_GUIDANCE}}`
- `{{VAULT_CONTEXT}}`
- `{{HUMAN_CONTACT}}`

## Prompt Source Artifact Rule

For source-grounded tools like NotebookLM, prefer adding stable instructions as notebook sources and using a short run prompt in chat.

Use source artifacts for:

- the packet export contract
- the vault context slice
- long topic guidance
- reusable rules that may exceed chat prompt limits

Use the chat prompt for:

- naming the current task
- pointing to the relevant source artifacts
- adding brief emphasis for the current run
- asking for Markdown-only output

This keeps NotebookLM grounded in the same protocol while avoiding oversized chat prompts.

## Literal Markdown Rule

Packet exports must preserve literal Markdown syntax, especially heading markers.

External tools or Google Docs may render headings visually and lose the leading `#` characters when exported as text. For packet exports, the visible characters matter:

- the topic title line starts with `# `
- required sections start with `## `
- candidate concept titles start with `### `

If a bridge output loses these markers, use explicit import repair before normalization.

## Wikilink Code Rule

Wikilinks are part of the graph. External LLMs should not wrap wikilinks in backticks.

Good:

```markdown
[[wiki/concepts/digital-garden|Digital Garden]]
```

Bad:

```markdown
`[[wiki/concepts/digital-garden|Digital Garden]]`
```

If an output backticks wikilinks, repair them before import so Obsidian and local validation can treat them as links.

## NotebookLM Transport Rule

Direct copy-paste from NotebookLM currently preserves literal Markdown better than exporting through Google Docs.

Use direct copy-paste as the default manual NotebookLM bridge. Treat Google Docs export as a rich-text transport that may require fenced-code output or local repair before strict import.

## Vault Context Injection Rule

Before using a prompt template with an external LLM, inject only the relevant current vault context. Prefer a topic-specific context slice over a whole-vault dump.

Good context candidates:

- existing synthesis notes relevant to the topic
- existing concept notes and aliases
- accepted protocol principles
- known suggested-patch targets
- explicit human-contact artifact

Context selection should optimize for relevance, not volume. Too much unrelated context can cause the external LLM to overfit to the vault instead of the notebook sources.

Avoid:

- dumping the whole vault
- including unrelated private context
- treating candidate concepts as trusted concepts
- asking the external LLM to promote notes directly
- allowing the external LLM to invent wikilinks for notes not supplied in context
- allowing placeholder source URLs or duplicate source entries to pass as clean source records

## Vault Context Slice Rule

A vault context slice is the small set of trusted notes, concepts, aliases, protocol principles, and suggested-patch targets that are relevant to the current notebook topic.

Use a slice when prompting external LLMs. Do not paste the whole vault by default.

A good slice should include:

- directly relevant trusted concepts
- directly relevant synthesis notes
- aliases that help concept recognition
- protocol principles that should guide the export
- notes that may receive suggested patches

A slice should exclude:

- unrelated trusted notes
- unrelated project docs
- stale candidate concepts
- private context not needed for the packet

The slice can be assembled manually at first. Later, an agent or tool can suggest candidate context by searching titles, aliases, links, and index entries.

## External LLM Boundary

External LLMs may produce packet exports, candidate concepts, and suggested trusted wiki output. They do not promote trusted notes. Promotion remains a local protocol step.

## Wikilink Rule

External LLMs should only use wikilinks that are supplied in the injected vault context. If the model wants to refer to a note that does not exist yet, it should use:

```text
NEW CANDIDATE: <title>
```

This keeps packet exports from inventing graph nodes.

## Existing Concept Rule

If the injected vault context includes an existing concept, the external LLM should mark that concept as `existing` and suggest a patch instead of recommending promotion.

## Missing Human Contact Rule

If no human-contact material is injected, the external LLM should write exactly:

```text
MISSING: human-contact artifact required before promotion.
```

The packet may still be imported, but promotion remains blocked.
