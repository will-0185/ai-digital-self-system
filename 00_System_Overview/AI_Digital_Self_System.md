# AI Digital Self System

**File purpose**: This document explains the core goals, architecture, file layers, invocation methods, material recording, output mechanisms, and evolution mechanisms of the AI Digital Self System.

## Goals

- **Core goal**: Build an AI digital self that grows closer to the user's thinking over time through long-term recording and periodic iteration.
- **System goal**: Enable the system to understand, assist judgment, aid creation, and sustain expression style across different AI models over time.
- **Long-term goal**: On longer time scales, this digital self can carry forward a part of the user's thinking and creation ability, forming a form of long-term continuity.

## Core components

- **Meta-cognition**: The program of thinking, invocation, arbitration, and revision.
- **Core personality**: The content body of the digital self (six dimensions).
- **Meta-knowledge**: A small set of generative paradigms distilled from external knowledge.
- **Knowledge base**: Callable facts, materials, skills, notes, and methods.

## Architecture

```text
00_System_Overview      System overview and prompt collection
01_System_Kernel        Meta-cognition, meta-knowledge, six core personality dimensions
02_Knowledge_Creation   External archive, skills, writing, knowledge notes
03_Material_Record      Monthly raw material records
04_Evolution            Monthly trend, quarterly review, annual report
```

## How it runs

The system uses a local-filesystem + dual workspace model:

- **System evolution workspace**: Maintain and optimize the system itself.
- **Content creation workspace**: Produce specific output based on the current system.

The local filesystem is the authoritative source. AI projects are temporary workspaces.

## Evolution cycle

- **Monthly**: Observe changes. Do not directly modify the system kernel.
- **Quarterly**: Conduct personality review. Propose revision suggestions.
- **Annual**: Judge whether the system has entered a new version.
- **Trigger-based**: Make small fixes when specific issues are found.

## Public version note

This repository is a public framework and example — not the author's full private digital self. Real material records, evidence indexes, life logs, personal relationships, and unpublished works should remain in your private system.

See [Privacy_Boundary.md](./Privacy_Boundary.md).
