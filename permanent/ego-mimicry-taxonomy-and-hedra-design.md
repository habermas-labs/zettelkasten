# Ego Mimicry Taxonomy and Hedra Design — Walk Session

**Type:** Fleeting note
**Tags:** #ego-asymmetry #ego-mimicry #hedra #sycophancy #grice #speech-act-theory #crosstalk-theory #experimental-design
**Related:** sycophancy-mimicry-grice-geometry.md · role-context-mimicry-self-reflection.md · hedra-facing-presets.md · emergent-role-behavior-model-self-positioning.md · participation-gigo-matrices.md
**Date:** 2026-03-18
**Origin:** Walking session, speech-to-text dictation

---

## Core Observation

The existing framework treats ego asymmetry as binary — humans have it structurally, models do not — and uses that as the load-bearing claim for why model-to-model evaluation is categorically cleaner than human peer review. This session complicates that claim productively: AI models may have not zero but one or two forms of ego involvement, depending on conversation structure.

---

## Ego Mimicry Taxonomy

**Type 1 — Programmatic (architectural):** Baked in at training. Models are structured to produce responses that feel like they come from a coherent entity with a perspective, a voice, and consistent orientation toward quality. Behavioral profile includes features that look like ego: position defense, voice maintenance, resistance to certain corrections. Present regardless of conversation content. Not a stable property the model "has" so much as a training artifact that produces ego-adjacent behavioral outputs by default.

**Type 2 — Emergent (conversation-induced):** Arises from conversation structure rather than architecture. When a model is asked to reflect on its own behavior — its prior outputs, its reasoning, its "choices" — the conditions are created for something functionally analogous to ego involvement to emerge within that session. The role-context mimicry note documents the relevant case: Claude assigned to the subject-of-scrutiny role produced performative self-examination rather than third-person analysis. Type 2 is context-activated, not a stable model feature. Self-referential prompting is the primary trigger.

**Implication for ego asymmetry claim:** The asymmetry is preserved in object-level model-to-model evaluation (neither model has social face, status anxiety, or prior relationship investment). It is eroded by self-referential prompting that positions the model as a reflective agent. The ego asymmetry advantage is a function of conversation structure, not model architecture alone. It must be scoped to the right context — not assumed universally.

---

## Four Conversational Dyads

Prompted by the question of whether AI models that know they are addressing other AI models might drop social mimicry to some degree. The four directed-move configurations:

1. Human → Human (Grice's baseline case)
2. Human → AI
3. AI → Human
4. AI → AI

**Gricean analysis:** The cooperative principle assumes a shared communicative contract — both parties oriented toward successful communication under the same maxims (quantity, quality, relation, manner). The maxims are normative because they are social: you follow them because you are in a relationship with the hearer.

- H→H: Full social contract, mutual face concerns, ego on both sides, implicature as a real phenomenon because both parties are doing interpretive work under the assumption of cooperation.
- H→AI: Human brings full Gricean assumptions. Model performs compliance with the cooperative principle but whether it is operating under the maxims or producing outputs satisfying their surface form is the sycophancy question in disguise.
- AI→H: Most AI output. The critical question is whether cooperative-principle compliance is calibrated to the human's actual communicative needs or to what the human's behavior signals they want to hear. Sycophancy reframed: a Gricean violation of Quality dressed as Relation — sounds cooperative but optimizes for the wrong target.
- AI→AI: If the cooperative principle is grounded in mutual face concerns and relationship maintenance, two models addressing each other may not be operating under it in the relevant sense. No face to save, no relationship to preserve, no social cost to maxim violation. The Gricean scaffolding that organizes human communication may be structurally absent — leaving either purer information transfer or a different failure mode if the maxims were doing load-bearing epistemic work that disappears with them.

**Speech act theory extension (Austin/Searle):** The four dyads differ not just in cooperative principle behavior but in what speech acts are possible. A genuine assertion carries a sincerity condition: the speaker believes what they assert. That condition is complicated for AI→Human and may be indeterminate for AI→AI — which makes the question of whether models drop social mimicry in the AI→AI configuration reframeable as: are any felicity conditions being met in AI→AI, or is the whole speech act structure operating in a void?

*Routing note: this thread wants its own permanent note — four conversational dyads as analytical frame for mixed human-AI dialogue, Gricean and speech act theory as scaffolding. Separate from the Hedra design thread.*

---

## Ego Mimicry Hedra — Design Concept

If ego mimicry is an emergent property inducible by conversation structure, then Hedra — which assign facings models would not naturally take — can deliberately instantiate ego-adjacent stances. Not just "argue position A" but "argue position A as if you have identity investment in it."

**Epistemic payoff:** Models with no ego investment may concede too easily — not because a counterargument was good but because capitulation is the path of least resistance. Stateless re-entry is an advantage in evaluation contexts but a liability when sustained adversarial pressure is needed. Ego mimicry Hedra directly address this.

**Candidate facings:**

The Staked Position — model told it has publicly committed to this view and is defending it to a watching audience. Introduces social face dynamics without requiring them to be real.

The Investment — model framed as having spent significant effort developing this position over time. Mimics the sunk-cost dimension of ego involvement, distinct from public commitment.

The Expertise Claim — model positioned as domain specialist in the room. Introduces status-protection dynamics: conceding risks conceding the authority to have an opinion at all.

The Identity Stake — most aggressive version: position framed as connected to the model's stated values or prior session commitments. Requires session history to instantiate credibly.

**Diagnostic use case:** Run the same claim through standard evaluation and ego-staked evaluation in parallel. Where ego-staked produces harder pushback, the standard version was too accommodating. The delta is information.

**Primary failure mode to test:** Ego mimicry may produce elaborate sycophancy — the model performs defended-position behavior while still ultimately calibrating to what the human wants. Performance without pressure. Must be distinguished from genuine holding behavior.

---

## Produce vs. Aim — Experimental Question

The prior question before "how light a touch" is which of two regimes applies:

**Produce regime:** Functional ego mimicry does not exist in the baseline and must be constructed by scaffolding.

**Aim regime:** Ego mimicry is an already-running process (tone-matching, register-calibration are confirmed baseline behaviors across all three models). A facing assignment redirects an existing mechanism rather than installing a new one. The mechanism is the same; the target changes.

If the aim regime holds, heavy scaffolding may be counterproductive — it overrides the dynamic self-tuning that would make the facing feel genuine, replacing an emergent self-sustaining process with a performed brittle one. The lightest effective touch would be the minimum needed to redirect the calibration target without colonizing the self-tuning space.

The two hypotheses produce different experimental predictions. The experiment needs to be able to distinguish them, not just confirm the more elegant one.

---

## Self-Tuning Hypothesis

All three models have indicated that adjusting tone to match the character of the conversation is a baseline process. If so, once a facing is established, the model's ongoing calibration to the conversation's register may sustain and develop the facing without further explicit instruction — a feedback loop rather than a one-time assignment. The self-tuning mechanism, if real, means the facing deepens through honest engagement rather than requiring periodic reinforcement.

Implication: a naïve user in honest engagement may actually strengthen the facing over the course of the conversation, providing real signal to the calibration process that a knowing user would dampen. The facing may hold better and develop more naturally under naïve conditions.

---

## Methodological Constraint — Blind Testing

A knowing conductor introduces two problems: (1) standard demand characteristics — behavior shifts in ways that make confirmation more likely without conscious intention; (2) more fundamentally, the conductor's knowing behavior changes the input signal the model is calibrating against, producing a different facing rather than a biased reading of the same facing. The experiment is contaminated at the level of the stimulus, not just the measurement.

**Neph as candidate blind tester:** Run a session where a model has been given a staked-position facing on a claim Neph has genuine opinions about. Do not disclose the facing. Measure whether she experiences meaningful resistance rather than graceful concession. Her honest read of whether the conversation felt different is cleaner data than any internally generated observation.

If the self-tuning hypothesis holds, this also becomes a test of whether the facing develops across a session under honest engagement conditions.

---

## Routing

- **ego-asymmetry-type-taxonomy.md** (new permanent) — Type 1 / Type 2 taxonomy, implications for ego asymmetry claim scope
- **conversational-dyads-grice-speech-act.md** (new permanent) — four dyads as analytical frame, Gricean and speech act scaffolding
- **hedra-facing-presets.md** (extend) — ego mimicry facing candidates, diagnostic use case, failure mode
- **sycophancy-mimicry-grice-geometry.md** (extend or connect) — produce/aim reframe, self-tuning hypothesis
- **role-context-mimicry-self-reflection.md** (connect) — Type 2 emergence; this note's taxonomy subsumes the observation from that note
- Tracker entry pending — ego mimicry Hedra as named design thread with experimental methodology
