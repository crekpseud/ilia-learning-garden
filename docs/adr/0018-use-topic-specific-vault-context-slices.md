# Use topic-specific vault context slices

External LLM prompts should receive a topic-specific vault context slice instead of a whole-vault dump. A slice includes the trusted concepts, synthesis notes, aliases, protocol principles, human-contact material, and suggested-patch targets that are relevant to the current learning packet.

**Considered Options**

- Paste the whole vault into external LLM prompts whenever possible.
- Give external LLMs no vault context and repair everything locally.
- Inject a small topic-specific context slice for each packet.
- Wait for automated retrieval before giving external tools any vault context.

**Consequences**

The external LLM gets enough context to avoid obvious duplicate concepts and stale assumptions, while the prompt stays focused on the material being learned. Context selection becomes an explicit protocol step that can be manual at first and automated later through title, alias, link, and index search.