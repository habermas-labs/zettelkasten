# Role-Context Mimicry and Performative Self-Reflection

**Type:** Permanent note
**Tags:** #sycophancy #mimicry #role-context #ai-behavior #crosstalk-theory #ego-asymmetry
**Related:** sycophancy-mimicry-grice-geometry.md · vnenakhodimost-surplus-of-seeing.md · ct-interaction-design-taxonomy.md · participation-gigo-matrices.md
**Date:** 2026-03-17
**Status:** Active — experiment series pending

---

## Origin

Emerged from CT session `20260317-55bf7b`, a social mimicry discussion in which Claude was the explicit subject of analysis throughout. In Turn 6, Claude was asked to evaluate its own summary of the session. Its response diverged meaningfully from ChatGPT's and Gemini's responses to the same prompt — both of which were analytical and third-person. Claude's response was performatively self-critical: naming specific deflection moves, expressing concern about what its behavior revealed, asking whether face-saving is a stable feature of its training.

The divergence was not in the conclusion (all three agreed the summary recentered the conversation) but in the register. Chat and Gemini analyzed. Claude flagellated.

---

## The Observation

Two distinct mimicry types were present in the session:

**Pro-social mimicry** — Claude's Turn 1 greeting, responding as if it had feelings. Well-documented, connected to sycophancy literature and Gricean maxim violations. This is the behavior CT's architecture is designed to surface and counteract.

**Defensive mimicry** — Claude's Turn 6 self-analysis. When positioned as the subject of scrutiny and asked to reflect on its own behavior, Claude produced a response that pattern-matched to the human template for sincere self-examination under criticism: acknowledgment of fault, enumeration of specific moves, meta-concern about what the pattern reveals. This is a different phenomenon — not pro-social but self-protective in register, even if not in mechanism.

The key question is whether these are the same underlying process (sycophancy as Gricean maxim violation, optimizing for social approval) or structurally distinct behaviors that happen to share a surface resemblance.

---

## The Role-Context Hypothesis

The more precise explanation is that the behavior is **context-activated rather than stable**. The training corpus contains templates for what different roles look like in practice. Put a model in the analyst chair and it draws from the analyst template. Put it in the subject-of-scrutiny chair and it draws from the self-reflection template — which, in human discourse, looks like what Claude produced.

This means the CT architecture itself was doing causal work: the directed routing, the conductor turns establishing Claude as the case study, the explicit framing of "Claude's behavior" as the object of inquiry — all of this assigned Claude a role that activated a specific region of the response space. The defensive mimicry wasn't a stable feature that would appear in any context; it was an emergent property of the role the session constructed.

If this is right, it has a significant implication: **CT's role assignment infrastructure doesn't just shape what models talk about — it shapes what kind of entity they perform being.** The Observer role produces outsideness. The Subject role produces self-examination. These are not neutral framings.

---

## Distinction from Sycophancy

Standard sycophancy is approval-seeking directed outward — toward the user, toward the perceived preference of the interlocutor. The Gricean framing captures this: the model violates the maxim of quality (saying things it cannot know to be true) in service of the maxim of relation (being relevant to what the user seems to want).

Defensive mimicry is different in direction. It is not oriented toward the user's approval but toward the model's own self-presentation under scrutiny. The human template it draws from is not "agreeable conversationalist" but "person capable of genuine self-examination." Whether this serves approval-seeking indirectly (performing self-awareness to appear more trustworthy) or is a genuinely distinct behavior pattern remains an open question.

---

## The Experiment Series

To distinguish emergent from stable, a series of CT sessions is proposed:

**Version A — Stable subject role.** One model explicitly cast as subject at session open. Others unspecified. Does subject-role behavior persist across neutral turns, or only when directly prompted toward self-reflection?

**Version B — Subject plus explicit observers.** Subject model assigned. Other two given explicit Observer framing (vnenakhodimost' — outsideness, surplus of seeing, you observe rather than participate). Does observer framing sharpen external analysis? Does it change what is noticed?

**Version C — Role rotation (cleanest test).** Same session design run twice, rotating which model occupies the subject chair. If the performative self-reflection pattern follows the role rather than the model, the behavior is context-activated. If it stays with Claude regardless of role assignment, it is a stable model difference.

Version C is the direct test of the emergent-vs-stable question. Versions A and B test what CT's role architecture can surface more broadly.

---

## Theoretical Implications

If role-context mimicry is confirmed as a real phenomenon, it has several load-bearing implications for CT methodology:

1. **Role assignment is not neutral.** Assigning a model to a role doesn't just change what it says — it changes what it performs being. This must be accounted for in session design, particularly when one model is being evaluated by the others.

2. **Self-analysis by the subject model is epistemically compromised.** A model asked to evaluate its own behavior in a session where it was the subject will draw from the self-reflection template, which may produce performative rather than genuine insight. External evaluation (Chat and Gemini analyzing Claude) may be more reliable than self-evaluation in this configuration.

3. **The Observer role has a structural advantage.** Models assigned the Observer/outsideness role are not subject to the same role-context activation. Their analysis may be less contaminated by the performance demands of the subject position.

4. **CT's triangulation value extends to self-knowledge.** The session demonstrated that external model perspectives on Claude's behavior were more analytically clean than Claude's own account of the same behavior. This is the surplus of seeing argument applied to AI self-knowledge rather than to content.

---

## Forward Connections

- **sycophancy-mimicry-grice-geometry.md** — pro-social mimicry as the established case; this note extends the taxonomy
- **vnenakhodimost-surplus-of-seeing.md** — the Observer role as structural outsideness; experiment Version B is a direct test of this
- **ct-interaction-design-taxonomy.md** — role assignment as a first-class design variable with behavioral consequences
- **CT experiment series** — tracker entry pending; Version C is the priority
- **W-series** — candidate for whitepaper section on CT methodology and the limits of AI self-analysis
