# Prompts

Reusable prompts for external LLMs and bridge workflows live here.

Prompts should separate:

- stable protocol requirements
- vault context supplied by the local system
- topic-specific instructions
- user reflection or human-contact material

For NotebookLM copy-text setup, prepare exactly three texts for the user:

- the packet export contract, with `GARDEN_META_SOURCE_ID: learning-packet-export-contract`
- the topic-specific vault context slice, with `GARDEN_META_SOURCE_ID: vault-context-slice:<topic-slug>`
- the run prompt, which refers to both sources by `GARDEN_META_SOURCE_ID` marker rather than NotebookLM filename

For the preferred Source-Manifest-First NotebookLM bridge, prepare a single short source-manifest prompt first. Use the three-text packet export setup only as fallback.

## Available Prompts

- [[notebooklm-source-manifest-prompt]] - Ask NotebookLM for a compact source manifest before local packet creation.
- [[notebooklm-contract-source]] - Add this as a NotebookLM source containing the stable packet export contract.
- [[vault-context-slice-template]] - Create a topic-specific vault context source for NotebookLM.
- [[notebooklm-run-prompt]] - Short chat prompt that asks NotebookLM to produce the packet export from its sources.
- [[notebooklm-repair-prompt]] - Repair useful NotebookLM output that failed the Markdown contract.
- [[notebooklm-packet-export]] - Legacy monolithic prompt for tools that can accept longer chat prompts.
- [[copilot-garden-onboarding]] - Start a Copilot session inside a copied garden.
