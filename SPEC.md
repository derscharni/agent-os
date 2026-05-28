# Spec — Personal Agent OS

## Definition

A Personal Agent OS is a set of local infrastructure components that does three things:

1. **Provide context** — a person's full context is available to one or more personal AI agents, locally, searchable.
2. **Enforce selective disclosure** — when the personal agent talks to external AI services or other agents, only what was defined gets through. Classification runs locally, before egress.
3. **Work asynchronously** — background processes connect, prioritize, suggest. Even when no one is active.

## Layers

### Context Layer

Where the context lives. Markdown vault, local, persistent.

Reference implementation: Napkin Vault (Obsidian-compatible, plain markdown, file-based).
Portable handoff to other agents: [`context-handshake`](https://github.com/derscharni/context-handshake) — identity + session intent as two markdown files.

### Sovereignty Layer

Classifies outgoing context into four classes — `PUBLIC`, `NEGOTIABLE`, `PRIVATE`, `SOVEREIGN`. Enforces rules before data goes to external services. Operational detection runs locally (no cloud call for classification).

Stub. Reference implementation in progress.

### Dreaming Layer

Asynchronous background processes. Links notes, prioritizes open threads, suggests in the morning what to act on next. Runs on schedule or trigger, not on user input.

Stub. Reference implementation: archivist pattern (vault evaluator with sycophancy check).

## What it is not

- Not a tool-calling framework.
- Not an orchestration layer for multi-agent workflows.
- Not an LLM provider.

Those problems are well solved elsewhere (LangGraph, CrewAI, LiteLLM, ...). Personal Agent OS is the layer underneath: what the agent knows about you, what it passes on, what it does without you.

## Design principles

- **Local-first** — vault, classifier, scheduling run without cloud dependency.
- **Account-boundary** — owner account (human) and agent account (execution) are separated. Privilege escalation only via documented, auditable bridges.
- **Idempotency** — every setup is re-runnable. Backups before mutations. Atomic writes.
- **Audit trail** — all classification and write decisions are traceable.

## Status

Phase 1 — core. Modules developed and published individually. See [ROADMAP.md](ROADMAP.md).
