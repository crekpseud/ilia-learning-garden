# Import Repair

The preserved inbox export satisfies the required top-level headings from [[schema/packet-export-contract]], but it is not `strict-valid`.

## Import Quality Tier

- Tier: `repairable`

## Contract And Reconciliation Issues

- Candidate concept entries omitted the required `If existing, suggested patch:` field.
- Candidate concept entries used useful content, but local normalization converted them to the exact packet concept structure.
- The raw `## Human-Contact Artifact` section contains a prepared Audio Overview entry, not evidence that the user listened to it or reflected on it.
- The notebook screen showed 10 sources, but the packet export listed 9 source records. The missing source is not invented locally.
- The suggested synthesis note was written as `NEW CANDIDATE: Object Thinking and the Digital Garden (Synthesis Note)`. Local normalization treats it as a proposed synthesis title, not a concept candidate.

## Local Repair

Local normalization repaired the export into:

- [[learning/packets/david-west-object-thinking/drafts/synthesis]]
- [[learning/packets/david-west-object-thinking/drafts/concepts]]
- [[learning/packets/david-west-object-thinking/drafts/patches]]
- [[learning/packets/david-west-object-thinking/sources]]
- [[learning/packets/david-west-object-thinking/review]]

The raw export remains unchanged at [[learning/inbox/notebooklm/david-west-object-thinking/packet-export]].
