# Typed AI Agent Tools

AI agents are only as reliable as the tools they can safely discover, inspect, validate, and compile. `effectorHQ` exists to make those tools typed and verifiable — without tying you to a single runtime.

## The problem: agent failure is common

Our analysis of 13,729 ClawHub skills found a **67% agent failure rate**, driven by untyped interfaces, missing prerequisites, and permission mismatches:
https://github.com/effectorHQ/clawhub-analysis

If two skills can be chained today but their interfaces (and permissions) are unclear, you are gambling with every run.

## The capability layer: typed sidecars + one compiler

An Effector capability is defined once (sidecars + docs), then processed consistently:

- `SKILL.md` — human-readable capability definition with typed interfaces
- `effector.toml` — object-based permission model (network/filesystem/env/subprocess)
- `@effectorhq/core` — parse, validate, type-check, and compile to multiple tool surfaces

The goal is simple: authors describe a capability, and the toolchain makes it safer and more composable across runtimes.

## The golden path (lint -> eval -> validate -> compile)

From a fresh scaffold:

```bash
npx @effectorhq/create-effector my-skill --type skill
cd my-skill

npx @effectorhq/skill-lint .              # structure + schema lint
npx @effectorhq/skill-eval . --static-only
npx @effectorhq/core validate .             # schema validate + type-check
npx @effectorhq/core compile . -t mcp      # emit MCP tool surface
```

## Compile targets you can plug into

`effector-core` supports multiple compilation targets from the same Effector inputs:

- `mcp` — MCP tool schema (JSON-RPC 2.0)
- `openai-agents` — OpenAI Agents function tool definition
- `langchain` — LangChain structured tool mapping
- `json` — raw Effector IR (useful for custom pipelines)

## Where to explore

- `@effectorhq/core`: https://github.com/effectorHQ/effector-core
- Skills and permissions: `SKILL.md` + `effector.toml`
- Security and drift checks: https://github.com/effectorHQ/effector-audit
- Authoring starter: https://github.com/effectorHQ/create-effector

