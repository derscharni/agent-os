# Sovereignty Layer

Selective disclosure for personal AI agents.

## Status

Stub. Reference implementation in progress.

## What it does (planned)

Classifies outgoing context fragments into four classes before they go to external services:

- **PUBLIC** — already public, free to pass.
- **NEGOTIABLE** — context-dependent, pass with flag.
- **PRIVATE** — not cleared, block.
- **SOVEREIGN** — highly sensitive or unclear, escalate.

Classification runs locally (local LLM, no cloud call). Rules are defined in a markdown file, not in code — auditable, editable.

## Spec to follow

Will be published in its own repo once the reference implementation is stable.
