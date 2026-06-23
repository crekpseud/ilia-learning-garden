# Prompt Design

Prompts are bridge artifacts. They teach external LLMs how to produce source manifests or packet exports that fit this vault's protocol.

## Principle

Keep prompt templates stable and inject current context at use time.

NotebookLM knows the notebook sources, but does not know the vault. The vault knows the protocol and trusted notes, but does not know the NotebookLM source structure.

For source-heavy NotebookLM notebooks, prefer asking NotebookLM for a full Packet Export after adding the packet export contract and a topic-specific vault context slice as sources. NotebookLM is allowed to do the heavy source digestion; the local garden agent validates, repairs, reconciles, and gardens the result.

A full packet export prompt combines:

- stable packet export requirements
- current vault context
- topic-specific guidance
- human-contact material

A Source Manifest prompt is a diagnostic bridge when provenance, URL recovery, blocked sources, or packet quality need investigation.

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

For source-grounded tools like NotebookLM, keep stable instructions as copied-text sources and use short run prompts that refer to those sources by `GARDEN_META_SOURCE_ID`.

Use source artifacts for normal NotebookLM packet export:

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

## NotebookLM Source Manifest Rule

When source provenance or packet quality needs investigation, ask NotebookLM for a Source Manifest.

The manifest should ask for:

- notebook title
- source count shown by NotebookLM
- source title, author, URL, and description for each source
- exact URLs for web and YouTube sources
- `not applicable - uploaded file` or `not applicable - copied text` when there is no URL-bearing source
- URL visibility labels such as `exact`, `domain-only`, `not-visible`, and `not-applicable`
- local recovery actions so the agent knows what to search, request, replace, or treat as NotebookLM-only
- a `NOT READY` preflight response only when there are zero usable learning sources
- 5-10 key themes or tensions
- notes about sources that are YouTube videos, private files, uploads, or otherwise hard for the local agent to inspect

Do not ask NotebookLM to promote concepts or update trusted notes.

Do not use Source Manifest as the default for large source-heavy notebooks. In those cases, NotebookLM's ability to digest books, large PDFs, YouTube transcripts, uploaded files, and mixed source sets is the bridge's main value.

## NotebookLM Copy-Text Source Identity Rule

When adding prompt source artifacts to NotebookLM as copied text, include stable identity markers at the top of the copied text. Do not rely on NotebookLM's generated filenames.

The packet export contract must start with:

```markdown
GARDEN_META_SOURCE_ID: learning-packet-export-contract
GARDEN_META_SOURCE_KIND: packet-export-contract
GARDEN_META_SOURCE_TITLE: Learning Packet Export Contract
```

A vault context slice must start with:

```markdown
GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>
GARDEN_META_SOURCE_KIND: vault-context-slice
GARDEN_META_SOURCE_TITLE: Vault Context Slice - <Topic Title>
```

Run prompts should refer to these marker lines, not to source filenames or UI titles.

## NotebookLM Three-Text Setup Rule

When preparing a new NotebookLM packet export, provide the user with three copyable texts:

- `learning-packet-export-contract`
- `vault-context-slice`
- `prompt`

The prompt should first check for the two required Garden Meta-Source IDs. If either is missing, it should return a `NOT READY` preflight response instead of generating a packet. If both are present, it should generate only the packet export.

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
