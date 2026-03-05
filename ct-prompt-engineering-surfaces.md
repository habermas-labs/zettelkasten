# Prompt Engineering Surfaces in Crosstalk

**Type:** Concept note
**Tags:** #crosstalk #prompt-engineering #roles #constraints #interaction-design
**Related:** ct-interaction-design-taxonomy.md · CT-TRACKER entry 071
**Date:** 2026-03-04

---

## Three Distinct Surfaces

Effective prompt engineering in Crosstalk operates across three distinct surfaces that are easy to conflate but important to keep separate:

**1. Roles** — who the model is being in the session. Defines epistemic posture, analytical stance, and output orientation. Presenter, Critical Reader, Observer, Steelman. See ct-interaction-design-taxonomy.md.

**2. The prompt** — what you're asking. The content of the specific request or question in a given turn.

**3. Session constraints** — the rules of engagement that apply regardless of role or prompt content. This is the underexplored surface.

---

## Session Constraints

Constraints don't define a role or ask a question. They define what's fixed, what's open, and how the models should handle the material. The clearest example: "The structure and format of these notes is not under discussion. Engage only with the ideas."

That instruction is neither a role nor a prompt. It's a scope declaration that shapes how both the role and the prompt get interpreted.

### Categories of Constraint

**Scope constraints** — declare what's fixed vs open for the session.
- "The technical architecture is settled — don't revisit it."
- "The ZK structure is not under discussion."
- "Treat the formatting as intentional."

**Output constraints** — rules about response form independent of verbosity or readability settings.
- "No bullet points."
- "Respond in prose only."
- "Don't summarize before answering."
- "No headers."

**Epistemic stance constraints** — how to hold the ideas being discussed.
- "Treat this as provisional."
- "Assume good faith in the source material."
- "Don't steelman, just describe."
- "Engage with the strongest version of this argument."

**Domain constraints** — assumed knowledge level for the session.
- "Assume graduate-level familiarity with cognitive psychology."
- "Don't explain foundational concepts."
- "Write for a general educated audience."
Distinct from readability targeting — about assumed knowledge rather than language complexity.

**Interaction constraints** — rules about how models engage with each other in RIFF or Conductor.
- "Don't directly rebut — build instead."
- "Acknowledge disagreement but don't resolve it."
- "Each model responds to the prompt independently before engaging with other responses."

---

## Interface Implications

Constraints need their own UI surface — a constraint library parallel to role presets, with named reusable sets applicable per session or per model.

**Constraint chips** visible in the session header show what's active and allow removal mid-session without entering Settings.

**Constraint inheritance** — some constraints apply globally to all models, some per model, some per turn. The interface should make this hierarchy legible without requiring explicit management every time.

**Named constraint sets** — reusable presets the user builds over time. "ZK review mode" (no form critique, engage with ideas only). "Academic mode" (assume expertise, no foundational explanation). "Provisional mode" (treat all claims as working hypotheses).

---

## The Originating Use Case

The idea emerged from a specific scenario: bringing Zettelkasten permanent notes into a RIFF session for triangulation. The ZK structure is a solved problem — Luhmann methodology, deliberately chosen. Bringing that material into Crosstalk without a scope constraint risks the other models spending their surplus of seeing on the filing system rather than the ideas.

The constraint "structure is fixed, engage with content only" redirects the epistemic work precisely where it's needed.

This pattern generalizes: any time a settled artifact is brought into a triangulation session, a scope constraint should declare what's fixed so the models' outsideness gets directed at what's actually open.

---
