# Use topographical reading with append-only process history

The vault should be read topographically but changed historically. Trusted knowledge is navigated through links, concepts, maps, and synthesis notes rather than reverse chronology; workflow history is recorded append-only in logs, packet reviews, and Git; existing trusted notes change through reviewed patches.

**Considered Options**

- Organize knowledge primarily by reverse chronology.
- Treat notes as immutable events and derive current knowledge as projections.
- Keep trusted notes as living documents while recording process history append-only.
- Allow silent rewrites of trusted notes when agents find improvements.

**Consequences**

The reading experience stays garden-like and meaning-oriented, while the process remains auditable like an event stream. Git handles mechanical history, and the protocol records semantic history: why knowledge changed, which packet caused it, and what was approved.
