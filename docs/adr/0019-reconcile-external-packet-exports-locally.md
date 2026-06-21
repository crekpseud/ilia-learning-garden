# Reconcile external packet exports locally

Packet exports produced by NotebookLM or another external LLM are advisory. The local protocol must reconcile them against the current vault before promotion by validating structure, preserving provenance, resolving existing concepts versus new candidates, and translating proposed wiki changes into reviewable drafts and patches.

**Considered Options**

- Trust external packet exports as ready-to-promote wiki output.
- Reject external exports unless they perfectly know the vault.
- Reconcile external exports locally before review.
- Make NotebookLM or another remote tool the source of truth for packet state.

**Consequences**

The vault remains the durable source of truth, and external tools can be swapped without changing the protocol. This prevents duplicate trusted concepts, invented wikilinks, and silent promotion, at the cost of a local reconciliation step that future tooling should automate.