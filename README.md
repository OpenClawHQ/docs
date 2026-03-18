# effectorHQ Documentation

The knowledge base for building skills and extensions with effectorHQ.

## Quick Navigation

| Guide | For who | What you'll learn |
|-------|---------|-------------------|
| [Getting Started](guides/getting-started.md) | New builders | Create your first skill in 10 minutes |
| [Architecture](guides/architecture.md) | Anyone curious | How effectorHQ fits together: manifests, core, targets, bridges |
| [Skill Development](guides/skill-development.md) | Skill builders | Build language-agnostic skills with SKILL.md |
| [Extension Development](guides/extension-development.md) | TypeScript developers | Build full-featured plugins with TypeScript |
| [SKILL.md Format Reference](reference/skill-format.md) | Everyone | Complete reference for SKILL.md files |
| [Manifest Reference](reference/plugin-manifest.md) | Extension builders | Reference for `effector.toml` runtime bindings |

## Key Concepts

**Skills**: Language-agnostic, markdown-based automation. Stored alongside code (or in a skills directory) and compiled/validated via the effector toolchain.

**Extensions/Plugins**: Full-featured TypeScript packages. Implement channels, configuration, and complex logic. Distributed via npm.

**Registry**: Optional distribution surface. Effector manifests are runtime-neutral; registries are integrations, not the core.

**Core**: Shared kernel that parses `SKILL.md` + `effector.toml`, validates schema/types, and compiles to targets (MCP / OpenAI Agents / LangChain / JSON).

**Agent Runtime**: Any runtime that can consume a compiled target artifact (e.g. MCP tool schema). effectorHQ does not require a bespoke runtime.

## Getting Help

- Check the [Architecture guide](guides/architecture.md) to understand how everything fits together
- Browse the [Skill Development guide](guides/skill-development.md) for building skills
- See [Extension Development](guides/extension-development.md) for TypeScript plugins
- Refer to [SKILL.md Format Reference](reference/skill-format.md) for all skill frontmatter fields

## Contributing to Docs

Found an error? Have a better explanation? PRs are welcome.

For doc-specific conventions: write in plain language, use code examples liberally, keep paragraphs short.

---

<sub>effectorHQ · Every effector extends the reach.</sub>
