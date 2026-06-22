# Separate bridge inputs from inbox outputs

Locally prepared materials for external tools should live under `learning/bridge/`. External tool outputs should land under `learning/inbox/` before normalization into learning packets.

**Considered Options**

- Store all NotebookLM-related materials under `learning/inbox/notebooklm/`.
- Store prompt and context slice materials under `schema/`.
- Separate locally prepared bridge inputs from externally produced inbox outputs.
- Store topic context slices directly inside packet folders before packet creation.

**Consequences**

The inbox stays semantically clean: it receives outputs from outside tools. The bridge area holds materials the local garden prepares for outside tools, such as NotebookLM context slices. This distinction should make future automation easier because importers can watch inbox paths without confusing locally prepared run materials for external packet exports.
