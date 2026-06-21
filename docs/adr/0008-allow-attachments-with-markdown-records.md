# Allow attachments with Markdown records

The vault will be Markdown-first rather than Markdown-only. Non-Markdown attachments such as PDFs, images, audio files, CSVs, and exported artifacts may live in the vault when they are referenced and contextualized by Markdown records.

**Considered Options**

- Store only Markdown files in the vault.
- Allow attachments directly in the vault with Markdown as the canonical record.
- Keep all attachments outside the vault in a separate cache.
- Allow attachments only as temporary bridge files.

**Consequences**

The system must treat Markdown records as the canonical source of context and provenance, even when the underlying material is a non-Markdown attachment. Tooling should never require understanding an attachment without a corresponding Markdown record.
