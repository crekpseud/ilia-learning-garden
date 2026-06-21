# Treat Markdown as the codebase

The project will treat the Obsidian-compatible Markdown vault as the durable codebase of the learning system. Obsidian is the first IDE, NotebookLM is a replaceable remote synthesis engine, Codex is a replaceable local automation agent, and Google Drive is a replaceable bridge; none of these tools owns the core model.

**Considered Options**

- Build around Obsidian as the primary application.
- Build around Codex as the primary automation environment.
- Build around NotebookLM as the primary learning source.
- Treat Markdown files and conventions as the primary system boundary.

**Consequences**

The repository should prefer Markdown schemas, prompts, logs, packet exports, and generated notes as first-class artifacts. Tooling can be added around the vault, but the vault structure must remain understandable and usable without any single vendor or client.
