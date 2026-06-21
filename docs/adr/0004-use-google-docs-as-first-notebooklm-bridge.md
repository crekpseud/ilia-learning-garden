# Use Google Docs as the first NotebookLM bridge

The first NotebookLM bridge will consume standardized packet exports saved from NotebookLM into Google Docs, then export those Docs to Markdown through Google Drive. NotebookLM remains the synthesis engine, Google Docs is only the transfer bridge, and the core system depends on portable Markdown packet exports rather than NotebookLM or Google-specific objects.

**Considered Options**

- Manually copy NotebookLM chat output into local Markdown.
- Scrape or automate the NotebookLM UI directly.
- Export NotebookLM notes to Google Docs and pull Markdown from Google Drive.
- Recreate NotebookLM-style synthesis from raw sources with another LLM.

**Consequences**

This removes the tedious copy-paste step while keeping the core bridgeable: future adapters can produce the same packet export format from ChatGPT, Claude, Gemini, local files, or another source.
