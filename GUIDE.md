---
FrontmatterVersion: 1
DocumentType: Guide
Title: IoC Container Guide
Summary: Playbook for maintaining the Fathym IoC container for Deno runtimes.
Created: 2025-11-20
Updated: 2025-11-20
Owners:
  - fathym
References:
  - Label: Project README
    Path: ./README.md
  - Label: Project Agents Guide
    Path: ./AGENTS.md
  - Label: Projects: Ref-Arch README
      Path: ../README.md
  - Label: Projects: Ref-Arch Guide
      Path: ../GUIDE.md
  - Label: Root Workspace Guide
    Path: ../../../WORKSPACE_GUIDE.md
---

# IoC Container Guide

Use this playbook to keep IoC container work predictable and discoverable.

## Current Focus

- Validate container lifecycle behaviors (transient, scoped) and symbol registration patterns.
- Provide usage examples for common scenarios (factory registrations, lazy resolutions, scoped lifetimes).
- Align APIs with other ref-arch libraries and the CLI where integration matters.

## Workflow

1. **Align scope** in [`README.md`](./README.md): note intended change (feature, fix, release prep) and target repo/branch if it moves.
2. **Design & docs**: capture API proposals or examples in `docs/` (create if needed) with frontmatter and links to upstream assumptions.
3. **Capture provenance**: record upstream source, release channel, and version pins in `UPSTREAM.md` once publishing.
4. **Validate behavior**: run `deno task test` for coverage; use `deno task
   build` or `deno task deploy` before releases, and add/update smoke examples as APIs evolve.
5. **Communicate changes**: document breaking changes with migration guidance and notify consumers (CLI, other libraries, micro-frameworks).

## Verification

- Ensure links stay relative and parent guides remain discoverable.
- Keep the roster entry in `../README.md` current when docs or status change.
- When workspace tasks exist, also run: `deno task prompts:verify-frontmatter`, `deno task link:verify`, `deno task workspace:check`.
