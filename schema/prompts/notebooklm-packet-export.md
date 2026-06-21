# NotebookLM Packet Export Prompt

Use this prompt inside a NotebookLM notebook to produce a packet export that can later be normalized into this vault's learning packet structure.

## Design

NotebookLM knows the notebook sources, but it does not know this vault or protocol unless we tell it. The local vault knows the protocol and current trusted notes, but it does not know how the NotebookLM sources are organized unless NotebookLM reports them.

This prompt therefore has four parts:

1. Stable packet export contract.
2. Injected vault context.
3. Topic-specific guidance.
4. Human-contact artifact.

## Prompt Template

```markdown
Create a Learning Packet Export in Markdown for my Markdown-first learning pipeline.

Use the sources in this notebook and produce a structured export that can be parsed by another tool.

Output only Markdown. Do not wrap the whole answer in a code block.

## Vault Context

The destination vault uses this protocol:

- Markdown is the durable protocol.
- The vault is read topographically through links, concepts, maps, and synthesis notes.
- Workflow history is append-only in logs, packet reviews, and Git.
- Trusted notes change through reviewed patches, not silent rewrites.
- Candidate concepts are suggestions only. Concept promotion requires human approval.
- A packet normally promotes one synthesis note by default, plus zero or more reusable concept notes.

Existing trusted notes and concepts that may be relevant:

{{VAULT_CONTEXT}}

## Topic

{{TOPIC_TITLE}}

## Topic Guidance

{{TOPIC_GUIDANCE}}

## Human-Contact Artifact

Record this human-contact artifact in the final section:

{{HUMAN_CONTACT}}

## Strict Output Rules

- Use wikilinks only for notes explicitly listed in Vault Context.
- If you want to refer to a note that does not exist in Vault Context, write `NEW CANDIDATE: <title>` instead of a wikilink.
- Do not invent note names, folder names, or vault areas.
- De-duplicate sources in the Source List.
- If a source URL is unavailable or unknown, write `URL: unknown`.
- Do not invent placeholder URLs.
- If a concept already exists in Vault Context, mark it as `existing` and suggest a patch instead of promotion.
- If no human-contact artifact is supplied, write exactly: `MISSING: human-contact artifact required before promotion.`

Use these exact required headings, exactly once:

# {{TOPIC_TITLE}}

## Source List

List the sources used in the notebook. De-duplicate sources. For each source, include:

- Title:
- Author:
- URL:
- Description:

## Learning Summary

Summarize the core idea of this notebook and how it relates to personal knowledge, learning loops, AI-assisted knowledge work, and the supplied vault context.

## Key Ideas

List the most important ideas as bullets. Prefer conceptual clarity over exhaustiveness.

## Candidate Concept Notes

Suggest reusable concepts that may deserve Obsidian concept notes. Use this exact structure for each concept:

### <Concept Title>

- Status: existing / new candidate / possible duplicate
- Definition:
- Why it matters:
- Possible aliases:
- Related existing notes:
- Promotion recommendation: yes / maybe / not yet
- If existing, suggested patch:

## Important Claims

List important claims from the sources. Include source references where possible.

## Questions And Uncertainties

List open questions, tensions, or things that should remain unresolved.

## Suggested Trusted Wiki Output

Suggest:

- one synthesis note title
- zero or more concept notes worth promoting
- suggested patches to existing notes from the supplied vault context
- potential future notes that do not exist yet

Only target supplied Vault Context notes in suggested patches.

## Human-Contact Artifact

Include the supplied human-contact artifact. If no artifact was supplied, write exactly:

`MISSING: human-contact artifact required before promotion.`
```

## Example Vault Context

```markdown
- [[wiki/synthesis/llm-wiki-pattern|LLM Wiki Pattern]]
- [[wiki/synthesis/digital-garden-ethos|Digital Garden Ethos]]
- [[wiki/concepts/digital-garden|Digital Garden]]
- [[docs/adr/0016-use-topographical-reading-with-append-only-process-history|Topographical reading with append-only process history]]
```