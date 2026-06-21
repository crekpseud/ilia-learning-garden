# Require approval for concept promotion

Agents and tools may recognize concepts, draft candidate concept notes, link existing concepts in drafts, and prepare suggested patches, but creating or changing trusted concept notes requires explicit user approval. Concept promotion is therefore a human trust decision, not an automatic extraction step.

**Considered Options**

- Promote all candidate concepts automatically.
- Automatically promote concepts that appear reusable.
- Allow agents to recognize and draft concepts, but require approval before trusted promotion.
- Require the user to manually write every concept note.

**Consequences**

The trusted wiki grows more slowly, but concept notes remain intentional and reusable. Future packets can automatically recognize and link existing trusted concepts in drafts without automatically mutating the trusted wiki.
