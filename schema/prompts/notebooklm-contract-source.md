# Learning Packet Export Contract

Add this file to NotebookLM as a source named `Learning Packet Export Contract`.

NotebookLM should use this source as the stable output contract for packet exports.

## Purpose

Create a portable Markdown packet export that can later be normalized into a Markdown-first learning garden.

The export is not trusted wiki output. It is advisory material for local review.

## Protocol Rules

- Output only Markdown.
- Do not wrap the whole answer in a code block.
- Use literal Markdown syntax characters. Heading lines must visibly begin with `#`, `##`, or `###`.
- Do not convert headings into rich-text document headings.
- The first line of the output must be the topic title as a literal Markdown H1: `# <Topic Title>`.
- Use the exact required headings listed below, exactly once.
- Use wikilinks only for notes explicitly supplied in the vault context source.
- Do not wrap wikilinks in backticks. Wikilinks must appear as plain Markdown links, like `[[wiki/concepts/digital-garden|Digital Garden]]`.
- If referring to a note that does not exist in the vault context source, write `NEW CANDIDATE: <title>` instead of a wikilink.
- Do not invent note names, folder names, or vault areas.
- De-duplicate sources in the Source List.
- If a source URL is unavailable or unknown, write `URL: unknown`.
- Do not invent placeholder URLs.
- If a concept already exists in the vault context source, mark it as `existing` and suggest a patch instead of promotion.
- If no human-contact artifact is supplied, write exactly: `MISSING: human-contact artifact required before promotion.`

## Output Self-Check

Before returning the final answer, silently verify:

- The first line starts with `# `.
- Each required section heading starts with `## `.
- Each candidate concept starts with a `### <Concept Title>` heading.
- Suggested new notes use plain titles or `NEW CANDIDATE: <title>`, not invented wikilinks.
- Existing-note wikilinks are not wrapped in backticks.
- Protocol/context sources are not listed as learning sources.

## Required Output Shape

# <Topic Title>

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

Do not omit the `### <Concept Title>` line. A concept entry without a title heading is invalid.

## Important Claims

List important claims from the sources. Include source references where possible.

## Questions And Uncertainties

List open questions, tensions, or things that should remain unresolved.

## Suggested Trusted Wiki Output

Suggest:

- one synthesis note title as plain text, not a wikilink, unless the note already exists in the supplied vault context
- zero or more concept notes worth promoting; new concept notes must use `NEW CANDIDATE: <title>`
- suggested patches to existing notes from the supplied vault context
- potential future notes that do not exist yet; these must use `NEW CANDIDATE: <title>`

Only target supplied vault context notes in suggested patches.

## Human-Contact Artifact

Include the supplied human-contact artifact. If no artifact was supplied, write exactly:

`MISSING: human-contact artifact required before promotion.`
