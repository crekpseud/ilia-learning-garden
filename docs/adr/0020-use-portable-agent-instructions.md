# Use portable agent instructions

The garden should include small, Markdown-based instruction files for common AI coding agents. These files should teach agents where to start, how to respect the learning protocol, and how to preserve one-way boundaries for downstream work gardens.

**Considered Options**

- Keep agent instructions only in chat history.
- Make Codex-specific skills the only automation surface.
- Add portable instruction files that point agents back to the garden protocol.
- Duplicate the full protocol inside every tool-specific instruction file.

**Consequences**

The garden becomes easier to copy into environments that use GitHub Copilot or another agent instead of Codex. The protocol remains in `schema/`, `CONTEXT.md`, and ADRs; agent instruction files act as entrypoints and guardrails, not as a second source of truth.
