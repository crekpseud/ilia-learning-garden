---
name: learning-garden-capture
description: Capture reusable insights from an AI-assisted work or learning session into a Markdown learning garden. Use when the user asks to capture a pattern, domain lesson, architectural insight, repeated decision, debugging lesson, or other reusable knowledge from the current session; or when an agent notices such an insight and should propose a safe inbox export without promoting it into trusted wiki.
---

# Learning Garden Capture

Use this skill to turn session-derived learning into an inbox packet export. The goal is capture, not promotion.

## Start

Read the garden entrypoints before writing:

- `AGENTS.md`
- `CONTEXT.md`
- `schema/README.md`
- `schema/packet-export-contract.md`
- `schema/packet-anatomy.md`

Respect these boundaries:

- `learning/inbox/` is the landing zone for new exports.
- `learning/packets/` is normalized packet workflow.
- `wiki/` is trusted knowledge and must not be changed by this skill.
- Work-garden knowledge must not be exported to a personal or public garden.

## When To Propose Capture

Propose a capture when the session reveals something likely to be reusable:

- a repeated implementation or architectural pattern
- domain knowledge the user may need again
- a debugging lesson or failure mode
- a naming, testing, or design heuristic
- a protocol improvement for the garden itself
- a question or concept that deserves later human reflection

Do not capture every interesting detail. Prefer fewer, higher-signal captures.

## Approval

Ask before writing unless the user explicitly enabled a capture mode for the session.

Good prompt:

```text
This looks reusable for the learning garden. Should I write a packet export to learning/inbox for later review?
```

If the user says yes, write an inbox export. If the user says no, do nothing.

## Export Location

Write exports under:

```text
learning/inbox/agent-captures/<slug>/packet-export.md
```

Use a short lowercase slug based on the insight title.

## Export Shape

Use the packet export contract shape so the capture can later be normalized into a learning packet.

```markdown
# <Insight Title>

## Source List

- Title: <session, task, issue, file, or source>
  Author: <user / agent / team / unknown>
  URL: <URL, local path, or not applicable>
  Description: <why this source produced the insight>

## Learning Summary

<Explain the reusable lesson in plain language.>

## Key Ideas

- <important point>
- <important point>
- <important point>

## Candidate Concept Notes

### <Concept Title>

- Status: new candidate / possible duplicate
- Definition:
- Why it matters:
- Possible aliases:
- Related existing notes:
- Promotion recommendation: yes / maybe / not yet
- If existing, suggested patch:

## Important Claims

- <claims that should be checked before promotion>

## Questions And Uncertainties

- <open questions>
- <risks or unclear boundaries>

## Suggested Trusted Wiki Output

- one synthesis note title: <plain title>
- zero or more concept notes worth promoting: NEW CANDIDATE: <title>
- suggested patches to existing notes: <only if relevant>
- potential future notes: NEW CANDIDATE: <title>

## Human-Contact Artifact

MISSING: human-contact artifact required before promotion.
```

If the user provides a reflection, correction, or teach-back while approving capture, include it under `Human-Contact Artifact` instead of the missing marker.

## Local Reconciliation Rules

- Link only to existing trusted notes that are actually present in the garden.
- Keep new concepts as candidates; do not create trusted concept notes.
- Write suggested patches instead of editing `wiki/`.
- Preserve uncertainty. If a claim came from debugging intuition, mark it as a claim, not a fact.
- Avoid copying secrets, credentials, private customer data, proprietary code, or restricted work knowledge into a garden that may leave that environment.

## Finish

After writing the export:

- Tell the user the inbox path.
- State that promotion is blocked until the packet is normalized, human contact is completed, and promotion review is approved.
- Do not commit unless the user asks.
