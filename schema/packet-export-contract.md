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
- Required headings must appear exactly once.
- Bridges should preserve the original packet export in the inbox before normalization.
- Missing required headings cause strict import failure unless explicit import repair is requested.
- Wikilinks should refer only to notes supplied in the prompt's vault context.
- Nonexistent notes should be marked as `NEW CANDIDATE: <title>`.
- Sources should be de-duplicated.
- Unknown URLs should be written as `URL: unknown`; placeholder URLs are invalid.

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

## Human-Contact Missing Value

If no human-contact artifact is supplied, the `## Human-Contact Artifact` section should contain exactly:

```text
MISSING: human-contact artifact required before promotion.
```