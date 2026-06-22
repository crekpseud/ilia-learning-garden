# Packet Export Contract

A packet export is a portable Markdown artifact produced by an external learning or synthesis tool. Bridges validate this structure before normalizing the export into a learning packet.

## Required Headings

```markdown
# <Topic Title>

## Source List

## Learning Summary

## Key Ideas

## Candidate Concept Notes

## Important Claims

## Questions And Uncertainties

## Suggested Trusted Wiki Output

## Human-Contact Artifact
```

## Optional Headings

```markdown
## Connections To Existing Knowledge
## Glossary
## Quiz Or Flashcards
## Personal Reflection
```

## Notes

- Optional YAML frontmatter is allowed.
- Required headings must use literal Markdown heading markers.
- The topic title must be a visible Markdown H1 that starts with `# `.
- Required section headings must be visible Markdown H2 lines that start with `## `.
- Required headings must appear exactly once.
- Bridges should preserve the original packet export in the inbox before normalization.
- Missing required headings cause strict import failure unless explicit import repair is requested.
- Wikilinks should refer only to notes supplied in the prompt's vault context.
- Wikilinks should appear as plain wikilinks, not inline code.
- Nonexistent notes should be marked as `NEW CANDIDATE: <title>`.
- Suggested new synthesis notes and future notes should not be invented wikilinks.
- Sources should be de-duplicated.
- Unknown URLs should be written as `URL: unknown`; placeholder URLs are invalid.

## Import Quality Tiers

Bridge validation assigns one of these tiers:

- `strict-valid`: the export satisfies the required headings, candidate concept format, wikilink rules, source rules, and human-contact marker rule.
- `repairable`: the export fails strict validation but satisfies the minimum repairability contract below.
- `rejected`: the export is too incomplete, too ambiguous, or too detached from source material to repair safely.

Only `strict-valid` exports normalize directly. `repairable` exports require an explicit `artifacts/import-repair.md` record before local normalization. `rejected` exports should not become packet drafts.

## Minimum Repairability Contract

A malformed packet export is repairable only when it contains enough material for local repair without inventing the learning substance.

It must contain:

- a visible topic title or otherwise unambiguous topic
- a substantive synthesis, summary, or set of key ideas
- a source list, source URLs, or enough source clues to preserve provenance honestly
- candidate concepts, important claims, or enough concept-level material to draft candidates locally
- either the exact missing-human-contact marker or an absence of human contact that is clearly detectable

It is not repairable when:

- the topic cannot be identified
- the answer is mostly meta-commentary about the task rather than learning material
- source provenance is absent and cannot be represented honestly
- local repair would require inventing concepts, claims, or sources not present in the export
- the answer contains conflicting instructions that make the packet state unclear

## Candidate Concept Format

Each candidate concept should use this structure:

```markdown
### <Concept Title>

- Status: existing / new candidate / possible duplicate
- Definition:
- Why it matters:
- Possible aliases:
- Related existing notes:
- Promotion recommendation: yes / maybe / not yet
- If existing, suggested patch:
```

The `### <Concept Title>` heading is required for each concept. A candidate concept entry without a title heading is invalid.

## Human-Contact Missing Value

If no human-contact artifact is supplied, the `## Human-Contact Artifact` section should contain exactly:

```text
MISSING: human-contact artifact required before promotion.
```
