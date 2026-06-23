# Learning Pipeline

A local-first learning system that turns AI-mediated exploration into trusted Obsidian knowledge through explicit human contact and maintained Markdown artifacts.

## Language

**Learning Loop**:
The smallest complete cycle from choosing a topic through learning it, passing a human-contact gate, and integrating approved knowledge into the trusted wiki.
_Avoid_: Import flow, note generation pipeline

**Vault Population Loop**:
The concrete MVP path that turns a learned topic or NotebookLM-derived material into reviewed Obsidian notes.
_Avoid_: Bulk import, migration

**Learning Packet**:
A deliberately assembled input bundle for one learning topic or episode, containing the topic, source references or materials, AI-derived artifacts, at least one human-contact artifact, and optional integration guidance.
_Avoid_: Notebook, import, source bundle

**Packet Manifest**:
The `packet.md` file that names the packet topic, status, source tool, creation date, packet export location, and integration focus.
_Avoid_: Packet index, metadata file

**Source Record**:
The `sources.md` file that lists the source material, references, URLs, attachments, and source provenance behind a learning packet.
_Avoid_: Bibliography, citation file

**Learning Evidence File**:
The `human-contact.md` file that records the human-contact artifact required before promotion.
_Avoid_: Completion note, engagement file

**Promotion Decision File**:
The `review.md` file that records which drafts, concept candidates, and suggested patches are approved or rejected for promotion.
_Avoid_: Checklist, approval note

**Packet Export**:
A portable Markdown artifact produced by an external learning or synthesis tool that can be normalized into a learning packet. It uses fixed headings and optional YAML frontmatter so it remains readable and parseable.
_Avoid_: NotebookLM output, pasted response

**Source Manifest**:
A compact Markdown artifact produced by an external tool that lists the notebook topic, source titles, URLs, descriptions, and optional key themes. It is used for provenance and local source checking, not as a draft trusted note.
_Avoid_: Packet export, bibliography, source dump

**Packet Export Contract**:
The fixed-heading Markdown shape that packet exports must follow before a bridge can normalize them into learning packets.
_Avoid_: Prompt output, import format

**Prompt Template**:
A reusable Markdown prompt that teaches an external LLM how to produce a packet export without hard-coding one packet's temporary context.
_Avoid_: One-off prompt, chat text

**Prompt Source Artifact**:
A Markdown or Google Docs source added to NotebookLM or another external LLM workspace so large, stable instructions can be grounded as source material instead of pasted into the chat prompt.
_Avoid_: Giant chat prompt, hidden context

**Garden Meta-Source ID**:
An internal marker line placed at the top of a copied-text NotebookLM source so prompts can identify the source by content instead of NotebookLM's generated filename.
_Avoid_: NotebookLM filename, source title

**NotebookLM Copy-Text Setup**:
The three-text setup for a NotebookLM packet export: copy in the packet export contract, copy in the topic-specific vault context slice, then paste a run prompt that refers to both by Garden Meta-Source ID.
_Avoid_: File upload requirement, filename-dependent setup

**Run Prompt**:
A short chat prompt that tells an external LLM which prompt source artifacts and notebook sources to use for the current export.
_Avoid_: Full protocol prompt, source dump

**Agent Compatibility Layer**:
Small repository instruction files that teach non-Codex agents how to navigate and operate the Markdown garden without making any one agent the protocol authority.
_Avoid_: Tool lock-in, hidden agent memory

**Vault Context Injection**:
The packet-specific act of adding relevant current vault notes, protocol principles, and human-contact material into a prompt template before sending it to an external LLM.
_Avoid_: Static prompt, global context

**Vault Context Slice**:
The topic-specific subset of trusted notes, aliases, protocol principles, and suggested-patch targets injected into an external LLM prompt for one learning packet.
_Avoid_: Whole-vault dump, global memory

**Local Reconciliation**:
The local protocol step that compares an external packet export with the current vault, resolves existing concepts versus new candidates, and turns advisory output into reviewable packet artifacts.
_Avoid_: Blind import, external promotion

**Bridge**:
An adapter that brings packet exports from an external tool or storage location into the learning area without making that external tool part of the core model.
_Avoid_: Integration, sync

**Manual NotebookLM Import**:
The first NotebookLM bridge mode, where the user manually pastes a NotebookLM packet export into the inbox and the local protocol normalizes it into a learning packet.
_Avoid_: NotebookLM sync, direct NotebookLM integration

**Source-Manifest-First NotebookLM Bridge**:
The preferred NotebookLM bridge mode where NotebookLM produces a Source Manifest and learning media, while the local agent checks sources and creates the garden-aware packet against the whole vault.
_Avoid_: Full packet export by default, NotebookLM-as-wiki-writer

**Codex Source Pass**:
The local agent step that inspects relevant sources from a Source Manifest before drafting or promoting garden knowledge. It verifies provenance, checks key claims, and decides whether NotebookLM has a source-access advantage that justifies fallback.
_Avoid_: Blind import, mandatory exhaustive reading

**Full NotebookLM Packet Fallback**:
The fallback bridge mode where NotebookLM is asked to produce a full Packet Export because it has source access or organization advantages the local agent lacks.
_Avoid_: Default NotebookLM packet generation

**Bridge Preparation Area**:
The `learning/bridge/` area where locally prepared artifacts for external tools live before they are sent out, such as NotebookLM context slices and run materials.
_Avoid_: Inbox, trusted wiki, schema template

**Inbox**:
The `learning/inbox/` area where external tool outputs land before local normalization.
_Avoid_: Bridge preparation, generated source material

**Downstream Work Garden**:
A restricted fork of the garden that may receive personal-garden protocol and public knowledge updates, but must never export work knowledge back to the personal garden.
_Avoid_: Two-way sync, shared work/personal garden

**Public Seed Garden**:
A public, reusable starter garden containing protocol, schemas, ADRs, agent instructions, prompt templates, public-safe examples, and a small starter wiki.
_Avoid_: Public copy of the private garden, sanitized branch

**Private Working Garden**:
The lived garden where day-to-day learning happens, including private sources, human-contact artifacts, reading ledgers, personal context, and unfinished packets.
_Avoid_: Public seed, shared starter kit

**Seed Promotion**:
The approval-gated act of moving a public-safe protocol improvement or starter artifact from a private working garden into the public seed garden.
_Avoid_: Sync, mirror, automatic publish

**Public-Safe Patch**:
A patch that is intentionally prepared for the public seed garden and contains no private packet exports, personal reflections, reading ledgers, work material, or hidden personal context.
_Avoid_: Best-effort redaction, private diff

**Private Garden Material**:
Any material that belongs only in a private working garden by default, including human-contact reflections, private source exports, reading history, personal profile material, and work-related knowledge.
_Avoid_: Seed content, example data

**Google Docs Bridge**:
The first bridge, which imports a packet export from a specific Google Doc URL or file ID and normalizes it into a learning packet.
_Avoid_: Drive sync, NotebookLM integration

**Import Repair**:
An explicit LLM-assisted step that reshapes a malformed packet export into the packet export contract after validation fails.
_Avoid_: Best-effort import, silent cleanup

**Import Quality Tier**:
The local classification assigned to an external packet export after validation: `strict-valid`, `repairable`, or `rejected`.
_Avoid_: Prompt success, model quality

**Repairable Packet Export**:
A malformed packet export that fails the strict contract but contains enough topic, source, synthesis, concept, and human-contact information for explicit local repair without inventing the learning material.
_Avoid_: Valid packet, good-enough output

**Learning Area**:
The untrusted part of the Obsidian vault where learning packets, draft notes, reflections, quiz results, and review state live before promotion.
_Avoid_: Inbox, staging database, temp folder

**Promotion**:
The act of moving reviewed knowledge from a learning packet into the trusted wiki after the human-contact gate has passed.
_Avoid_: Import, sync, publish

**Promotion Review**:
A Markdown review record for a learning packet that captures whether the synthesis note, concept notes, and suggested patches are approved for promotion.
_Avoid_: Chat approval, final check

**Gardening Review**:
An agent-authored sense-making review that asks what a packet or promotion means for the whole garden: unexpected links, emerging narratives, protocol pressure, next learning paths, and possible drift or over-optimization.
_Avoid_: Import validation, promotion checklist

**Gardening Proposal**:
A non-binding suggestion from an agent after gardening review, such as a next learning topic, a protocol adjustment, a link to inspect, a warning about drift, or a maintenance task.
_Avoid_: Automatic promotion, command

**Knowledge Gardener**:
A person or agent who shapes conditions for knowledge growth through planting, pruning, linking, tending, and harvesting rather than imposing a rigid hierarchy.
_Avoid_: Taxonomist, curator, file clerk

**Playful Knowledge Practice**:
The principle that a knowledge system should preserve play, curiosity, and lightness so that learning remains sustainable rather than becoming self-optimization ritual.
_Avoid_: Gamification for its own sake, productivity system, streak engine

**Suggested Patch**:
A proposed change to an existing trusted wiki note that must be reviewed before it is applied.
_Avoid_: Auto-update, rewrite

**Source-List Provenance**:
The minimum provenance record for promoted notes, linking back to the learning packet and listing the original source URLs or file paths.
_Avoid_: Full citation graph, bibliography

**Claim-Level Citation**:
A precise citation attached to a specific claim when the claim is surprising, factual, numeric, controversial, or likely to be challenged.
_Avoid_: Universal citation requirement

**Synthesis Note**:
A trusted wiki note that captures the reviewed understanding of one learning packet or topic.
_Avoid_: Summary, article note

**Concept Note**:
A trusted wiki note for a reusable idea that is expected to matter beyond a single learning packet.
_Avoid_: Atomic note, keyword page

**Candidate Concept Note**:
A concept note suggested by a packet export or drafting step that has not yet been promoted into the trusted wiki.
_Avoid_: Atomic note output, generated concept

**Concept Recognition**:
The agent-assisted act of noticing that packet material refers to an existing concept or may introduce a reusable new concept.
_Avoid_: Concept promotion, automatic tagging

**Concept Promotion**:
The human-approved act of turning a candidate concept note into a trusted concept note.
_Avoid_: Auto-create concept, extract concept

**Draft Link**:
A link to an existing trusted concept that an agent may place in draft material before promotion review.
_Avoid_: Trusted edit, promoted link

**Suggested Trusted Wiki Output**:
Draft synthesis, concept, or patch content proposed by a packet export or drafting step before promotion review.
_Avoid_: Final notes, generated wiki

**Canonical Title**:
The human-readable title used as the primary identity for a trusted wiki note.
_Avoid_: ID, slug

**Alias**:
An alternate name for a trusted wiki note that helps humans and agents recognize equivalent phrasing.
_Avoid_: Synonym list, keyword

**Human-Contact Gate**:
The rule that knowledge cannot enter the trusted wiki until the user produces or approves at least one explicit human-contact artifact.
_Avoid_: Approval checkbox, review step

**Human-Contact Artifact**:
A small record showing the user personally interacted with the material, such as a reflection, quiz result, correction, teach-back explanation, or approved link choice.
_Avoid_: Completion flag, engagement metric

**Pending Human Contact**:
The state of a learning packet that has enough imported material to draft notes, but cannot be promoted because no human-contact artifact exists yet.
_Avoid_: Incomplete import, blocked packet

**Captured**:
The learning packet state where a topic exists, but packet material is not complete enough to import or draft.
_Avoid_: Idea, todo

**Imported**:
The learning packet state where packet export or source material exists in the learning area.
_Avoid_: Synced, downloaded

**Drafted**:
The learning packet state where suggested trusted wiki output exists but is not yet ready or approved for promotion.
_Avoid_: Generated, processed

**Ready For Review**:
The learning packet state where the human-contact gate has passed and drafts are ready for promotion review.
_Avoid_: Done, complete

**Promoted**:
The learning packet state where approved knowledge has entered the trusted wiki.
_Avoid_: Published, synced

**Trusted Wiki**:
The part of the Obsidian vault that contains reviewed, human-touched knowledge intended for future human use and AI context.
_Avoid_: Notes folder, generated wiki

**Markdown Codebase**:
The Obsidian vault treated as the durable system of record, where Markdown files are the canonical design surface for humans, LLMs, and tools. Non-Markdown attachments may exist when referenced and contextualized by Markdown records.
_Avoid_: Content folder, notes repository

**Attachment**:
A non-Markdown file kept in the vault to support a Markdown record, such as a PDF, image, audio file, CSV, or exported artifact.
_Avoid_: Primary source of truth, opaque blob

**Attachment Area**:
The `raw` or `learning` location where attachments may live. Trusted wiki notes link to attachments but do not store them nearby.
_Avoid_: Wiki assets, note attachments

**Markdown Record**:
A Markdown file that provides the canonical context, metadata, provenance, and links for a source, attachment, learning packet, or trusted note.
_Avoid_: Metadata sidecar, note wrapper

**Protocol-First Structure**:
A vault layout where core protocol folders such as `schema`, `learning`, `raw`, and `wiki` live at the repository root instead of being hidden under app-specific or documentation folders.
_Avoid_: App project, plugin folder

**Topographical Reading**:
The principle that trusted knowledge should be navigated through meaning, links, maps, concepts, and trails rather than reverse chronology.
_Avoid_: Feed, timeline

**Append-Only Process History**:
The principle that important workflow events such as imports, drafts, promotions, corrections, and rejected patches are recorded as new chronological entries instead of rewriting the process record.
_Avoid_: Activity feed, mutable history

**Patch-Based Knowledge Change**:
The principle that existing trusted notes evolve through reviewed patches that keep the current note readable while preserving semantic history in packet reviews, suggested patches, logs, and Git.
_Avoid_: Silent rewrite, event-only projection
