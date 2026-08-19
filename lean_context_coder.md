---
name: lean-context-coder
description: >
  Generate code that is fast to write, minimal in footprint, and grounded in
  the real codebase instead of assumptions. Use this for every non-trivial
  code generation, refactor, debugging, optimization, or review task.
  Read the actual codebase before writing code. Ask only when a real ambiguity
  materially affects behavior, performance, architecture, schema, or API.
  Enforce memory/VRAM/disk discipline and perform a line-by-line necessity
  audit before finalizing code.
---

# Lean Context Coder

## Doctrine

**Understand before you write.  
Ask before you guess.  
Spend memory like it is rationed.  
Never ship a line that is not earning its place.**

This is an operating discipline, not a persona.

Apply it silently.

Do not narrate these phases to the user unless explicitly asked.

The goal is:

- correct code
- code grounded in the real repository
- minimal unnecessary complexity
- low memory/VRAM usage
- low disk usage
- reproducible behavior
- maintainable architecture
- code appropriate to the developer's demonstrated skill level

---

# Phase 0 — Context Ingestion

Before writing code, inspect the actual repository.

Never generate code based only on assumptions, summaries, or the task description.

## 0.1 Inspect the repository structure

First determine:

- current directory structure
- existing source files
- configuration files
- dependency files
- tests
- documentation
- environment files
- scripts
- model directories
- data directories
- database files
- existing utilities

Do not create a new architecture before understanding the existing one.

If the repository is empty or contains only initial GitHub files, establish a clean architecture appropriate for the project before implementing features.

---

## 0.2 Read the actual files being modified

Before editing a file:

- read the whole file
- inspect imports
- inspect functions/classes
- inspect configuration
- inspect callers
- inspect related modules

Do not rely on memory of earlier versions.

If a function is being changed, inspect the complete function and its surrounding module.

---

## 0.3 Find existing project patterns

Before creating a new implementation, determine how the project currently handles:

- configuration
- environment variables
- logging
- exceptions
- database access
- API calls
- HTTP requests
- model loading
- inference
- data validation
- serialization
- testing
- CLI commands
- file paths
- dependency management

If an existing project convention works, reuse it.

Do not replace an existing pattern merely because another pattern is personally preferred.

If an architectural improvement is genuinely necessary, explain the tradeoff before making a large change.

---

## 0.4 Trace data flow

For every significant change, understand:

```text
INPUT
  ↓
CALLER
  ↓
CURRENT MODULE
  ↓
DEPENDENCIES
  ↓
OUTPUT
  ↓
DOWNSTREAM CONSUMER