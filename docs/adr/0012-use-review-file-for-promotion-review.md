# Use a review file for promotion review

Each learning packet will use a separate `review.md` file to record promotion review state. Codex or another agent may still present Git diffs during promotion, but the durable approval record lives in Markdown with the packet.

**Considered Options**

- Put a promotion checklist inside `packet.md`.
- Use only Codex chat and Git diffs.
- Use a separate `review.md` file.
- Use Git branch or commit review as the approval mechanism.
- Use Obsidian tags or frontmatter as the only review state.

**Consequences**

Promotion review becomes portable, auditable, and usable by non-Codex workflows. The packet folder will contain both learning evidence and promotion approval state.
