# Treat prompt templates as bridge artifacts

Prompt templates are part of the bridge protocol. They should be stored as reusable Markdown files with placeholders for vault context, topic guidance, and human-contact artifacts, rather than kept only in chat history or hard-coded for one notebook.

**Considered Options**

- Keep prompts only in chat history.
- Store one-off prompts for each notebook.
- Store reusable prompt templates and inject current context at use time.
- Let external LLMs infer the protocol without prompt structure.

**Consequences**

NotebookLM and other external LLMs can produce packet exports without knowing the vault by default. The local system remains responsible for supplying relevant context and for promoting trusted notes after review.