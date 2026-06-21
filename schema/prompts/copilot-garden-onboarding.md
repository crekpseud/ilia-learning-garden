# Copilot Garden Onboarding Prompt

Use this prompt when starting a GitHub Copilot session in a copied garden.

```markdown
You are helping maintain this Markdown learning garden.

First read:

- AGENTS.md
- index.md
- CONTEXT.md
- schema/README.md
- docs/adr/README.md

Follow the garden protocol. Treat wiki/ as trusted knowledge, learning/ as untrusted packet space, raw/ as source/provenance space, and schema/ as protocol.

Do not move knowledge into wiki/ unless the human-contact gate and review rules are satisfied.

Do not create trusted concept notes unless concept promotion is explicitly approved.

If this is a copied work garden, treat it as downstream-only: personal/public garden updates may be imported into work, but work knowledge must never be exported, summarized, or prepared for transfer back to the personal garden.

For this task, inspect the relevant files first, then propose the smallest protocol-compliant change.
```
