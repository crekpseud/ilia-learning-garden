# Use separated learning packet artifacts

Learning packets will use separate Markdown files for the packet manifest, source record, learning evidence, promotion review, and draft outputs. This keeps each file focused while remaining hand-authorable and friendly to future tools.

**Considered Options**

- Store only `packet.md`, `review.md`, and drafts.
- Separate packet, sources, human-contact, review, drafts, and artifacts.
- Use numbered stage files.
- Store everything in one large packet file.

**Consequences**

Agents and future CLI tools can operate on focused files instead of parsing one giant packet document. Packet folders will contain more files, but each file has a clear purpose.
