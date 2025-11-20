---
FrontmatterVersion: 1
DocumentType: Guide
Title: Fathym IoC Container
Summary: Lightweight inversion-of-control container for Fathym runtimes and Deno apps.
Created: 2025-11-20
Updated: 2025-11-20
Owners:
  - fathym
References:
  - Label: Projects: Ref-Arch README
      Path: ../README.md
  - Label: Projects: Ref-Arch AGENTS
      Path: ../AGENTS.md
  - Label: Projects: Ref-Arch Guide
      Path: ../GUIDE.md
  - Label: Root README
    Path: ../../../README.md
  - Label: Root Agents Guide
    Path: ../../../AGENTS.md
  - Label: Root Workspace Guide
    Path: ../../../WORKSPACE_GUIDE.md
  - Label: Project Agents Guide
    Path: ./AGENTS.md
  - Label: Project Guide
    Path: ./GUIDE.md
---

# Fathym IoC Container

Lightweight inversion-of-control (IoC) container for Deno and Fathym runtimes, providing simple registration/resolution with support for transient and scoped lifestyles.

- **Goal:** deliver a minimal, ergonomic IoC container for internal libraries, the CLI, and micro-frameworks.
- **Outputs:** container API, usage examples, and build/test scripts.
- **Code location:** this folder currently hosts the source.

## Current Status

- Source and exports live in this pod (`mod.ts`, `src/`).
- Deno tasks available (`deno task test`, `deno task build`, `deno task deploy`, `deno task version`).
- Publish/provenance not documented yet; add `UPSTREAM.md` when pinning.

## How to Work in This Pod

1. Read the root and portfolio Instruction Documents plus this project’s [`AGENTS`](./AGENTS.md) and [`GUIDE`](./GUIDE.md).
2. Declare intent before editing; summarize outcomes and open questions in this README or a short log.
3. Capture provenance and release channel in `UPSTREAM.md` once publishing to jsr/npm or other registries.
4. Keep links relative and note integrations with other ref-arch libraries or the CLI when APIs change.
5. Record prompts/scripts used for design or automation in the `References` sections of docs.
