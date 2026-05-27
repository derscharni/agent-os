# Vault / Dreaming Layer

Second Brain mit asynchronen Background-Prozessen.

## Status

Stub. Reference-Implementation in Arbeit.

## Was es macht (geplant)

Lokaler Markdown-Vault (Obsidian-kompatibel) plus zwei Background-Prozesse:

- **Archivar** — Vault-Evaluator, läuft nachts, schlägt Supersessions/Connections/Decay vor.
- **Dreaming Cron** — verknüpft neue Notizen mit bestehenden Konzepten, priorisiert offene Threads, schlägt morgens Aktionen vor.

Beide arbeiten ohne User-Input. Output landet im Inbox-Pattern: Vorschläge in einem Dropbox-Verzeichnis, Mensch reviewed und merged.

## Spec folgt

Wird in eigenem Repo veröffentlicht, sobald Reference-Implementation stabil ist.
