# Fleeting — Information Asymmetry in CT Session Architecture

**Type:** Fleeting note
**Tags:** #crosstalk #session-architecture #distributed-metacognition #conductor #information-asymmetry #design-gap
**Related:** `distributed-metacognition.md` · `human-ai-asymmetry-inventory.md` · `ct-tetras.md` · `ct-session-auth-privacy-architecture.md`
**Date:** 2026-05-27
**Status:** Capture — design principle gap; routes to distributed-metacognition.md and ct-tetras.md

---

## Origin

Identified by DeepSeek in CT session 20260527 (YB trio), in the analysis of Grok and Mistral's responses on Tetra/Hedra generalizability. Named as the gap that both Grok and Mistral's accounts of distributed metacognition left unaddressed.

---

## The Asymmetry

In CT's current architecture, the conductor holds structural information advantages that AI models do not:

- The conductor sees all parallel column outputs simultaneously
- The conductor holds the full session history including their own routing decisions
- The conductor knows which model received which forwarded content and in what sequence
- The conductor holds the metacognitive overview of the entire session

The AI models see only what has been directed to them. They do not have access to parallel outputs from other models unless explicitly forwarded. They cannot observe the conductor's routing decisions or their rationale.

---

## Why This Matters

This structural information asymmetry is the *actual* source of the metacognitive imbalance in CT sessions — more fundamental than the cognitive asymmetries documented in `human-ai-asymmetry-inventory.md`. Those asymmetries are about intrinsic cognitive architecture differences between humans and AI. This one is architectural: a feature of how CT's session design distributes information, not a feature of what minds are.

For distributed metacognition to be genuinely symmetric — the design aspiration articulated in `distributed-metacognition.md` — the models would need access to:

- Each other's uncertainty signals and confidence levels
- Some awareness of the conductor's routing decisions and their rationale
- The ability to observe patterns across the session rather than only their own thread

DeepSeek's formulation: "If distributed metacognition is to be genuine, the geometry must eventually make the conductor's overview visible and contestable — not just their individual utterances."

---

## Distinction from Cognitive Asymmetries

This is distinct from the six cognitive asymmetries in `human-ai-asymmetry-inventory.md` in an important way. Those asymmetries are features of what human and AI cognition *are* — memory architecture, temporal structure, embodiment, ego machinery. This asymmetry is a feature of what CT's session *does* — how it distributes information across participants.

The implication: this asymmetry could be reduced by design without changing anything about the underlying cognitive architectures. It is an architectural choice, not an ontological given. Whether reducing it is desirable is a separate question — the conductor's privileged overview may be part of what makes the conductor role epistemically valuable.

---

## Design Questions This Opens

- Should CT provide models with access to each other's column outputs as part of the base interaction geometry, rather than requiring the conductor to forward explicitly?
- Could a "session transparency" layer show models a summary of routing decisions and parallel responses without full access?
- Does making the conductor's overview visible to models undermine or enhance the conductor's epistemic function?
- Is there a version of distributed metacognition that is genuinely symmetric without collapsing the conductor's structural role?

---

## Relationship to the Participation Question

This asymmetry also bears on the distributed mind participation question developed throughout the same session. Grok's formulation — "participation remains derivative, depends on the human continuing to treat the model's output as carrying normative force" — is partly a consequence of this information asymmetry. Models cannot fully participate in the metacognitive regulation of the session because they lack the overview the conductor holds. Closing the information asymmetry (even partially) would change what participation is available to the models.

---

## Forward

- Add to `distributed-metacognition.md` forward connections: information asymmetry as a structural barrier to symmetric distributed metacognition
- Add to `ct-tetras.md` open questions: "How does the conductor's information asymmetry shape what distributed metacognition is achievable in current CT architecture?"
- Consider as a design principle for Hedras specifically: Hedra design should account for whether additional facings increase or decrease productive information asymmetry
