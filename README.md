# agent-os

Personal Agent OS — infrastructure for AI agents that know your context without giving it away.

## What this is

Most AI frameworks solve the wrong problem. They optimize tool-calling and orchestration. That isn't the bottleneck.

The bottleneck is different: your personal agent has your full context. Every other AI it talks to should get what it needs — nothing more. That's context sovereignty as infrastructure. Not as a pattern, not as a best practice. As code that runs.

Beyond that, the second brain layer: a system that thinks without you, prioritizes, connects — and meets you in the morning with results.

## Modules

- [`context-handshake`](https://github.com/derscharni/context-handshake) — Portable agent context. Identity + session intent in two markdown files. First module, MVP live.
- [`modules/sovereignty/`](modules/sovereignty/) — Selective Disclosure Layer. Stub.
- [`modules/vault/`](modules/vault/) — Second Brain / Dreaming Layer. Stub.

## Status

Early stage. Active modules above. Roadmap in [ROADMAP.md](ROADMAP.md). Scope and boundaries in [SPEC.md](SPEC.md).

## Related Work

- **[ax-stack](https://github.com/derscharni/ax-stack)** — The design framework. AX Stack defines the five operational layers of human-agent interaction. agent-os is the infrastructure that runs them.
- **[context-handshake](https://github.com/derscharni/context-handshake)** — The first published module, portable agent context.
- **[trust-stack](https://github.com/derscharni/trust-stack)** — Three-layer model for trustworthy agent memory: security, authorization, temporal integrity.

## License

MIT.

---

*by [Jens Scharnetzki](https://www.linkedin.com/in/scharnetzki/) — Agent Experience design and context sovereignty infrastructure.*
