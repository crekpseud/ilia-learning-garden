# Use NotebookLM source artifacts with short run prompts

NotebookLM packet export should use stable prompt source artifacts plus a short chat run prompt when the monolithic packet-export prompt is too large for the chat box.

**Considered Options**

- Keep shortening the monolithic NotebookLM chat prompt.
- Split the task into multiple chat turns.
- Add protocol and vault context as NotebookLM sources, then use a short run prompt.
- Move all packet drafting out of NotebookLM and into the local agent.

**Consequences**

NotebookLM can stay focused on its strength: synthesizing its notebook sources. The packet export contract and vault context become visible source material instead of oversized chat text. The local garden still owns validation, reconciliation, human-contact gating, and promotion.

Direct copy-paste from NotebookLM should be preferred for now because it preserves literal Markdown heading markers better than Google Docs export. Google Docs export is a rich-text transport and may require fenced-code output or local repair before strict import.
