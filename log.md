# Log

Append-only chronological log of bridge imports, packet creation, promotions, lint passes, and major maintenance actions.

## [2026-06-21] packet.create | LLM Wiki Pattern

Created the first protocol-only learning packet at [[learning/packets/llm-wiki-pattern/packet]] using [[docs/research/karpathy-llm-wiki]] as the source.

## [2026-06-21] packet.draft | LLM Wiki Pattern

Drafted synthesis, candidate concepts, and suggested patches for [[learning/packets/llm-wiki-pattern/packet]].

## [2026-06-21] packet.promote | LLM Wiki Pattern

Promoted the approved synthesis note to [[wiki/synthesis/llm-wiki-pattern]] and updated [[index]].

## [2026-06-21] packet.create | Digital Garden Ethos

Created draft packet [[learning/packets/digital-garden-ethos/packet]] from [[raw/sources/digital-garden-ethos]].

## [2026-06-21] packet.draft | Digital Garden Ethos

Drafted synthesis, candidate concepts, and a suggested patch for [[learning/packets/digital-garden-ethos/packet]]. The packet remains blocked from promotion pending a human-contact artifact.

## [2026-06-21] packet.review | Digital Garden Ethos

Recorded the human-contact artifact for [[learning/packets/digital-garden-ethos/packet]] from the user's NotebookLM podcast listening notes and reflection. Updated the packet to ready-for-review.

## [2026-06-21] packet.promote | Digital Garden Ethos

Promoted [[wiki/synthesis/digital-garden-ethos]] and [[wiki/concepts/digital-garden]] from [[learning/packets/digital-garden-ethos/packet]], and applied the approved patch to [[wiki/synthesis/llm-wiki-pattern]].

## [2026-06-21] bridge.notebooklm.manual-import | Knowledge Gardening

Preserved manual NotebookLM packet export at [[learning/inbox/notebooklm/knowledge-gardening/packet-export]].

## [2026-06-21] packet.create | Knowledge Gardening

Normalized the manual NotebookLM export into [[learning/packets/knowledge-gardening/packet]]. The packet is blocked from promotion pending a human-contact artifact.

## [2026-06-21] packet.draft | Knowledge Gardening

Drafted synthesis, candidate concepts, and suggested patches for [[learning/packets/knowledge-gardening/packet]]. Local concept recognition corrected NotebookLM's `Digital Garden` candidate to an existing trusted concept.

## [2026-06-21] packet.review | Knowledge Gardening

Recorded human-contact artifact for [[learning/packets/knowledge-gardening/packet]] from the user's NotebookLM podcast and draft-review reflection. Updated the packet to ready-for-review and captured the need for topic-specific vault context slices in external LLM prompts.

## [2026-06-21] packet.promote | Knowledge Gardening

Promoted [[wiki/synthesis/technopastoral-synthesis]] and [[wiki/concepts/the-stream]] from [[learning/packets/knowledge-gardening/packet]]. Applied approved patches to [[wiki/concepts/digital-garden]] and [[wiki/synthesis/digital-garden-ethos]]. Deferred Evergreen Note, Bi-directional Linking, and Epistemic Status.

## [2026-06-21] protocol.decision | Knowledge Gardening Import

Recorded the protocol lessons from the manual NotebookLM experiment: use topic-specific vault context slices, reconcile external packet exports locally, and keep manual NotebookLM import as a first-class bridge while sync automation is deferred.

## [2026-06-22] protocol.decision | NotebookLM Prompt Split

Recorded the decision to feed NotebookLM stable packet-export instructions and vault context as sources, then use a short run prompt in chat when the monolithic prompt is too large.

## [2026-06-22] protocol.decision | Bridge Input Area

Recorded the decision to store locally prepared bridge inputs in `learning/bridge/` and keep `learning/inbox/` for external tool outputs.

## [2026-06-22] protocol.maintenance | NotebookLM Contract Hardening

Tightened NotebookLM prompt sources after an Evergreen Notes export lost Markdown heading markers and invented a synthesis wikilink. Added literal Markdown requirements, candidate concept heading requirements, and a repair prompt.

## [2026-06-22] protocol.maintenance | NotebookLM Copy-Paste Findings

Recorded that direct NotebookLM copy-paste preserves Markdown structure better than Google Docs export, and added prompt rules requiring plain wikilinks instead of backticked wikilinks.

## [2026-06-22] bridge.notebooklm.manual-import | Evergreen Notes

Preserved direct NotebookLM packet export at [[learning/inbox/notebooklm/evergreen-notes/packet-export]]. The raw export preserves the model output, including backticked wikilinks.

## [2026-06-22] packet.create | Evergreen Notes

Normalized the direct NotebookLM export into [[learning/packets/evergreen-notes/packet]]. The packet is blocked from promotion pending a human-contact artifact.

## [2026-06-22] packet.draft | Evergreen Notes

Drafted synthesis, candidate concepts, suggested patches, and an import repair note for [[learning/packets/evergreen-notes/packet]]. Local repair removed backticks around valid existing wikilinks in normalized packet artifacts.

## [2026-06-22] packet.capture | Mastering the Architecture of Original Thought

Created captured packet scaffold [[learning/packets/architecture-of-original-thought/packet]] from a user-provided NotebookLM notebook screenshot. The packet is pending strict NotebookLM packet export and human contact.

## [2026-06-22] bridge.notebooklm.prepare | Architecture of Original Thought

Prepared [[learning/bridge/notebooklm/context-slices/architecture-of-original-thought]] and [[learning/bridge/notebooklm/run-prompts/architecture-of-original-thought]] so NotebookLM can generate a strict packet export for local reconciliation.

## [2026-06-22] bridge.notebooklm.manual-import | Architecture of Original Thought

Preserved direct NotebookLM packet export at [[learning/inbox/notebooklm/architecture-of-original-thought/packet-export]]. The export did not satisfy the strict packet export contract and required explicit local repair.

## [2026-06-22] packet.draft | Architecture of Original Thought

Normalized the repaired NotebookLM export into [[learning/packets/architecture-of-original-thought/packet]]. Drafted synthesis, candidate concepts, suggested patches, and an import repair note. The packet is blocked from promotion pending a human-contact artifact.

## [2026-06-22] protocol.maintenance | NotebookLM Heading Self-Check

Hardened [[schema/prompts/notebooklm-run-prompt]] after the Architecture of Original Thought export passed preflight but still renamed or omitted required headings. Added a final instruction asking NotebookLM to compare output headings against the contract before sending.

## [2026-06-22] protocol.decision | Import Quality Tiers

Recorded [[docs/adr/0023-classify-external-packet-exports-by-import-quality]] after the Architecture of Original Thought export showed that NotebookLM can pass meta-source preflight but still fail strict structure. Added `strict-valid`, `repairable`, and `rejected` import quality tiers to [[schema/manual-notebooklm-import]] and [[schema/packet-export-contract]].

## [2026-06-22] protocol.decision | NotebookLM Embedded Meta-Source IDs

Recorded [[docs/adr/0024-use-embedded-meta-source-ids-for-notebooklm-copy-text]] after deciding that NotebookLM copy-text sources should be identified by `GARDEN_META_SOURCE_ID` markers instead of generated filenames. Updated [[schema/prompts/notebooklm-contract-source]], [[schema/prompts/vault-context-slice-template]], [[schema/prompts/notebooklm-run-prompt]], and [[schema/prompt-design]] so future notebook ingestion setup produces three copyable texts: contract, context slice, and prompt.

## [2026-06-22] packet.capture | David West Object Thinking

Created captured packet scaffold [[learning/packets/david-west-object-thinking/packet]] from a user-provided NotebookLM notebook screenshot about David West's Object Thinking.

## [2026-06-22] bridge.notebooklm.prepare | David West Object Thinking

Prepared three NotebookLM copy-text inputs for [[learning/packets/david-west-object-thinking/packet]]: [[schema/prompts/notebooklm-contract-source]], [[learning/bridge/notebooklm/context-slices/david-west-object-thinking]], and [[learning/bridge/notebooklm/run-prompts/david-west-object-thinking]].

## [2026-06-22] bridge.notebooklm.manual-import | David West Object Thinking

Preserved direct NotebookLM packet export at [[learning/inbox/notebooklm/david-west-object-thinking/packet-export]]. Classified the export as `repairable`: required top-level headings were present, but candidate concept format and human-contact semantics required local reconciliation.

## [2026-06-22] packet.draft | David West Object Thinking

Normalized the repaired NotebookLM export into [[learning/packets/david-west-object-thinking/packet]]. Drafted synthesis, candidate concepts, suggested patches, and an import repair note. The packet is blocked from promotion pending a completed human-contact artifact.

## [2026-06-22] protocol.decision | Active Gardening Review

Recorded [[docs/adr/0025-require-active-gardening-review]] after deciding that agents should actively participate in the garden instead of only importing and promoting notes. Added [[schema/gardening-review]], `garden.review`, and the first packet-specific review at [[learning/packets/david-west-object-thinking/artifacts/gardening-review]].

## [2026-06-22] packet.review | Evergreen Notes

Recorded human-contact artifact for [[learning/packets/evergreen-notes/packet]] from the user's NotebookLM podcast listening notes. Updated the packet to ready-for-review, added `Note Titles as APIs` as a user-originated candidate concept, and created [[learning/packets/evergreen-notes/artifacts/gardening-review]].

## [2026-06-22] packet.promote | Evergreen Notes

Promoted [[wiki/synthesis/evergreen-notes-as-evolving-insight]], [[wiki/concepts/evergreen-note]], [[wiki/concepts/the-ritualization-trap]], and [[wiki/concepts/note-titles-as-apis]] from [[learning/packets/evergreen-notes/packet]]. Applied approved patches to [[wiki/concepts/digital-garden]] and [[wiki/synthesis/digital-garden-ethos]]. Deferred `Bi-directional Linking` and `Epistemic Status`.

## [2026-06-22] packet.review | David West Object Thinking

Recorded human-contact artifact for [[learning/packets/david-west-object-thinking/packet]] from the user's NotebookLM podcast listening notes and reflection. Updated the packet to ready-for-review, added `Option/Maybe Pattern` and `Actor Model` as user-originated candidates, and updated [[learning/packets/david-west-object-thinking/artifacts/gardening-review]] with post-contact promotion guidance.

## [2026-06-22] packet.promote | David West Object Thinking

Promoted [[wiki/synthesis/object-thinking-and-the-digital-garden]], [[wiki/concepts/object-thinking]], [[wiki/concepts/software-as-theater-metaphor]], [[wiki/concepts/self-evaluating-rule]], and [[wiki/concepts/option-maybe-pattern]] from [[learning/packets/david-west-object-thinking/packet]]. Applied approved patches to [[wiki/synthesis/digital-garden-ethos]] and [[wiki/concepts/digital-garden]]. Deferred `Null Object Pattern` and `Formalism vs Hermeneutics`.

## [2026-06-22] concept.promote | Digital Garden Ethos

Promoted [[wiki/concepts/knowledge-gardener]] and [[wiki/concepts/playful-knowledge-practice]] from [[learning/packets/digital-garden-ethos/packet]] after the user approved the previously deferred concepts. Recorded [[learning/packets/digital-garden-ethos/artifacts/gardening-review]] with the recommendation to explore emojis as a separate learning packet before adding emoji conventions to the protocol.

## [2026-06-23] packet.review | Architecture of Original Thought

Recorded human-contact artifact for [[learning/packets/architecture-of-original-thought/packet]] from the user's NotebookLM podcast listening notes and reflection. Updated the packet to ready-for-review and added [[learning/packets/architecture-of-original-thought/artifacts/gardening-review]] with promotion guidance around active reconstruction, desirable difficulties, cognitive offloading, and memory-value selection.

## [2026-06-23] bridge.notebooklm.prepare | Emoji Education AI Communication

Prepared [[learning/bridge/notebooklm/context-slices/emoji-education-ai-communication]] and [[learning/bridge/notebooklm/run-prompts/emoji-education-ai-communication]] for a NotebookLM packet about emojis, education, contextual digital symbols, and AI interpretation.

## [2026-06-23] bridge.notebooklm.manual-import | Emoji Education AI Communication

Preserved direct NotebookLM packet export at [[learning/inbox/notebooklm/emoji-education-ai-communication/packet-export]]. Classified the export as `repairable`: required sections were present, but local reconciliation was needed because the screenshot showed 6 sources while the export listed 5.

## [2026-06-23] packet.draft | Emoji Education AI Communication

Normalized the repaired NotebookLM export into [[learning/packets/emoji-education-ai-communication/packet]]. Drafted synthesis, candidate concepts, suggested patches, import repair, and [[learning/packets/emoji-education-ai-communication/artifacts/gardening-review]]. The packet is blocked from promotion pending a completed human-contact artifact.

## [2026-06-23] protocol.decision | Source-Manifest-First NotebookLM Bridge

Recorded [[docs/adr/0028-use-source-manifest-first-notebooklm-bridge]] after deciding that NotebookLM should usually provide source manifests and learning media, while Codex checks sources and creates garden-aware packets locally. Added [[schema/prompts/notebooklm-source-manifest-prompt]] and updated [[schema/manual-notebooklm-import]], [[schema/prompt-design]], [[schema/operations]], and [[CONTEXT]].

## [2026-06-23] protocol.maintenance | Source Manifest Provenance Hardening

Hardened [[schema/prompts/notebooklm-source-manifest-prompt]] after a NotebookLM Source Manifest returned mostly `URL: unknown` entries and treated access-blocker pages as sources. The prompt now requires exact URLs for URL-based sources and returns a `NOT READY` preflight when provenance is incomplete.

## [2026-06-23] protocol.maintenance | Source Manifest Provenance Calibration

Softened [[schema/prompts/notebooklm-source-manifest-prompt]] after the strict provenance preflight proved too brittle. Source manifests now label URL visibility and local recovery actions instead of failing the whole manifest when public URLs can likely be recovered by Codex search.

## [2026-06-23] protocol.decision | NotebookLM Packet Export Default

Recorded [[docs/adr/0029-use-notebooklm-packet-export-as-default-source-heavy-bridge]] after deciding that source-heavy NotebookLM notebooks should return to full Packet Export by default. Source Manifest remains as a diagnostic provenance tool, but NotebookLM should do the heavy digestion for books, large PDFs, transcripts, uploaded files, and large mixed source sets. Updated [[schema/manual-notebooklm-import]], [[schema/prompt-design]], [[schema/prompts/README]], [[schema/operations]], and [[CONTEXT]].

## [2026-06-23] bridge.notebooklm.prepare | Agentic AI Architectures Frameworks Operational Loops

Prepared [[learning/bridge/notebooklm/context-slices/agentic-ai-architectures-frameworks-operational-loops]] and [[learning/bridge/notebooklm/run-prompts/agentic-ai-architectures-frameworks-operational-loops]] for a NotebookLM packet about agentic AI architectures, planning, tools, memory, feedback mechanisms, loop engineering, and operational risks.

## [2026-06-23] packet.promote | Architecture Of Original Thought

Promoted [[wiki/synthesis/original-thought-as-active-reconstruction]], [[wiki/concepts/first-principles-reasoning]], and [[wiki/concepts/desirable-difficulties]] from [[learning/packets/architecture-of-original-thought/packet]]. Applied approved patches to [[wiki/synthesis/llm-wiki-pattern]], [[wiki/synthesis/digital-garden-ethos]], and [[wiki/concepts/digital-garden]]. Deferred `Active Reconstruction`, `Illusion of Competence`, `Cognitive Offloading`, `Bloom's Taxonomy`, and `Levels of Reading`.

## [2026-06-23] bridge.notebooklm.manual-import | Agentic AI Architectures Frameworks Operational Loops

Preserved direct NotebookLM packet export at [[learning/inbox/notebooklm/agentic-ai-architectures-frameworks-operational-loops/packet-export]]. Classified the export as `repairable`: required sections were present, but source URLs were incomplete, the screenshot showed 10 sources while the export listed 8, and the human-contact section contained a generated podcast brief rather than completed human contact.

## [2026-06-23] packet.draft | Agentic AI Architectures Frameworks Operational Loops

Normalized the repaired NotebookLM export into [[learning/packets/agentic-ai-architectures-frameworks-operational-loops/packet]]. Drafted synthesis, candidate concepts, suggested patches, import repair, and [[learning/packets/agentic-ai-architectures-frameworks-operational-loops/artifacts/gardening-review]]. The packet is blocked from promotion pending a completed human-contact artifact.

## [2026-06-25] seed.import | Learning Garden Capture Skill

Imported [[skills/learning-garden-capture/SKILL]] from the public seed into the private working garden so local agents can capture reusable session insights into `learning/inbox/agent-captures/` without bypassing human-contact or promotion review.
