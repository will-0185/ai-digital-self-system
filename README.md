# AI Digital Self System

**English** | [中文](./README.zh-CN.md)

A local-first filesystem framework for building, maintaining, and evolving a personal AI digital self.

## What is this?

Most AI conversations are temporary. Context disappears. Memory is unstable. And deeper patterns of how a person thinks, judges, and creates are rarely preserved over time.

AI Digital Self System solves this by using the local filesystem as the authoritative source of truth.

It separates:

- System evolution
- Content creation
- Personal material
- Knowledge resources
- Periodic self-review

The result is a migratable, iterable, model-agnostic framework for long-term personal AI modeling.

## Architecture

```text
00_System_Overview      System overview and prompt collection
01_System_Kernel        Meta-cognition, meta-knowledge, core personality
02_Knowledge_Creation   External archive, skills, writing, notes
03_Material_Record      Monthly raw material records
04_Evolution            Monthly, quarterly, and annual review
```

## Quick start

1. Read `00_System_Overview/AI_Digital_Self_System.md`
2. Copy the structure to your local filesystem
3. Write your own system kernel files
4. Start recording material monthly
5. Run periodic evolution reviews (monthly / quarterly / annual)
6. Use the prompts in `Prompt_Collection.md` with your preferred AI model

## Public vs private boundary

This repository is a public framework and example — not the author's full private digital self.

**Do not put your real digital self directly into a public repository.**

Keep the following in your private system or private repository:

- Real monthly summaries
- Personal relationships
- Life logs
- Evidence indexes
- Unpublished works
- Sensitive personal materials
- API keys, tokens, account credentials

See `00_System_Overview/Privacy_Boundary.md` for details.

## License

MIT License — see [LICENSE](./LICENSE).
