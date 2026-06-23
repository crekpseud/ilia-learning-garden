# Use public seed and private working garden

The garden should split into a public seed garden and a private working garden.

**Context**

This repository started as the first living seed vault. That was useful while the protocol, packets, trusted wiki, and agent workflows were still forming together.

The garden now contains two different kinds of value:

- reusable protocol material that other people should be able to clone, read, and adapt
- personal learning material, human-contact reflections, reading signals, and private context that should not become part of a public starter kit

The user wants to share the protocol and some public-safe starting knowledge with colleagues while continuing to grow a personal garden. A copied work garden may also receive protocol updates, but must not export work knowledge back.

**Considered Options**

- Keep one public repository and mark private files with frontmatter.
- Keep one repository with public and private branches.
- Keep one repository but rely on `.gitignore` for private material.
- Split into a public seed garden and a private working garden in separate folders/repositories.

**Decision**

Use two separate working folders/repositories:

```text
learning-garden-seed/      public seed garden
ilya-learning-garden/      private working garden
```

The public seed garden contains protocol, schemas, ADRs, portable agent instructions, prompt templates, public-safe examples, and a small starter wiki.

The private working garden is where day-to-day learning happens. It may contain reading ledgers, Goodreads exports, personal human-contact reflections, private packet exports, work-adjacent learning, private profile context, and any other non-public material.

Public and private gardens are not sync peers. The public seed is an upstream source of protocol. The private garden may pull or apply public seed updates. Private changes may be deliberately promoted back only as public-safe protocol patches.

Use separate folders rather than branches. Branches are not a privacy boundary because one `.git` directory stores history for both branches, accidental checkout or push can expose private files, and Obsidian cannot comfortably treat two branches as two simultaneous vaults. Separate folders make the boundary visible to humans, agents, Git remotes, and tools.

**Consequences**

The public seed can become a clean starter kit for other gardeners.

The private garden can keep growing without turning every personal source or reflection into a publication decision.

Agents must use allowlist language when preparing public seed changes. Metadata such as `visibility: private` can help agents, but it is not a security boundary.

The existing repository needs extraction work before it is suitable as the public seed. It currently mixes protocol, seed material, personal reflections, packet exports, and private context.

This decision refines [[0006-use-this-repository-as-the-seed-vault]]: the current repository began as a seed vault, but reuse now requires separating public seed material from private working material.
