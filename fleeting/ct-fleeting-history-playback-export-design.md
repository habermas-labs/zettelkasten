# Fleeting: History, Playback, and Export Design Session — 2026-03-25

**Type:** Fleeting
**Tags:** #crosstalk #history #playback #export #session-knowledge-architecture
**Related:** CT-039, CT-052, CT-054, CT-055, CT-060, CT-078, CT-093, CT-103, CT-104, CT-105
**Date:** 2026-03-25

---

## Provenance

Design session covering history navigation, playback mode, per-model response review, and export system evolution. Conducted in Claude project thread. Tracker updated same session — see CT-TRACKER.md commit 2026-03-25.

---

## History / Turn Chips (CT-104)

Current history panel shows user prompt chips only. Decision: reconceptualize as turn chips representing every turn — user prompts and AI-only turns (Conductor/Forward moves). AI-only turns get compact subdued routing indicators (e.g. → ◈ Claude → ◇ ChatGPT). Turn number always visible. This is prerequisite infrastructure for both CT-103 (Focus Thread) and CT-039 (playback).

---

## Playback Mode (CT-039)

Reframed from automated replay to turn viewer. Key decisions:

- Clicking a turn chip in playback mode renders that turn's full state into the three-column layout — model responses in their columns as they appeared live
- Input field locked during playback
- All chips visible; active turn highlighted
- Restore to present: implicit on mode exit; explicit "return to present" control within playback for non-linear navigation
- Per-column prev/next arrows scoped to each model's response sequence — surface within playback mode only; resolves CT-055 as byproduct
- Checkbox on turn chips serves dual function: flags turns for Focus Thread export (CT-103) and for re-entry — exit playback with flagged turn pre-loads context into input band

Data layer confirmed sufficient: turnHistory.results is keyed by model, full response text present. displayedTurnIndex tracked per chip as local state. No schema changes required.

---

## Per-Model Navigation (CT-055 / CT-093)

Resolved as part of CT-039. Per-column arrows in playback mode give each column independent navigation through that model's response history. The chip-click is a global turn index set; the column arrows are per-model fine navigation within playback. Both available simultaneously.

---

## Reverse Chronological Toggle (CT-052)

Default reverse chron for history panel — most recent turn is almost always the working surface. Explicit toggle to chronological. Ships independently; lower complexity than bidirectional chip navigation.

---

## Export System Evolution

**060** — bullet minimal summary: format option on summary flyout, not a new export type. Same trigger, different output shape.

**078** — plain text export: format option alongside existing types. Use cases: renderer-free inspection, user preference.

**047** — exit scaffold: forward-looking artifact distinct from summary. Captures conditions for re-entry — key claims, open questions, what's worth carrying forward as a generative prompt. Model choice for generating the scaffold may matter. Candidate for "Summarize with" flyout.

**103** — Focus Thread: live annotation layer, not a range selector. User checks turn chips during the session at the moment of sharpest attention. Checkbox dual function noted above. Requires CT-104.

**103 deferred for its own session** — conceptually substantial enough to warrant dedicated treatment. Checkbox mechanism seeded in CT-039/CT-104 implementation.

---

## Deferred Items

- CT-049 (configurable dashboard widgets) → deferred, revisit as widescreen support
- CT-054 (history panel as dashboard widget) → same

---

## Routing Addendum

Full session knowledge architecture synthesis captured in CT-TRACKER Notes (2026-03-25 entry) and proposed as W009 permanent note: session-knowledge-architecture.md.
