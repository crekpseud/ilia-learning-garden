# Import Repair

The preserved inbox export did not satisfy [[schema/packet-export-contract]].

## Contract Failures

- Used `## Synthesis Summary` instead of required `## Learning Summary`.
- Used `## Candidate Concepts` instead of required `## Candidate Concept Notes`.
- Omitted required sections:
  - `## Key Ideas`
  - `## Important Claims`
  - `## Questions And Uncertainties`
  - `## Suggested Trusted Wiki Output`
- Candidate concepts had `###` headings but did not use the required bullet structure.
- Repeated deferred concepts from the vault context slice as `NEW CANDIDATE` lines even though the packet did not add new source-specific material about them.
- Listed one source URL in the title position while also saying `URL: unknown`.

## Local Repair

Local normalization repaired the export into:

- [[learning/packets/architecture-of-original-thought/drafts/synthesis]]
- [[learning/packets/architecture-of-original-thought/drafts/concepts]]
- [[learning/packets/architecture-of-original-thought/drafts/patches]]
- [[learning/packets/architecture-of-original-thought/sources]]
- [[learning/packets/architecture-of-original-thought/review]]

The raw export remains unchanged at [[learning/inbox/notebooklm/architecture-of-original-thought/packet-export]].

## Prompt Lesson

NotebookLM may still collapse required sections even after a successful preflight. For the next run, consider adding a final instruction to the run prompt:

```markdown
Before answering, compare your output headings against the required headings from the contract. If any required heading is missing or renamed, fix it before sending.
```
