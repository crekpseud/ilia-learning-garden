# Operations

Canonical operation names for agents and future tools.

## Packet

**packet.create**:
Create a new learning packet skeleton from a title or topic.

**packet.draft**:
Create suggested trusted wiki output from an imported learning packet.

**packet.reconcile**:
Compare an imported packet export with the current vault, resolving existing concepts, new candidates, suggested patches, provenance, and human-contact status before review.

**packet.review**:
Prepare or update the promotion review for a drafted learning packet.

**packet.promote**:
Promote approved learning packet output into the trusted wiki.

## Garden

**garden.review**:
Actively interpret a packet, promotion, or trusted-wiki change in the context of the whole garden, looking for unexpected links, emerging narratives, protocol pressure, drift, next learning paths, and useful proposals.

**garden.propose**:
Record non-binding proposals that arise from gardening review, such as next packets, suggested patches, maintenance tasks, or warnings about over-optimization.

## Concepts

**concept.recognize**:
Identify existing trusted concepts and candidate new concepts in packet material or drafts.

**concept.promote**:
Promote a human-approved candidate concept note into the trusted wiki.

**concept.patch**:
Prepare a suggested patch for an existing trusted concept note.

## Bridges

**bridge.google-doc.import**:
Import a packet export from a Google Doc URL or file ID into the learning area.

**bridge.notebooklm.manual-import**:
Import a manually pasted NotebookLM packet export from `learning/inbox/notebooklm/<slug>/packet-export.md` into the learning area.

## Wiki

**wiki.lint**:
Check the trusted wiki for missing links, orphan notes, stale claims, contradictions, duplicate concepts, and other maintenance issues.
