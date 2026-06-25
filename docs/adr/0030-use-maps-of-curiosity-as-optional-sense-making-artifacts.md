# Use maps of curiosity as optional sense-making artifacts

**Context**

Some learning sources are not source-heavy notebooks or single-topic articles. Long-running AI conversations, reading histories, Goodreads exports, and recurring personal questions can be valuable because they reveal a trajectory of curiosity.

If the protocol tries to reduce these materials immediately into synthesis notes and concept candidates, it can overfit to the final or most polished part of the source. The earlier trail may contain the more important signal.

**Considered Options**

- Treat every long conversation as a normal packet export.
- Ignore long conversation trails unless they contain a polished thesis.
- Add a required map step to every packet.
- Add `Map Of Curiosity` as an optional untrusted artifact.

**Decision**

Use `Map Of Curiosity` as an optional sense-making artifact for materials whose value is partly in their question trail.

The map may live in an inbox capture, in a normalized packet's `artifacts/` folder, or as a whole-garden review artifact when the map is not packet-specific.

It should identify recurring questions, curiosity trails, nearby trusted notes, and possible next packets. It must not promote knowledge, replace human contact, or become a required gate.

Template:

```text
schema/templates/map-of-curiosity.md
```

**Consequences**

The garden can preserve the shape of curiosity before forcing a topic into trusted notes.

This should help with long AI conversations, reading ledgers, Goodreads exports, and repeated work-session insights.

The risk is ritual overhead. Agents should use this artifact only when it clarifies learning direction or prevents loss of an important trail.
