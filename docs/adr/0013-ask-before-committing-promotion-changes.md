# Ask before committing promotion changes

Promotion may write approved files and present a diff summary, but the system will ask before creating a Git commit. This keeps Git history useful without making lifecycle transitions feel automatic or irreversible.

**Considered Options**

- Never commit automatically.
- Ask before committing promotion changes.
- Commit automatically after an explicit promote command.
- Commit every lifecycle transition.
- Keep Git entirely separate from the tool.

**Consequences**

Codex and future tooling can support commits as part of the workflow, but committing remains an explicit user-approved action.
