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

**Skills**: Markdown-first capabilities that live next to code (or under a `skills/` tree). The toolchain parses, validates, and compiles them—no single vendor runtime required.

**Extensions/Plugins**: TypeScript packages with full IDE and deployment stories: channels, config, and heavier logic—published like any other npm module.

**Registry**: Optional. Manifests stay transport-agnostic; a registry is just one way to distribute them—not part of the core contract.

**Core**: One kernel reads `SKILL.md` and `effector.toml`, checks schema and types, and emits MCP, OpenAI Agents, LangChain, or JSON IR.

**Agent Runtime**: Whatever can load the compiled artifact (e.g. an MCP host). effectorHQ does not ship or mandate its own agent loop.

## Getting Help

- [Architecture](guides/architecture.md) — how manifests, core, targets, and bridges relate
- [Skill Development](guides/skill-development.md) — authoring `SKILL.md`
- [Extension Development](guides/extension-development.md) — TypeScript extensions
- [SKILL.md format](reference/skill-format.md) — every frontmatter field

## Contributing to Docs

Corrections and clearer explanations are welcome as pull requests.

Prefer plain sentences, concrete code snippets, and short paragraphs.

---

<sub>effectorHQ · Every effector extends the reach.</sub>

## License

This project is currently licensed under the Apache 2.0 License 。
