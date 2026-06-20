# User Working Profile

## Project-Relevant Summary

### Remembered Facts

* Senior software engineer and aspiring architect with strong interest in systems thinking, knowledge representation, event-driven architectures, distributed systems, functional programming, learning science, and AI-assisted workflows.
* Heavy NotebookLM user. Frequently creates topic-focused notebooks, listens to Audio Overviews during walks, uses quizzes selectively, and increasingly treats AI as a learning amplifier rather than a search engine.
* Long-time Obsidian user with a strong preference for linked Markdown, local ownership of knowledge, and incremental refinement over polished publishing.
* Interested in architecture-as-code, topology-as-code, semantic graphs, WASM/component models, agentic skills, and reusable cognitive building blocks.

### Strong Inferences

* Sees knowledge systems as living ecosystems rather than document repositories.
* Wants a durable intellectual substrate that compounds over years.
* Values systems that increase understanding rather than merely generating content.

### Why This Project Matters

This project is an attempt to connect:

* Curiosity
* AI-mediated learning
* Human understanding
* Long-term knowledge accumulation

into a continuous feedback loop.

The goal is not note generation.

The goal is building a learning system that:

1. Helps acquire understanding.
2. Stores durable knowledge.
3. Uses accumulated knowledge to personalize future learning.

### Success Looks Like

* NotebookLM becomes the exploration layer.
* Obsidian becomes the trusted knowledge layer.
* AI helps move material between them.
* Human interaction acts as a quality gate.
* The knowledge graph becomes increasingly personalized and useful over time.
* Learning future topics becomes easier because the system understands existing knowledge.

---

## Learning Style

### How New Material Is Best Absorbed

Strong:

* Podcast-style explanations.
* Long-form conversational learning.
* NotebookLM Audio Overviews.
* Walking while listening.
* Conceptual connections between domains.
* Analogies.
* Historical context.
* Architecture-level understanding before details.

Moderately Useful:

* Quizzes.
* Flashcards.
* Diagrams.
* Structured summaries.

Less Effective:

* Pure memorization.
* Dense academic exposition without intuition.
* Large unstructured information dumps.

### Useful Friction

Useful:

* Listening to a topic before storing it.
* Quizzes.
* Reflection prompts.
* Explaining ideas back.
* Reviewing generated notes.
* Choosing links between concepts.

Annoying:

* Excessive manual tagging.
* Endless note maintenance.
* Repeated data entry.
* Bureaucratic workflows.
* Complex PKM rituals.

### Common Failure Pattern

Initial excitement
→ excessive system building
→ maintenance burden
→ abandonment

Design should optimize for:

* continuity
* low cognitive overhead
* gradual accumulation

not maximal structure.

---

## Knowledge Management Preferences

### Obsidian Philosophy

Obsidian is viewed as:

```text
human-readable semantic substrate
```

not:

```text
content warehouse
```

Preferred primitives:

* Markdown
* Wiki links
* Atomic notes
* Maps of Content
* Frontmatter
* Local files

### Preferred Knowledge Objects

* Concepts
* Patterns
* Theorems
* Architectures
* Historical ideas
* Mental models
* Connections between ideas

### Preferred Structures

Strong fit:

```text
raw/
learning/
wiki/
schema/
```

where:

* raw = immutable sources
* learning = active learning artifacts
* wiki = trusted knowledge
* schema = maintenance rules

### Content Sludge

Avoid:

* AI-generated notes with no human review.
* Massive summaries.
* Duplicate concepts.
* Orphan notes.
* Automatically generated "knowledge" not connected to understanding.

---

## Collaboration Style With AI

### Communication

Preferred:

* Architect-to-architect discussion.
* Conceptual clarity.
* Explicit tradeoffs.
* Strong reasoning.

Avoid:

* Marketing language.
* Excessive enthusiasm.
* Generic productivity advice.

### Challenge Level

AI should:

* challenge assumptions
* identify failure modes
* propose alternatives

without becoming adversarial.

### Decision Making

When uncertain:

* surface options
* explain tradeoffs
* recommend defaults

Do not repeatedly ask for confirmation on obvious implementation details.

### Summaries

Prefer:

* concise
* structural
* actionable

over exhaustive recaps.

---

## Technical And Workflow Context

### Known Tools

Strong confidence:

* Obsidian
* NotebookLM
* Anki
* C#
* .NET
* Azure
* Git
* Azure DevOps

Likely:

* Codex
* local scripting
* markdown processing
* automation pipelines

### Workflow Preferences

Strong fit:

* local-first
* plain text
* inspectable artifacts
* Git-friendly storage
* automation with review gates

Weak fit:

* opaque SaaS workflows
* proprietary formats
* hidden AI behavior

### Development Style

Prefers:

* incremental evolution
* architecture-first thinking
* abstraction discovery
* reusable pipelines

---

## Product Design Guidance

### Build For Daily Use

The system should feel like:

```text
learning companion
```

not:

```text
knowledge management project
```

### Strong Automation

Automate:

* parsing
* linking suggestions
* note generation
* metadata
* provenance
* MOC generation
* duplicate detection
* vault indexing

### Human Gates

Require human interaction before trusted ingestion.

Examples:

* listened to podcast
* passed quiz
* corrected summary
* accepted links
* wrote reflection

### Transparency

Everything should be:

* editable
* inspectable
* recoverable

Generated markdown should remain first-class.

---

## Risks And Failure Modes

### Overbuilding

Major risk.

Signs:

* complex schemas
* many note types
* excessive workflows
* automation before real usage

### Content Inflation

Danger:

```text
knowledge graph size
≠
understanding
```

The system must optimize for learning, not note count.

### Trust Erosion

Trusted vault should never become:

```text
LLM output archive
```

Human contact is required.

### Friction Extremes

Too little friction:

* low-quality knowledge

Too much friction:

* abandonment

The design challenge is finding the minimum useful gate.

---

## Implementation Advice For Codex

### Preferred Strategy

Build:

```text
simple
→ useful
→ observable
→ extensible
```

not:

```text
complete
→ theoretical
→ huge
```

### Recommended Early Milestones

1. NotebookLM import format.
2. Vault indexer.
3. Concept identity matching.
4. Safe note creation.
5. Safe note enrichment.
6. Provenance tracking.
7. Learning-state tracking.
8. Review gates.

### Useful Defaults

Assume:

* Markdown is canonical.
* Obsidian is source of truth.
* Existing notes should never be overwritten.
* Human review is preferred over automatic merging.

### Before Implementing Major Features

Ask:

* What user behavior does this support?
* What learning problem does this solve?
* What human action should validate it?

---

## Open Questions

### Important Unknowns

1. What exact learning gates should exist before wiki ingestion?

   * podcast completion?
   * quiz score?
   * reflection?
   * manual approval?

2. What is the canonical identity of a concept?

   * filename?
   * title?
   * aliases?
   * semantic similarity?

3. Should the system track learning state separately from knowledge state?

4. Should the trusted wiki be append-only or allow AI-assisted refactoring?

5. How much authority should agents have to modify existing notes?

6. Is the primary unit:

   * concept note
   * entity note
   * synthesis note
   * MOC
   * or all of the above?

7. How should future agentic skills integrate with the vault?

   * teach-me
   * challenge-me
   * connect-this
   * notebooklm-to-obsidian
   * architect-review

These skills may become first-class citizens of the system rather than separate tools.

