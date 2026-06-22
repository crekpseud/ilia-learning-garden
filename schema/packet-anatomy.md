# Packet Anatomy

Each learning packet lives under:

```text
learning/packets/<slug>/
  packet.md
  sources.md
  human-contact.md
  review.md
  drafts/
    synthesis.md
    concepts.md
    patches.md
  artifacts/
    gardening-review.md
```

## Files

**packet.md**:
The packet manifest. Names the topic, status, source tool, creation date, packet export location, and desired integration focus.

**sources.md**:
The source record. Lists source material, URLs, attachments, source provenance, and references behind the packet.

**human-contact.md**:
The learning evidence file. Records the explicit human-contact artifact required before promotion.

**review.md**:
The promotion decision file. Records what is approved or rejected for promotion.

**drafts/synthesis.md**:
Candidate synthesis note for the trusted wiki.

**drafts/concepts.md**:
Candidate reusable concept notes for the trusted wiki.

**drafts/patches.md**:
Suggested patches to existing trusted wiki notes.

**artifacts/**:
Packet-specific attachments and bridge artifacts.

Packet-specific artifacts are materials attached to an already-normalized packet. Cross-packet or pre-packet bridge inputs belong in `learning/bridge/`.

**artifacts/gardening-review.md**:
Optional but recommended agent-authored sense-making review. It records what this packet means in the context of the whole garden, including unexpected links, emerging narratives, next learning paths, protocol pressure, and possible drift.
