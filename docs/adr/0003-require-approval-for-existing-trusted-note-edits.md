# Require approval for existing trusted note edits

The MVP may create new trusted notes after review approval, but changes to existing trusted notes must be presented as suggested patches and approved before being written. This preserves trust in the wiki while still allowing the system to identify connections, contradictions, and improvements.

**Considered Options**

- Allow only new note creation.
- Allow append-only updates to existing notes.
- Require approval for suggested patches to existing notes.
- Allow autonomous edits with Git history as the safety net.

**Consequences**

The first version needs a clear review surface for proposed changes, but it avoids silently mutating knowledge the user already accepted.
