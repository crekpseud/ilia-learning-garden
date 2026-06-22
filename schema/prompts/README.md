# Prompts

Reusable prompts for external LLMs and bridge workflows live here.

Prompts should separate:

- stable protocol requirements
- vault context supplied by the local system
- topic-specific instructions
- user reflection or human-contact material

## Available Prompts

- [[notebooklm-contract-source]] - Add this as a NotebookLM source containing the stable packet export contract.
- [[vault-context-slice-template]] - Create a topic-specific vault context source for NotebookLM.
- [[notebooklm-run-prompt]] - Short chat prompt that asks NotebookLM to produce the packet export from its sources.
- [[notebooklm-repair-prompt]] - Repair useful NotebookLM output that failed the Markdown contract.
- [[notebooklm-packet-export]] - Legacy monolithic prompt for tools that can accept longer chat prompts.
- [[copilot-garden-onboarding]] - Start a Copilot session inside a copied garden.
