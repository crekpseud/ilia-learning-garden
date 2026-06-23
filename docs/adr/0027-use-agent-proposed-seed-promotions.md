# Use agent-proposed seed promotions

Agents may actively discover protocol improvements in a private working garden and propose public-safe seed promotions.

**Context**

Most protocol improvements will be discovered while using the private working garden: a prompt fails, a packet shape becomes awkward, a privacy rule needs tightening, or a new operation emerges from repeated practice.

Those discoveries are valuable to the public seed garden, but the surrounding private context often is not. The user wants agents to notice reusable protocol improvements and help apply them to the public checkout without leaking private material.

**Considered Options**

- Require the user to remember and manually copy every protocol improvement.
- Let agents automatically push private protocol changes to the public seed.
- Let agents scan the private garden and propose public-safe seed promotions for approval.
- Treat the private and public gardens as two-way synchronized peers.

**Decision**

Add agent-proposed seed promotion as an advisory workflow.

An agent operating in the private working garden may run a seed review and produce a proposal that identifies:

- protocol files that changed or should change
- repeated private workflow friction that suggests a public protocol improvement
- prompt/template improvements that are public-safe after redaction
- ADR or glossary changes that belong in the public seed
- example material that must be synthesized or sanitized before public use

The agent must not apply or push to the public seed automatically. It prepares a public-safe patch proposal. The user approves what crosses the boundary.

The allowed public seed surface is allowlist-based. Typical allowed targets are:

- `schema/`
- `docs/adr/`
- public-safe `CONTEXT.md`
- `AGENTS.md` and other portable agent entrypoints
- reusable prompt templates
- synthetic or public-source example packets
- public-safe starter wiki notes
- public seed planning docs

Private packet exports, raw personal sources, reading ledgers, Goodreads exports, human-contact reflections, private profile material, work notes, and personal logs do not cross the boundary unless the user explicitly writes a redacted public version.

**Consequences**

The public seed can improve from real use without becoming a leak of the private garden.

Agents become useful scouts for reusable protocol pressure, but the human remains the release gate for public seed changes.

The workflow adds a review step, but that cost is intentional. The boundary is not merely technical; it protects trust, privacy, and the social usefulness of the public seed.

Future tooling may automate detection and patch preparation, but the operation remains proposal-first and approval-gated.
