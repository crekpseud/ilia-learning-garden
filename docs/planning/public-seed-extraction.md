# Public Seed Extraction Plan

## Verdict

The current garden is not suitable to become a public seed as-is.

It is valuable as the private working garden and as the source from which a public seed can be extracted. It already contains reusable protocol decisions, prompt templates, agent instructions, and starter concepts. It also contains personal learning traces and packet history that should not be part of a public starter kit.

## Why It Is Not Public-Seed Ready

### Private Or Personal Material

- `docs/context/user-working-profile.md` contains personal working-profile information.
- `learning/packets/*/human-contact.md` contains human-contact reflections and listening notes.
- `learning/packets/*/artifacts/gardening-review.md` often contains user-specific interpretation and next-learning paths.
- `learning/inbox/notebooklm/**/packet-export.md` contains raw external model output tied to the user's notebooks.
- `log.md` records the user's actual learning and promotion history.

### Starter-Kit Clarity

The current vault tells the story of how this garden was built. That is useful for the user, but a public seed should tell a different story: how another person can start their own garden.

The public seed should avoid feeling like someone else's personal brain dump. It should provide protocol, examples, and enough public-safe knowledge to help an agent operate.

### Source Licensing And Quoting

`docs/research/karpathy-llm-wiki.md` is useful as a bootstrapping source, but the public seed should prefer a source record, summary, and link rather than redistributing large third-party text unless the license clearly permits it.

### Privacy Boundary

The current repository has already acted as both public seed and private working garden. Future work should separate those roles structurally rather than relying on memory, frontmatter, or `.gitignore`.

## Recommended Public Seed Contents

### Keep Or Extract

- `AGENTS.md`
- `CONTEXT.md`, after making it public-seed oriented
- `schema/`
- `docs/adr/`
- `docs/planning/initial-milestones.md`, if rewritten as starter guidance
- `docs/context/project-idea.md`, if rewritten as public project overview
- `wiki/synthesis/llm-wiki-pattern.md`
- `wiki/synthesis/digital-garden-ethos.md`
- `wiki/synthesis/technopastoral-synthesis.md`
- `wiki/concepts/digital-garden.md`
- `wiki/concepts/the-stream.md`
- `wiki/concepts/evergreen-note.md`
- `wiki/concepts/knowledge-gardener.md`
- `wiki/concepts/playful-knowledge-practice.md`
- selected public-safe source records under `raw/sources/`

### Convert To Examples

- Replace real learning packets with one or two synthetic example packets.
- Use public source links and fake human-contact artifacts clearly marked as examples.
- Include a minimal NotebookLM example flow without the user's real notebook exports.

### Keep Private

- `docs/context/user-working-profile.md`
- real `learning/packets/**/human-contact.md`
- real `learning/inbox/**`
- Goodreads or other reading ledgers
- private or work-related packet exports
- personal `log.md`
- any future `private/` area

## Proposed Extraction Sequence

1. Make or choose a private working garden folder.

   The current repository can become the private working garden if the public GitHub repository is replaced by a clean seed repository. If any already-published material is sensitive, make the current GitHub repository private or recreate public history from a clean seed.

2. Create a new public seed checkout in a separate folder.

   Recommended shape:

   ```text
   learning-garden-seed/
   ilya-learning-garden/
   ```

3. Copy the allowlisted protocol surface into the public seed.

   Start with `schema/`, `docs/adr/`, `AGENTS.md`, `CONTEXT.md`, prompt templates, and public-safe wiki notes.

4. Rewrite public-facing docs.

   Add a public `README.md` that explains what the seed is, how to start, and what must stay private.

5. Add synthetic examples.

   Create example learning packets that demonstrate packet anatomy, human-contact gating, promotion review, and gardening review without using personal material.

6. Run a privacy audit.

   Search for personal names, private notes, human-contact reflections, local paths, Goodreads exports, work references, and unreviewed packet exports.

7. Publish the public seed.

   Commit the clean seed separately. Do not preserve private working-garden history in the public seed.

8. Add the public seed as an upstream source for the private garden.

   Pull public protocol improvements into the private garden deliberately.

## Folder Versus Branch Decision

Use separate folders and repositories, not branches.

Branches are convenient for code variants, but they are weak for privacy boundaries:

- both branches share one Git object database and history
- accidental pushes can expose private commits
- checkout mistakes can show private files in the public working tree
- Obsidian treats the folder as one vault, so branch switching changes the same vault underfoot
- public seed and private garden need different social meanings, remotes, and audit rules

Separate folders make the boundary legible:

```text
learning-garden-seed/       public, clean starter kit
ilya-learning-garden/       private, lived learning garden
work-learning-garden/       downstream work garden, no export back
```

## Agent Workflow

In the private garden, agents may run `seed.review` to detect reusable protocol improvements.

The output should be a proposal, not an automatic sync:

```text
private observation
-> public-safe seed proposal
-> user approval
-> patch applied in public seed checkout
-> public seed commit
-> private garden imports public update
```

The agent should use allowlists. It should not copy private packet material and then redact it by best effort.

## Open Questions

- Should the first public seed be a new GitHub repository or a cleaned replacement of the current repository?
- Which trusted wiki notes are public starter knowledge versus private evolved knowledge?
- Should public examples live under `learning/examples/` instead of `learning/packets/`?
- Should public seed releases use tags so private gardens can import protocol versions?
