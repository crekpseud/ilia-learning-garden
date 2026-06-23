# NotebookLM Source Manifest Prompt

Use this as the default first NotebookLM prompt after the user shares a notebook screenshot or notebook title. The goal is source provenance and rough orientation, not packet generation.

```markdown
Create a Source Manifest for this notebook.

Output only Markdown.
Do not wrap the answer in a code block.

# <Notebook Title>

## Notebook Snapshot

- Notebook title:
- Source count shown by NotebookLM:
- Notebook date shown, if visible:
- Source-access notes:

## Source List

For each source, use this exact shape:

### <Source Title>

- Author: <author or unknown>
- URL: <url or unknown>
- Source type: <web page / PDF / YouTube / Google Doc / uploaded file / copied text / unknown>
- Description: <1-2 sentences>
- Local access note: <public URL / private source / transcript source / uploaded file / unknown>

## Key Themes

- <theme or tension>
- <theme or tension>
- <theme or tension>

## Source Advantage Check

List any reasons NotebookLM may have source access or organization advantages over a local agent, such as YouTube transcripts, private Drive files, uploaded audio, uploaded PDFs/images, or a very large source set.

If there are no obvious source advantages, write:

No obvious NotebookLM-only source advantage detected.
```

## Local Agent Use

After receiving the manifest, the local agent should:

- preserve it under `learning/inbox/notebooklm/<slug>/source-manifest.md`
- check public or otherwise accessible sources directly
- decide whether local packet creation is sufficient
- fall back to full NotebookLM packet export only when NotebookLM has a meaningful source advantage
