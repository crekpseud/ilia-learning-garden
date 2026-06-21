# Garden Agent Instructions

This repository is a Markdown-first learning garden. Treat Markdown files as the durable system of record.

## Start Here

Before changing files, read:

- [[index]]
- [[CONTEXT]]
- [[schema/README]]
- [[docs/adr/README]]

For Copilot or other agents that do not follow Obsidian wikilinks automatically, open the same files by path:

- `index.md`
- `CONTEXT.md`
- `schema/README.md`
- `docs/adr/README.md`

## Trust Boundaries

- `wiki/` is trusted, reviewed knowledge.
- `learning/` is untrusted packet, draft, review, and human-contact space.
- `raw/` stores source records and supporting materials.
- `schema/` defines the protocol.
- `docs/adr/` records protocol decisions.

Do not move knowledge into `wiki/` unless the human-contact gate and promotion review rules are satisfied.

Do not create a trusted concept note just because a source or LLM suggests it. Candidate concepts stay in packet drafts until the user approves promotion.

Do not silently rewrite existing trusted notes. Use suggested patches and review records when a packet changes trusted knowledge.

## Work Garden Boundary

If this garden is copied into a restricted work environment, treat that copy as a downstream work garden.

Allowed:

- Import personal-garden protocol updates into the work garden.
- Import public, non-confidential personal-garden knowledge that is explicitly allowed.
- Grow private work learning packets and work trusted notes inside the work garden.

Forbidden:

- Export work-garden knowledge back to the personal garden.
- Prepare patches, summaries, bundles, or prompts that move work-specific information out of the work environment.
- Treat work and personal gardens as bidirectional sync peers.

Use one-way import language, not sync language.

## Editing Rules

- Keep files Markdown-first and link-rich.
- Preserve raw packet exports; normalize and repair in packet artifacts instead.
- Prefer topic-specific context slices over whole-vault dumps.
- Keep deferred candidate concepts as plain text or code paths, not wikilinks.
- Keep tool-specific instruction files small and point back to the protocol docs.
