# Concept Promotion

Concept notes are promoted conservatively. A candidate concept becomes a trusted concept only when the user approves that it has value beyond the current learning packet.

## Automation Boundary

Agents and future tools may automatically:

- recognize likely existing concepts by canonical title and aliases
- suggest new candidate concepts
- draft concept notes in `drafts/concepts.md`
- link to existing trusted concepts in draft material
- check `wiki/concepts/` for likely duplicates
- prepare suggested patches for existing concept notes
- update `index.md` and `log.md` after approved promotion

Agents and future tools must not automatically:

- create a new trusted concept note without approval
- change an existing trusted concept note without an approved suggested patch
- treat a candidate concept as trusted merely because it appears in a packet export
- promote every candidate concept from a packet by default

## Protocol Flow

```text
learning packet
-> drafts/concepts.md
-> concept recognition
-> promotion review
-> duplicate and alias check
-> create concept note or suggested patch
-> update index and log
-> ask before commit
```

## Approval Rule

The user approves concept promotion in `review.md`.

Example:

```markdown
## Approved Concept Promotions

- [x] Persistent Wiki -> [[wiki/concepts/persistent-wiki]]
```

## Existing Concept Rule

If a candidate matches an existing concept by canonical title or alias, the system should not create a duplicate note. It should link to the existing concept in drafts and prepare a suggested patch if the new packet adds important nuance.

## Linking Rule

Linking to existing trusted concepts is allowed in drafts. Creating or changing trusted concept notes requires approval.

## History Rule

Concept notes are living trusted notes, not immutable event streams. When a packet changes a concept, preserve the current concept note as readable knowledge and record the semantic change through `review.md`, `drafts/patches.md`, `log.md`, and Git.

## Concept Note Location

New trusted concept notes live in:

```text
wiki/concepts/<concept-slug>.md
```

Use `schema/templates/concept-note.md` as the starting template.
