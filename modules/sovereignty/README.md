# Sovereignty Layer

Selective Disclosure für persönliche AI-Agenten.

## Status

Stub. Reference-Implementation in Arbeit.

## Was es macht (geplant)

Klassifiziert ausgehende Kontext-Fragmente in vier Klassen, bevor sie an externe Services gehen:

- **PUBLIC** — bereits öffentlich, freie Weitergabe.
- **NEGOTIABLE** — kontextabhängig, mit Flag passieren.
- **PRIVATE** — nicht freigegeben, blockieren.
- **SOVEREIGN** — hochsensibel oder unklar, eskalieren.

Klassifikation läuft lokal (Local-LLM, kein Cloud-Call). Regeln sind als Markdown-Datei definiert, nicht als Code — auditierbar, anpassbar.

## Spec folgt

Wird in eigenem Repo veröffentlicht, sobald Reference-Implementation stabil ist.
