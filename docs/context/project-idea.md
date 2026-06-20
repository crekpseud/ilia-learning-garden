# Project Idea: AI-Augmented Learning Pipeline

## One-Sentence Vision

Build a local-first learning system that turns curiosity into durable, trusted Obsidian knowledge through AI-mediated learning, explicit human friction, and incremental wiki maintenance.

## Core Loop

```text
curiosity
-> source gathering
-> AI-mediated learning experience
-> human ingestion gate
-> trusted Obsidian knowledge
-> personalized future AI context
-> deeper curiosity
```

The project should help knowledge compound without turning the vault into an archive of unreviewed AI summaries.

## Motivation

The current learning workflow is already energizing:

- Capture several topics per day worth exploring.
- Use NotebookLM to gather sources and generate Audio Overviews.
- Listen while walking, biking, or resting.
- Sometimes use quizzes to reinforce understanding.

The missing step is persistence. After becoming familiar with a topic, the knowledge should enter a personal knowledge base in a structured, linked, queryable, and trustworthy form.

## Guiding Principle

The LLM may draft, connect, refactor, and maintain knowledge, but only human contact can promote material into trusted knowledge.

Human contact can include:

- listening to an Audio Overview
- passing or attempting a quiz
- correcting an AI-generated summary
- explaining the idea back
- choosing or approving links
- writing a reflection
- manually approving ingestion

The gate should be real enough to protect trust, but lightweight enough to support daily use.

## Conceptual Foundation

This project adapts Karpathy's LLM Wiki pattern:

```text
raw sources -> LLM-maintained markdown wiki -> schema-guided maintenance
```

The important extension is an explicit learning layer:

```text
raw sources
-> learning artifacts and human-contact state
-> trusted wiki
-> schema, logs, and maintenance rules
```

Karpathy's pattern treats the LLM as the maintainer of a persistent markdown wiki. This project keeps that idea, but adds a distinction between generated knowledge and personally touched knowledge.

## Proposed Knowledge Layers

### Raw

Immutable source materials.

Examples:

- clipped articles
- PDFs
- copied NotebookLM source exports
- transcripts
- source metadata
- links and bibliographic information

The LLM can read raw materials but should not modify them.

### Learning

Artifacts and state from the active learning process.

Examples:

- NotebookLM notebook/topic metadata
- podcast or Audio Overview status
- quiz prompts and results
- reflection answers
- generated draft summaries
- candidate links
- learning session logs
- review state

This layer records whether the user actually interacted with the material.

### Wiki

Trusted Obsidian knowledge.

Examples:

- concept notes
- entity notes
- synthesis notes
- maps of content
- comparison notes
- learning trails
- maintained indexes

This layer should be useful both to the human and to future LLM sessions.

### Schema

Rules and instructions that make the system maintainable.

Examples:

- note templates
- frontmatter conventions
- ingestion workflow
- review gate rules
- linking rules
- provenance conventions
- linting checks
- agent behavior rules

This layer should evolve with usage, not be overdesigned upfront.

## Product Shape

The system should feel like a learning companion, not a knowledge management project.

It should automate:

- parsing and normalization
- draft note creation
- provenance tracking
- candidate link discovery
- duplicate detection
- index and MOC updates
- wiki health checks

It should require human involvement for:

- promoting knowledge into the trusted wiki
- accepting important links
- resolving ambiguous concepts
- approving modifications to existing trusted notes
- deciding when a learning episode is complete enough

## Initial Use Case

Populate a fresh Obsidian vault with notes based on knowledge currently stored in NotebookLM notebooks.

The first version may not require a deep NotebookLM integration. A manual or semi-manual import path is acceptable if it lets the project validate the core learning loop.

Possible early inputs:

- NotebookLM-generated summaries
- Audio Overview notes or transcripts, if available
- copied quiz output
- source lists
- manually exported source files
- user reflections

Possible early outputs:

- draft learning packet
- candidate Obsidian notes
- proposed links to existing notes
- provenance metadata
- review checklist
- final integrated wiki notes

## Candidate Workflow

1. Create or select a learning topic.
2. Add sources or NotebookLM-derived artifacts.
3. Generate a learning packet.
4. Complete a human-contact gate.
5. Review draft notes and candidate links.
6. Promote approved material into the trusted wiki.
7. Update indexes, maps of content, and logs.
8. Use the updated vault as context for future learning.

## Key Design Tensions

### Automation vs Trust

Too little automation makes the system feel like chores. Too much automation turns the vault into untrusted AI output.

### Friction vs Continuity

Too little friction weakens learning. Too much friction risks abandonment.

### Structure vs Evolvability

The system needs enough structure for agents to maintain it, but not enough ceremony to become a PKM tax.

### Local-First vs External Integrations

Obsidian and Markdown should remain canonical. NotebookLM integration may be valuable, but should not make the core system dependent on opaque APIs or fragile exports too early.

### Wiki Maintenance vs Human Ownership

The LLM can maintain cross-links, indexes, and summaries, but the user must remain able to inspect, edit, and override everything.

## Early Architecture Hypothesis

```text
vault/
  raw/
  learning/
  wiki/
  schema/
  index.md
  log.md
```

Or, if this lives as tooling around an existing Obsidian vault:

```text
obsidian-vault/
  00-system/
    schema/
    logs/
  10-raw/
  20-learning/
  30-wiki/
```

This should remain provisional until the grilling and planning phases.

## Near-Term Milestones

1. Define the domain model: topics, sources, learning packets, notes, concepts, gates, provenance, and promotion.
2. Decide the minimal trusted ingestion workflow.
3. Define a small Markdown/frontmatter schema.
4. Build a vault indexer that can read existing notes.
5. Build a learning packet importer from manual NotebookLM-style inputs.
6. Generate draft notes with provenance and candidate links.
7. Add a review gate before writing to the trusted wiki.
8. Add a log and basic wiki health checks.

## Non-Goals For The First Version

- Fully automatic NotebookLM synchronization.
- Complex spaced repetition system.
- Heavy database-backed PKM platform.
- Perfect semantic deduplication.
- Fully autonomous vault rewriting.
- Large UI before validating the workflow.

## Open Questions

1. What exact human-contact gates are required before trusted ingestion?
2. What is the first acceptable NotebookLM import format?
3. Should learning state live inside Obsidian, beside Obsidian, or in a separate project directory?
4. What is the canonical identity of a concept: filename, title, aliases, frontmatter ID, or semantic match?
5. What note types are necessary for the first version?
6. How much authority should the LLM have to edit existing notes?
7. Should the system optimize first for populating a fresh vault or augmenting an existing one?
8. What does a successful daily workflow feel like in five minutes or less?
9. What should the system do when a new source contradicts existing trusted notes?
10. How should future AI sessions retrieve and use the trusted vault as personalized context?

## Working Name Ideas

- Learning Pipeline
- Living Wiki
- Mycelium
- Learning Loop
- Obsidian Learning Compiler
- Knowledge Metabolism

## Current Best Framing

This project is a local-first learning loop for turning AI-assisted exploration into trusted, linked Markdown knowledge.

It should preserve the joy of NotebookLM-style learning while adding the missing durable memory layer: an Obsidian wiki that grows only through reviewed, human-touched knowledge.
