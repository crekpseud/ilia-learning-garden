# Import Repair

The preserved inbox export mostly satisfies the packet export contract, but it wraps valid existing wikilinks in backticks.

Local normalization repaired those links in packet drafts and source-derived artifacts by converting patterns like:

```markdown
`[[wiki/concepts/digital-garden|Digital Garden]]`
```

to:

```markdown
[[wiki/concepts/digital-garden|Digital Garden]]
```

The raw export remains unchanged at [[learning/inbox/notebooklm/evergreen-notes/packet-export]].
