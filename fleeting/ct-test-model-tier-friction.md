# Intra-Model Tier Friction — Experimental Design

**Type:** Fleeting note
**Tags:** #crosstalk-theory #model-selection #experimental-design #divergence #friction
**Related:** emergent-role-behavior-model-self-positioning.md · ct-epistemic-training-framework.md
**Date:** 2026-03-14
**Status:** Capture

---

Core question: Does divergence occur between tiers of the same AI family (e.g., Haiku vs. Sonnet vs. Opus within Claude), and if so, does it carry the same epistemic signal as cross-LLM divergence?

Origin: CT walk session 2026-03-14. Cross-LLM friction observed in live sessions has raised the question of whether friction is architectural (different training, different data, different values) or depth-of-reasoning (System 1 vs. System 2 adjacent processing). Intra-family tier comparison holds architecture roughly constant and varies reasoning depth — isolating the variable that cross-LLM comparisons cannot.

Rough cognitive-register analogy: Haiku is fast/intuitive (System 1 adjacent), Sonnet is balanced, Opus is deliberative/slow (System 2 adjacent). Whether this maps onto differential divergence patterns is the empirical question.

Experimental design:
- Run the same prompt simultaneously to two or three tiers of the same family (e.g., Haiku + Opus, or all three)
- Compare divergence patterns to a baseline cross-LLM session on the same prompt
- Note: does intra-family divergence appear at all? If so, is it qualitative (different positions) or tonal/depth (same position, different confidence or elaboration)?
- Secondary comparison: does a Haiku + Opus pairing produce more or less friction than Claude + ChatGPT on the same prompt?

Hypothesis: intra-family divergence, if it exists, will be primarily depth-of-reasoning divergence rather than positional divergence — the models will agree more often but differ in how far they develop a position, how many qualifications they surface, and how much uncertainty they acknowledge. Cross-LLM divergence is more likely to be positional — different conclusions, not just different elaboration depth.

Implication for CT theory: if the hypothesis holds, it suggests two distinct sources of epistemic value in multi-model triangulation — architectural divergence (cross-LLM, positional) and depth divergence (intra-family, elaboration). These may be complementary rather than redundant. A session combining both could in principle surface both kinds of signal.

Implication for UI: CT-097 (model version selection) becomes more than a settings convenience feature — it is the mechanism for accessing depth divergence as a distinct epistemic mode. Framing in documentation matters: this is not "pick your preferred model" but "select your reasoning depth configuration."

Forward: cross-LLM friction session notes (pending)
