# Crosstalk Interaction Design Taxonomy: Roles, Modes, Meta-Structure

**Type:** Concept note
**Tags:** #crosstalk #interaction-design #modes #roles #meta-structure
**Related:** vnenakhodimost-surplus-of-seeing.md · CT-TRACKER.md entries 040–047
**Date:** 2026-03-03

---

## The Three-Level Taxonomy

Crosstalk's interaction design operates at three distinct levels. Conflating them leads to architectural confusion; keeping them distinct clarifies what belongs where.

### Level 1: Roles
Predefined system prompt configurations for individual models. A role defines what a model is instructed to do and how it frames its output within a session.

Current role presets (initial set):
- **Presenter / Developer** — constructs the strongest affirmative case for an idea
- **Critical Reader** — adversarial pressure-testing; peer reviewer function
- **External Observer** — meta-commentator on the shape of the conversation; structural instantiation of Bakhtinian outsideness (vnenakhodimost')
- **Synthesizer** — finds throughline and convergence points across outputs
- **Steelman** — best possible case for a position the model might otherwise resist

Roles are building blocks. They are not modes. A role without a mode context is just a system prompt.

### Level 2: Modes
Combinations of roles assigned across models, plus the rules governing how models interact within a session. Different modes serve different epistemic purposes.

Current modes:
- **Parallel** — independent simultaneous responses; no roles; no inter-model awareness
- **Conductor** — sequential; each model sees prior responses before answering; roles optional
- **RIP (Rapid Idea Prototyping)** — divergent, generative; models have ambient awareness of each other's outputs; roles counterproductive; idea coordinate system (041) is native to this mode
- **RIFF** — structured dialogue; role presets load-bearing; productive friction by design; grounded in Bakhtinian dialogism
- **Focus** — single-model; Crosstalk's epistemic infrastructure wrapped around a solo session; gains value from meta-structure even without multi-model interaction

### Level 3: Meta-Structure
Session-level behavioral rules enforced at the application level. Meta-structure governs:
- Turn sequencing
- Inter-model awareness rules
- Index management (for RIP)
- Mode entry conditions
- Mode exit conditions and offboarding workflow

Meta-structure cannot be fully captured in system prompts alone. The application must know it is in a mode and behave accordingly — the models' role prompts are necessary but not sufficient.

**Mode exit** is a first-class concept in meta-structure. Exit is always user-triggered. It opens an exit strategy workflow (047) that treats session end as an epistemic moment rather than a hard stop.

---

## Key Distinctions

**Roles vs. modes:** A role is what one model does. A mode is the structure within which multiple models (or one model) operate together.

**Modes vs. meta-structure:** A mode defines the epistemic purpose and role configuration. Meta-structure defines the session-level rules that make the mode function as intended at the application level.

**Pause vs. disable:** Pause preserves session state and index continuity. Disable breaks it. RIP sessions require all models to be active or paused — not disabled.

**Focus mode vs. native interface:** Focus mode is not just a cost-reduction path to a single model. It is a single-model session with Crosstalk's meta-structure wrapped around it, including the exit scaffolding that native interfaces do not provide.

---

## RIP–RIFF as a Two-Phase Methodology

RIP and RIFF are designed to work in sequence:

1. **RIP first** — expand the possibility space; generate branches; follow tangents; build the idea index
2. **RIFF then** — bring structured friction to bear on the richest branches; role assignments have more material to engage with

The idea coordinate system (041) is the connective tissue: coordinates generated in RIP become the reference points for directing RIFF attention. "Everybody look at A3" is both a RIP navigation command and a RIFF session seed.

---

## Theoretical Grounding

The RIFF mode and the role of the External Observer are theoretically grounded in Bakhtin's dialogism — specifically outsideness (vnenakhodimost') and the surplus of seeing. See permanent note: vnenakhodimost-surplus-of-seeing.md.

The broader claim: multi-model triangulation is not just parallel task execution with multiple opinions aggregated. It is an epistemic practice in which meaning becomes visible at the boundary between model perspectives — meaning that would remain invisible inside any single model's framework.
