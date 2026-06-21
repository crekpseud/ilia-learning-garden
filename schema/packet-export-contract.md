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

