# Use a protocol-first top-level structure

The repository will expose the learning protocol at the top level with folders such as `schema`, `learning`, `raw`, and `wiki`. Project documentation remains in `docs`, but the vault protocol is not nested under `docs` or a tool-specific application folder.

**Considered Options**

- Put protocol folders at the repository root.
- Use numbered Obsidian folders.
- Put the vault under a nested `vault` folder.
- Keep all content under `docs`.

**Consequences**

The repository reads as a Markdown codebase first. Tools, clients, and bridges should operate on the top-level protocol folders rather than owning the structure.
