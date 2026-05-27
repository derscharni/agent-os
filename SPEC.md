# Spec — Personal Agent OS

## Definition

Ein Personal Agent OS ist ein Set lokaler Infrastruktur-Komponenten, das drei Dinge tut:

1. **Context bereitstellen** — der volle Kontext einer Person ist für einen oder mehrere persönliche AI-Agenten verfügbar, lokal, durchsuchbar.
2. **Selective disclosure durchsetzen** — wenn der persönliche Agent externe AI-Services oder andere Agenten anspricht, geht nur durch, was definiert wurde. Klassifizierung passiert lokal, vor dem Egress.
3. **Asynchron arbeiten** — Background-Prozesse verknüpfen, priorisieren, schlagen vor. Auch wenn niemand aktiv ist.

## Schichten

### Context Layer

Wo der Kontext lebt. Markdown-Vault, lokal, persistent.

Reference-Implementation: Napkin Vault (Obsidian-kompatibel, plain markdown, file-based).
Portable Übergabe an andere Agenten: [`context-handshake`](https://github.com/derscharni/context-handshake) — Identität + Session Intent als zwei Markdown-Files.

### Sovereignty Layer

Klassifiziert ausgehenden Kontext in vier Klassen — `PUBLIC`, `NEGOTIABLE`, `PRIVATE`, `SOVEREIGN`. Setzt Regeln durch, bevor Daten an externe Services gehen. Operationelle Detection läuft lokal (kein Cloud-Call für Klassifikation).

Stub. Reference-Implementation in Arbeit.

### Dreaming Layer

Asynchrone Background-Prozesse. Verknüpft Notizen, priorisiert offene Threads, schlägt morgens vor was als nächstes ansteht. Läuft auf Schedule oder Trigger, nicht auf User-Input.

Stub. Reference-Implementation: Archivar-Pattern (Vault-Evaluator mit Sycophancy-Check).

## Was es nicht ist

- Kein Tool-Calling-Framework.
- Kein Orchestration-Layer für Multi-Agent-Workflows.
- Kein LLM-Provider.

Diese Probleme sind anderswo gut gelöst (LangGraph, CrewAI, LiteLLM, ...). Personal Agent OS ist die Schicht darunter: was der Agent über dich weiß, was er weitergibt, was er ohne dich tut.

## Design-Prinzipien

- **Lokal first** — Vault, Klassifikator, Scheduling laufen ohne Cloud-Abhängigkeit.
- **Account-Boundary** — Owner-Account (Mensch) und Agent-Account (Execution) sind getrennt. Privilegien-Eskalation nur über dokumentierte, audit-bare Bridges.
- **Idempotenz** — jedes Setup ist mehrfach laufbar. Backups vor Mutations. Atomare Writes.
- **Audit-Trail** — alle Klassifikations- und Schreib-Entscheidungen sind nachvollziehbar.

## Status

Phase 1 — Kern. Module einzeln entwickelt und veröffentlicht. Siehe [ROADMAP.md](ROADMAP.md).
