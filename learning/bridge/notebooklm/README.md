# NotebookLM Bridge

Prepared NotebookLM bridge materials live here.

## Areas

- [[learning/bridge/notebooklm/context-slices/README|Context Slices]] - topic-specific vault context files to add to NotebookLM as sources.
- [[learning/bridge/notebooklm/run-prompts/README|Run Prompts]] - short NotebookLM chat prompts that refer to contract and context sources.

## Copy-Text Setup

NotebookLM may generate source filenames when text is pasted directly. Do not rely on those filenames.

Each garden meta-source should identify itself with `GARDEN_META_SOURCE_ID` at the top of the copied text. Run prompts should refer to those marker lines.

For a new NotebookLM packet, prepare three copyable texts:

- `learning-packet-export-contract`
- `vault-context-slice`
- `prompt`
