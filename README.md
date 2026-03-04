# Zettelkasten — Personal Knowledge Vault

A single Obsidian vault serving as the primary knowledge management system across all projects and intellectual work. Built on Luhmann's Zettelkasten methodology — one system for an entire intellectual career rather than project-specific notebooks.

## Philosophy

This vault follows the single-vault principle: project affiliation is handled through tags and links, not folder silos. Fragmenting the knowledge graph across projects would undermine the core value of the system — the unexpected connections that emerge when ideas from different domains occupy the same space.

The organizing principle is epistemic function, not subject matter or project origin. A note about Bakhtinian dialogism and a note about API architecture live in the same vault because they may turn out to be the same note.

## Infrastructure

**Working layer:** Obsidian Sync — live across all devices, end-to-end encrypted.
**Backup and version history:** This repository. Sync is the primary; Git is the off-platform record.

The `.obsidian/` configuration folder is tracked (minus workspace state files) to preserve plugin settings, themes, and hotkeys across machines.

## Structure

Folders organize notes by epistemic type:

- `/fleeting` — raw captures, unprocessed, low barrier to entry
- `/literature` — source-based notes, ideas attributed to specific texts or conversations
- `/permanent` — fully developed concept notes, meant to persist and accumulate links
- `/log` — session and decision records
- `/atelier` — drafts in progress, notes that haven't resolved into permanent form yet

## Current Permanent Notes

- `vnenakhodimost-surplus-of-seeing.md` — Bakhtin's outsideness and surplus of seeing; connection to sociocultural hermeneutics and multi-model triangulation
- `ct-interaction-design-taxonomy.md` — Crosstalk interaction design taxonomy: roles, modes, and meta-structure as three distinct levels

## Related Repositories

- `habermas-lab/crosstalk` — Crosstalk Lab project
- `habermas-lab/codex-kitchen` — Codex Kitchen project

---
*Vault initialized: 2026-03-03*
