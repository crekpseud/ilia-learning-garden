# Use strict import with explicit repair

Bridge imports will validate packet exports against the expected Markdown contract and fail without normalizing when required structure is missing. Malformed exports may be saved in the inbox with an import error, and LLM-assisted repair can be run explicitly afterward.

**Considered Options**

- Strictly reject malformed imports.
- Save malformed imports and create a repair task.
- Automatically use an LLM to repair malformed imports.
- Best-effort normalize whatever can be parsed.
- Use strict import by default with explicit repair mode.

**Consequences**

The normal bridge path stays deterministic and trustworthy. LLM repair remains available, but malformed input cannot silently become a learning packet.
