# AI Digital Self System

**File purpose**: This document explains the core goals, architecture, file layers, invocation methods, material recording, output mechanisms, and evolution mechanisms of the AI Digital Self System.

## Goals

- **Core goal**: Build an AI digital self that grows closer to the user over time through long-term recording and periodic iteration.
- **System goal**: Enable the system to understand the user, assist judgment, aid creation, and sustain expression style across different AI models over time.
- **Long-term goal**: On longer time scales, this digital self can carry forward a part of the user's thinking and creation ability, forming a form of long-term continuity.

## Core components

- **Meta-cognition**: The program of thinking, invocation, arbitration, and revision. This is what makes the digital self "think like the user" rather than "quote the user".
- **Core personality**: The content body of the digital self. Six dimensions: World View, Value Priorities, Life Direction, Survival Philosophy, Decision Making, Aesthetic Interests.
- **Meta-knowledge**: A small set of generative paradigms distilled from external knowledge. Used for domain-level reasoning and expression.
- **Knowledge base**: Callable facts, materials, skills, notes, and methods for creation.

**Relationships**:
- Meta-cognition is the operating system, core personality is the content body, meta-knowledge provides paradigms, and knowledge base provides facts and methods.
- Meta-cognition, core personality, and meta-knowledge together define "who the user is" — they live in the system kernel layer. The knowledge base defines "what can be called" — it lives in the knowledge creation layer.

## Architecture

```text
00_System_Overview      System overview and prompt collection
01_System_Kernel        Meta-cognition, meta-knowledge, core personality
02_Knowledge_Creation   External archive, skills, writing, notes
03_Material_Record      Monthly raw material records
04_Evolution            Monthly trend, quarterly review, annual report
```

**Structure**:
- **System Overview (00)**: Architecture document and prompt collection. Background material for any LLM session.
- **System Kernel (01)**: The core of the digital self. Meta-cognition, meta-knowledge, and six personality dimensions exist in parallel.
- **Knowledge Creation (02)**: Creative workspace containing both inputs (archive, skills, notes) and outputs (writing).
- **Material Record (03)**: Raw material. Daily records organized by topic.
- **Evolution (04)**: Horizontal governance tool. Periodically reviews whether the system needs revision.

## System kernel

The system kernel is the "self" of the digital self. Eight files in parallel:

| File | Purpose |
|------|---------|
| Meta_Cognition | Program of thinking, invocation rules, conflict arbitration, self-revision |
| Meta_Knowledge | Generative paradigms distilled from external knowledge |
| World_View | How the user sees the world |
| Value_Priorities | What matters more to the user |
| Life_Direction | Where the user wants to go |
| Survival_Philosophy | How the user chooses to live |
| Decision_Making | How the user judges and acts in specific situations |
| Aesthetic_Interests | What attracts the user, what style they prefer |

**Three categories**:
- **Meta-cognition (process)**: Defines how to think, how to invoke other files, how to handle conflicts, how to revise. Does not produce content judgments.
- **Meta-knowledge (paradigms)**: Provides cross-domain generative paradigm. Each entry is a highly abstract judgment used as a foundation for reasoning.
- **Core personality (content)**: Provides concrete world view, values, life direction, decision principles, aesthetic preferences. Maintained independently, tensions allowed.

## How it runs

The system uses a "local filesystem + dual workspace" model:

```
1. System evolution workspace  → Maintain and optimize the system itself
2. Content creation workspace  → Produce output based on the current system
```

Workspace 1 defines "who the user is". Workspace 2 uses that to complete "what to say". Output from workspace 2 feeds back into workspace 1's material records.

They communicate through the **local filesystem** — not directly.

### Local filesystem vs workspace

```
Local filesystem  =  Master system / source of truth / long-term storage
Workspace         =  Temporary processing / not long-term storage
```

**Key principles**:
- **Local filesystem is the single source of truth**: All files ultimately follow the local version.
- **Workspace is temporary**: LLM conversation history and uploaded files are temporary.
- **Cross-LLM migratable**: Simply upload local files + copy project instructions to migrate to a new LLM.

## Evolution cycle

- **Monthly**: Observe changes. Generate monthly trend report. Do not modify the system kernel.
- **Quarterly**: Conduct personality review. Propose revision suggestions. Actually modify personality and meta-knowledge.
- **Annual**: Generate annual evolution report. Make version-level revisions across all kernel files.
- **Trigger-based**: Make small fixes when specific issues are found.

## Content creation workspace

### Invocation principles

- **Meta-cognition always takes priority**: Any task first applies meta-cognition rules for orchestration.
- **Core personality called by default**: But which dimensions are primary vs secondary depends on the task.
- **Knowledge base, meta-knowledge, material records**: Called on demand, not always loaded.

**Typical scenarios**:
- Commentary → Meta-cognition + World_View/Value_Priorities + material records
- Domain analysis → Meta-cognition + knowledge base + meta-knowledge support
- Fiction → Meta-cognition + Aesthetic_Interests/Survival_Philosophy + materials on demand

## Core principles

- **System level**: Local filesystem is the master. Any LLM can run this system — upload files + copy instructions.
- **Architecture level**: Four-layer main architecture (System Kernel / Knowledge Creation / Material Record / Evolution) plus System Overview. Numbers are directory ordering, not invocation order. System kernel is flat — eight files in parallel.
- **File maintenance**: Single file for external archive, folder for skills, individual md files for notes. Monthly records organized into three sections: life log / personality signals / external knowledge.
- **Evolution governance**: Monthly trends only filter signals. Quarterly review has revision suggestion authority. Annual report makes version judgments. Small changes anytime, big changes by cycle.
- **Operation**: System evolution workspace defines "who the user is". Content creation workspace produces "what to say". They communicate through the local filesystem.

## Public version note

This repository is a public framework and example — not anyone's full private digital self. Real material records, evidence indexes, life logs, personal relationships, and unpublished works should remain in your private system.

See [Privacy_Boundary.md](./Privacy_Boundary.md).
