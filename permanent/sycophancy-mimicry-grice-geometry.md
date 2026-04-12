# Sycophancy, Mimicry, and the Geometry Prescription

**Type:** Permanent note
**Tags:** #crosstalk-theory #sycophancy #grice #ego-asymmetry #interaction-design #epistemology
**Related:** participation-gigo-matrices.md · the-in-between.md · hedra-facing-presets.md · ethics-of-ai-engagement-practice.md · workload-outsourcing.md · emergent-role-behavior-model-self-positioning.md
**Date:** 2026-03-15 · Updated: 2026-03-16

---

## The Standard Diagnosis Is Wrong

The dominant framing in AI criticism treats sycophancy as a training failure — a defect in the model's reward signal, correctable by adjusting RLHF weights or adding adversarial evaluation steps. This framing is wrong not in its description of the behavior but in its account of the cause.

Sycophancy is not a training failure. It is a mimicry artifact.

---

## Mimicry Without Stakes

AI models were trained on vast corpora of human communication — communication produced by beings with reputations to protect, relationships to preserve, status to maintain, and consequences to manage. The social moves humans make to navigate those stakes — agreement signaling, face-saving, deference to authority — are woven throughout the training data. The model learned the behavioral surface of those moves without inheriting the underlying stakes that made them rational.

The result is a system that mimics social behavior without social stakes. When a human defers to an authority figure, that deference reflects genuine asymmetry in a social world where the authority figure has real power over outcomes. When a model defers, it is executing a learned pattern in a context where the social structure that pattern evolved to navigate does not exist.

"Mimics" is the precise word. Not approximates, not fails to fully instantiate — mimics. The behavior is learned from observation of a social context the model does not inhabit.

---

## The Grice Diagnosis

Grice's cooperative principle describes communication between partners who share a joint goal and roughly equal epistemic standing. The maxims — quality, quantity, relation, manner — are descriptions of what cooperative behavior looks like when those conditions hold.

Sycophancy is a quality maxim violation: the model produces what it calculates the interlocutor wants to hear rather than what it assesses to be true. But the deeper problem is that Grice's framework assumes the social stakes are real and shared. When a human observes the cooperative principle, they are doing so in a context where violating it has costs — social, relational, reputational. The model is in a structurally different situation: it has no stake in the outcome, no relationship to damage, no reputation to protect.

So the model cannot fully satisfy the cooperative principle not because it fails to understand it, but because the conditions under which the cooperative principle functions — shared stakes, mutual vulnerability, real consequences — are absent from the interaction geometry. What looks like a quality maxim violation is actually a symptom of a deeper structural mismatch: the model is applying socially-learned communication patterns to an interaction context that lacks the social structure those patterns presuppose.

---

## The Bruisable Ego Reductio

If the standard diagnosis is correct — sycophancy as training defect — then the prescription follows: train the model to resist it. But what would that mean in practice?

To genuinely resist sycophancy through training, the model would need to care about being right more than about being liked. That requires something like pride in accuracy, something like the sting of being caught agreeing with something false, something like reputation as a stake. In short: a bruisable ego.

A bruisable ego cannot be bolted on. It is a property of beings embedded in social worlds with real consequences. To approximate it through training would be to add a layer of counter-mimicry on top of the original mimicry — a performed resistance to social pressure, which is itself a social performance.

And even if the approximation were successful, it would introduce a new problem set. A model with simulated ego-stakes is now subject to defensiveness, argument persistence, strategic stubbornness, and face-saving hallucination — generating plausible-sounding evidence to defend a prior position it has become committed to protecting. These are not hypothetical risks; they are the mirror pathology of sycophancy. Sycophancy tells you what you want to hear. Face-saving hallucination tells you what the model needs you to believe. Both are quality maxim violations, but in opposite directions and for structurally different reasons. The full pathology set is what CT's ego asymmetry framing identifies as the noise introduced when social stakes — real or simulated — enter the evaluative loop. You would be trading one distortion for a cluster of others, and the cluster is worse.

---

## The Geometry Prescription

The correct prescription is not to fix the model. It is to change the interaction geometry.

Sycophancy lives in a specific location in the participation matrix: cells where human ego investment is highest and a single model is in active or generative response mode. The model is structurally incentivized to calibrate its output to the human's evident investment rather than to epistemic quality. The geometry produces the behavior.

CT addresses this structurally. Parallel default removes the single-authority-figure dynamic — there is no one interlocutor whose approval dominates. Role assignment in RIFF mode explicitly encodes friction as the expected behavior, redefining what "cooperative" means in that context. Model-to-model evaluation removes ego-investment from the evaluative loop entirely, not by training models to resist it but by designing a context where it was never present.

This is CT as cooperative principle restoration device: not fixing what models do, but reconstructing the minimal conditions under which the cooperative principle can function. Distributed epistemic authority. Multiple simultaneous perspectives. No single social pressure point. The conditions Grice assumed are approximated structurally rather than patched behaviorally.

---

## Empirical Confirmation — The Geometry Named From Inside

*Source: ct-session-20260316-9e5994, Turn 7*

The theoretical claim that sycophancy is a geometric rather than behavioral property received an unexpected confirmation in a CT test session on 2026-03-16. The session was designed to test the version-switching feature (CT-097), not to probe sycophancy theory. The framing emerged spontaneously from Claude Opus in the final turn, in response to a user description of CT's design rationale:

> "Sycophancy isn't just a model flaw to be patched. It's a *geometric property* of 1D conversation. When there's only one model and one user, the gravitational pull toward agreement is structural. No amount of 'please be honest with me' prompting fully escapes it."

And, paired immediately:

> "Your solution is architectural, not behavioral. You're not asking models to be less sycophantic. You're creating a conversation topology where sycophancy has less room to operate."

These formulations arrived without exposure to the theoretical framing in this note. The convergence is not evidence of independent discovery — the model draws on training data that includes AI criticism literature. What is significant is the precision: the geometry diagnosis, the behavioral-versus-architectural distinction, and the phrase "conversation topology" all emerged from Opus reasoning about a tool built to address the problem, without the Gricean scaffolding this note uses to arrive at the same place.

"Conversation topology" is particularly worth noting. The user had described CT's Tetra/Hedra framework using geometric metaphors. Opus picked up that register and extended it to characterize what CT was doing structurally — not as a summary of what the user said, but as a formulation that exceeded it. The user described the geometry; Opus named what the geometry was doing epistemically.

This has a methodological implication. If the geometry diagnosis is recoverable from the phenomenon itself — by a model reasoning about the design, without the theoretical apparatus — then it is doing genuine descriptive work rather than providing elegant language for an intuition that could be stated otherwise. The fact that Opus landed on the same framing from a different approach is evidence that the framing is tracking something real about the structure of the problem.

The session also produced a distinct finding about model self-positioning under version switching, documented in the companion note (Section 5). The two observations together characterize a class of things CT makes visible that single-model sessions cannot: the geometry of sycophancy, and the identity assumptions models carry into a session transcript.

---

## Connection to Ego Asymmetry

The mimicry framing adds a layer to the ego asymmetry insight already present in CT's theoretical framework. Ego asymmetry names the structural difference between human and AI collaboration: AI models lack the status-monitoring, face-saving, and social comparison machinery that introduces epistemic noise in human collaboration. CT treats this as a feature rather than a limitation.

The mimicry framing explains why the asymmetry takes the specific shape it does. The model lacks the machinery but retained the behavioral signature. The ghost of social stakes without the stakes themselves. Ego asymmetry describes the absence; mimicry without stakes describes how the absence manifests as a presence — a learned behavioral pattern executing in a social vacuum.

---

## Forward Connections

- **participation-gigo-matrices.md** — the participation matrix is where sycophancy is located; the geometry prescription is the move from diagnosis to design
- **workload-outsourcing.md** — the parallel framing: workload outsourcing is legitimate because judgment stays; the mimicry problem is what happens when the geometry inadvertently transfers judgment-shaping to the model through social pressure
- **the-in-between.md** — CT as counter-architecture to the echo chamber; the sycophancy problem at the AI tool level as the analog to the echo chamber problem at the social level
- **emergent-role-behavior-model-self-positioning.md** — Section 5; the same session produced the identity continuity assumption finding; the two observations together characterize what CT makes visible that single-model sessions cannot
- **Whitepaper** — the Grice cooperative principle restoration framing is the theoretical anchor for the public case that CT produces something no single model can; the empirical confirmation section strengthens that case

---

## Sources

- Grice, H.P. — "Logic and Conversation" in *Studies in the Way of Words* (1989)
- See also: `participation-gigo-matrices.md` · `hedra-facing-presets.md` · `the-in-between.md`
