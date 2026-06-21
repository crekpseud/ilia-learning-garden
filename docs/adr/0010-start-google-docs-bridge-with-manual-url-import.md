# Start Google Docs bridge with manual URL import

The first Google Docs bridge will import a packet export from a user-provided Google Doc URL or file ID rather than watching a Drive folder. This proves the bridge and normalization workflow before adding Drive folder search, polling, or inbox automation.

**Considered Options**

- Watch a specific Google Drive folder.
- Search Drive by document title prefix.
- Use both folder and title prefix.
- Import a specific Google Doc URL or file ID.
- Import from manually downloaded local files.

**Consequences**

The MVP trigger remains explicit and simple: "import this Google Doc as a packet." Folder-based batch import can be added later without changing the packet export contract.
