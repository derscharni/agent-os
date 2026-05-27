# agent-os

Personal Agent OS — Infrastruktur für AI-Agenten, die deinen Kontext kennen, ohne ihn weiterzugeben.

## Was das ist

Die meisten AI-Frameworks lösen das falsche Problem. Sie optimieren Tool-Calling und Orchestration. Das ist nicht der Engpass.

Der Engpass ist anders: dein persönlicher Agent hat deinen vollen Kontext. Jede andere KI, die er anspricht, soll bekommen, was sie braucht — nicht mehr. Das ist Context Sovereignty als Infrastruktur. Nicht als Pattern, nicht als Best Practice. Als Code, der läuft.

Dazu kommt der Second Brain Layer: ein System, das ohne dich nachdenkt, priorisiert, verknüpft — und morgens mit Ergebnissen wartet.

## Module

- [`context-handshake`](https://github.com/derscharni/context-handshake) — Portable Agent Context. Identität + Session Intent in zwei Markdown-Files. Erstes Modul, MVP live.
- [`modules/sovereignty/`](modules/sovereignty/) — Selective Disclosure Layer. Stub.
- [`modules/vault/`](modules/vault/) — Second Brain / Dreaming Layer. Stub.

## Status

Frühe Phase. Aktive Module siehe oben. Roadmap in [ROADMAP.md](ROADMAP.md). Was das Konzept genau abgrenzt, steht in [SPEC.md](SPEC.md).
