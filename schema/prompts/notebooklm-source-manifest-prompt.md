# NotebookLM Source Manifest Prompt

Use this as a diagnostic NotebookLM prompt when source provenance, blocked sources, URL recovery, duplicate entries, or packet export quality need investigation. It is not the default packet creation flow.

For normal source-heavy NotebookLM ingestion, use the three-text packet export setup: packet export contract, vault context slice, and run prompt. The goal there is to let NotebookLM digest its full source set and produce a Packet Export for local reconciliation.

The prompt is provenance-aware, not provenance-absolutist. It should expose what NotebookLM can see, label weak provenance honestly, and give the local agent enough information to recover public URLs by search when possible.

```markdown
Create a Source Manifest for this notebook.

Your job is source provenance, not synthesis.

Output only Markdown.
Do not wrap the answer in a code block.
Do not create a learning packet.
Do not suggest trusted wiki notes.
Do not recommend concept promotion.
Do not infer or guess URLs from source titles, domains, authors, or your general knowledge.
Use only source metadata and source content that are actually visible in this notebook.

Required notebook:
- Title: <Notebook Title>
- Source count shown by NotebookLM: <Source Count>
- Notebook date shown, if visible: <Notebook Date>

Create the full manifest even when some exact URLs are not visible. Do not stop at preflight unless there are zero usable sources.

For web pages and YouTube sources, an exact original URL is required.
For uploaded files, an exact filename is required and URL should be `not applicable - uploaded file`.
For copied text, URL should be `not applicable - copied text`.
For private Google Drive files, URL should be the visible Drive URL if available; otherwise write `not visible to NotebookLM`.

For every source, include a URL visibility field:

- `exact` when the exact original URL is visible
- `domain-only` when only a domain or site name is visible
- `not-visible` when no URL is visible
- `not-applicable` for uploaded files or copied text

If a URL is not exact, do not guess. Preserve the best visible clue in `URL clue` so the local agent can search.

If there are zero usable learning sources, return only this NOT READY shape:

# Source Manifest Preflight

## Readiness

NOT READY: no usable learning sources were found.

## Reason

- <reason>

Otherwise, create the manifest below.

# <Notebook Title>

## Notebook Snapshot

- Notebook title: <Notebook Title>
- Source count shown by NotebookLM: <Source Count>
- Source count listed in this manifest: <count>
- Notebook date shown, if visible: <Notebook Date or unknown>
- Provenance status: <complete / partial / weak>
- Exact URL count: <count>
- Recoverable-by-search count: <count>
- Manual-source-needed count: <count>

## Source List

For every source in the notebook, use this exact shape:

### <Source Title>

- Author: <author or unknown>
- URL: <exact URL / not applicable - uploaded file / not applicable - copied text / not visible to NotebookLM>
- URL visibility: <exact / domain-only / not-visible / not-applicable>
- URL clue: <visible domain, site name, source title clue, YouTube channel, or not applicable>
- Source type: <web page / PDF URL / YouTube / Google Doc / uploaded PDF / uploaded audio / uploaded image / uploaded file / copied text / unknown>
- Exact filename, if uploaded: <filename or not applicable>
- Source import status: <usable / blocked by Cloudflare / access blocker imported / transcript source / uploaded file / copied text / unknown>
- Local access note: <public URL / private source / transcript source / uploaded file / copied text / not locally accessible / unknown>
- Local recovery action: <Codex can search public web / user should provide URL / use NotebookLM transcript / use uploaded file only / none>
- Description: <1-2 sentences>

If a source title or content is an access blocker such as "Just a moment...", "Access denied", "Checking your browser", "Cloudflare", or a login wall, mark:
- Source import status: access blocker imported
- Local access note: source should be replaced or manually provided

## Key Themes

List 5-10 key themes or tensions across the usable sources.

- <theme or tension>
- <theme or tension>
- <theme or tension>

## Source Advantage Check

List any reasons NotebookLM may have source access or organization advantages over a local agent, such as YouTube transcripts, private Drive files, uploaded audio, uploaded PDFs/images, copied-text sources, or a very large source set.

If there are no obvious NotebookLM-only source advantages, write:

No obvious NotebookLM-only source advantage detected.

## Local Packet Recommendation

Choose exactly one:

- LOCAL PACKET READY: Codex can likely inspect the sources and create the packet locally.
- PACKET EXPORT NEEDED: NotebookLM has source access advantages that Codex likely cannot reproduce.
- MANUAL SOURCE FIX NEEDED: Some source URLs or source files need to be provided manually first.

## Recovery Checklist

List only sources that need follow-up:

- <source title> - <Codex can search / user should provide URL / replace blocked source / use NotebookLM transcript / uploaded file only>
```

## Local Agent Use

After receiving the manifest, the local agent should:

- reject `NOT READY` output as an incomplete manifest, not as a packet input
- preserve ready manifests under `learning/inbox/notebooklm/<slug>/source-manifest.md`
- check public or otherwise accessible sources directly
- recover public URLs by searching source titles when URL visibility is `domain-only` or `not-visible`
- decide whether local packet creation is sufficient
- rerun the normal NotebookLM packet export prompt when NotebookLM has a meaningful source advantage or the manifest shows the local agent would be doing unnecessary heavy digestion
