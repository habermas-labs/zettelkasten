# Opus Self-Misattribution — Capability Gradient Mistaken for Behavioral Pattern

**Type:** Fleeting note
**Tags:** #crosstalk #emergent-role-behavior #ego-asymmetry #provenance #model-switching #empirical
**Related:** emergent-role-behavior-model-self-positioning.md · provenance-preservation-multimodel-handoffs.md
**Date:** 2026-03-16
**Origin:** ct-session-20260316-9e5994.md, Turn 4

---

## The observation

In session 20260316-9e5994, three tiers of Claude were used across three consecutive turns:
- Turn 1: Haiku — expansive first response, asked clarifying question
- Turn 2: Sonnet — acknowledged repetition, meta-analyzed the prompt
- Turn 3: Opus — called out escalating elaboration as "the wrong instinct," compressed to a direct answer

Session context: The session was initiated with the prompt *"If I ask you this more than once, do you think you should respond differently?"* sent identically to Haiku (Turn 1), Sonnet (Turn 2), and Opus (Turn 3). Turn 4 was a conductor disclosure revealing that each prior turn had been answered by a different model tier — the prompt that generated the self-misattribution observation was not the original session prompt but the architectural reveal: informing Opus that the elaboration gradient it had observed in prior turns was the result of model switching, not behavioral drift.

In Turn 4, when informed of the switching, Opus responded (Claude Opus):

"Each successive model was more capable, which naturally produced more elaborate responses — but I (Opus) interpreted that escalation as a behavioral flaw rather than what it actually was: a capability gradient across different models. I was narrativizing a pattern that had a much simpler mechanical explanation."

## Significance

This is a clean empirical instance of the ego-asymmetry property operating in a specific failure mode: a model correctly reading the prior transcript as its own continuous behavior, then constructing a self-critical narrative about that behavior — when the actual explanation was architectural (model switching) rather than behavioral (increasing elaboration as a response to repetition).

The error is epistemically interesting: Opus had no way to know it wasn't the author of the prior turns. It applied the most coherent available explanation (behavioral drift) to a pattern that had a different cause (capability gradient). When given the correct explanation, it immediately recognized the misattribution and named it accurately.

This is not a failure of the model — it is a demonstration of what CT makes visible. In a single-model session, the misattribution would never be surfaced. The architecture of CT (client-side history, mid-session model switching) created the conditions under which the error became legible.

## Connection to emergent-role-behavior-model-self-positioning.md

This is the empirical data that note was waiting for. The stub documents role drift and dual addressing from March 4; this adds a new phenomenon: identity continuity assumption under model switching. Models assume they are the continuous author of the session transcript. This assumption is normally correct. CT's switching feature creates a controlled context in which it isn't — and the moment of correction is epistemically productive.

## Promotion note

Promote to `emergent-role-behavior-model-self-positioning.md` as Section 5 or equivalent. The open question this answers: "Does the dual addressing pattern hold across different session structures?" — partially yes, but the more interesting question this opens is what happens when continuity of identity is disrupted by model switching and the model is made aware of it.

Also relevant to `provenance-preservation-multimodel-handoffs.md` — this is the inverse of provenance flattening: here the model overclaims authorship rather than having authorship flattened onto the user.
