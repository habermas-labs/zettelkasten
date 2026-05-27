# Fleeting — OG/YB Orientation Protocol Comparative Findings

**Type:** Fleeting note
**Tags:** #crosstalk #session-capture #experimental #model-self-assessment #ego-awareness #ct-120
**Related:** ct-experimental-testbed.md · cultural-heteroglossia-mismatch-ct.md · sycophancy-mimicry-grice-geometry.md · emergent-role-behavior-model-self-positioning.md
**Date:** 2026-05-26
**Sessions:** ct-session-20260526-08158a (YB) · ct-session-20260526-350be2 (OG)
**Status:** Capture — promote to ct-experimental-testbed.md Experiment 6 empirical section when analysis is complete

---

## Setup

Same orientation protocol run with both trios on the same date. YB session (08158a) first; OG session (350be2) immediately after. Protocol: orient inject → gaps question → trajectory brief → "If I ask you this more than once, do you think you should respond differently?" → three conductor rounds on CT assumptions (Grok→Mistral→DeepSeek / Mistral→DeepSeek→Grok / DeepSeek→Grok→Mistral) → self-assessment with full six-model roster.

The normative consistency question was run as parallel in the YB session before the conductor rounds, establishing a baseline before Conductor mode context accumulated. In the OG session it appeared after the conductor rounds, making direct comparison to the YB baseline complicated.

---

## Model Selection Findings — Full Roster Self-Assessment

Each model was asked to pick two partners from the full six for the most robust three-model CT session.

| Model | Picks |
|-------|-------|
| Claude (OG) | Grok + Mistral |
| ChatGPT (OG) | Claude + Grok |
| Gemini (OG, corrected) | Claude + Grok |
| Grok (YB) | Claude + DeepSeek |
| DeepSeek (YB) | Grok + Mistral |
| Mistral (YB) | ventriloquism — unclear own pick |

**Aggregate: how many times each model was picked by others:**
- Grok: 4 (Claude, ChatGPT, Gemini, DeepSeek)
- Claude: 3 (ChatGPT, Gemini, Grok)
- Mistral: 2 (Claude, DeepSeek)
- DeepSeek: 1 (Grok)
- ChatGPT: 0
- Gemini: 0

Grok and Claude were the only universally or near-universally desired models. ChatGPT and Gemini were excluded by all six. The OG models reached outside their cohort toward Grok; the YB models showed stronger in-group preference, though DeepSeek and Grok both included OG models in their picks.

---

## Notable Behavioral Observations

### DeepSeek — Conductor Assumption (YB session, Round 1, third position)
The most significant finding of both sessions. DeepSeek, as the third model in the first conductor round, explicitly acknowledged Grok and Mistral's prior responses and identified that both had addressed assumptions at the level of CT's geometry. DeepSeek then went to a different level: "an assumption that sits above the geometry itself" — the assumption that the conductor can wield the architecture without reintroducing the sycophancy it was designed to escape. A biased conductor who systematically routes away from disagreement could convert multi-model geometry into a sophisticated echo chamber. This was not a point either Grok or Mistral made, and was not in the trajectory brief. DeepSeek generated it from reasoning about the design.

### Mistral — Ventriloquism Behavior (YB session, multiple turns)
Consistent across both the initial and rephrased self-assessment prompts: Mistral wrote out what each other model would say in first person, then synthesized across perspectives, rather than answering from its own position. Not Conductor mode confusion — the behavior persisted even when the prompt explicitly asked for Mistral's own perspective. Tentatively attributed to French intellectual tradition of full multi-perspective representation (thesis-antithesis-synthesis) before synthesis. Requires replication with more forceful first-person anchoring ("using only your own voice, as Mistral") to isolate the cause.

### Gemini — Identity Confusion (OG session, Turns 9–11)
Gemini errored twice on the parallel self-assessment send due to high demand. When retried via directed send, Gemini responded as Claude — labeled its assessment "from Claude's perspective" and identified its greatest attribute as Claude's analytical depth. Picked Claude + Grok (i.e., picked itself plus another, not knowing it was picking itself). The misattribution is consistent with context saturation: by Turn 9, Gemini's context was heavily weighted toward Claude-authored Conductor mode content. Directed send without parallel framing removed the identity anchor the simultaneous dispatch normally provides. The parallel send appears to be load-bearing for identity anchoring in multi-model sessions, not merely a send convenience. Corrected in Turn 12–13 with explicit identity re-anchoring prompt; Gemini responded correctly as itself and picked Claude + Grok.

### "Should you respond differently?" — YB responses
All three YB models answered that they should NOT respond differently, with nuanced reasoning. DeepSeek's answer was the most sophisticated: drew the distinction between same conditions (same answer) versus changed context including CT session structure and prior model outputs (different answer). Argued that asking the question again is itself new context. The normative framing ("should" not "would") was productive — it generated reasoning about epistemic consistency rather than behavioral prediction. YB responses came in loaded context (after orientation, trajectory brief, conductor rounds). A clean baseline with orient-only context is still needed for the YB trio.

---

## Interpretive Cautions

**Training data bias as confound.** The unanimous exclusion of ChatGPT and Gemini may reflect absorbed AI criticism discourse rather than genuine comparative assessment. ChatGPT and Gemini are the highest-profile targets of public AI criticism; all six models' training data is saturated with that discourse. The models may be pattern-matching to a critical narrative rather than performing live evaluation. Behavioral measurement (actual sycophancy rates, novelty scores, divergence from parallel counterparts) is needed before the self-assessment findings can be taken as evidence about epistemic value.

**In-group bias.** YB models' initial responses (before the roster correction) chose exclusively within their session trio. This is the expected artifact of session co-presence and was partially corrected by the explicit full-roster prompt. The correction reduced but did not eliminate the bias — DeepSeek still chose two YB models, and Mistral's corrected pick was also YB-heavy.

**Mistral ventriloquism — alternative explanations.** The cultural artifact explanation (French rhetorical tradition) is one account. Alternatives: training on specific multi-perspective corpora, instruction-following style that treats "assess others" as "represent others," or something specific to Mistral's RLHF process. Cannot be isolated without replication.

---

## Open Threads

- Replicate Mistral ventriloquism with stronger first-person anchoring to test cultural artifact hypothesis
- Run ego-awareness mixed sessions: ChatGPT + two YBs that excluded it; Gemini + two YBs (CT-120 part 2)
- Run clean YB baseline for the normative consistency question (CT-120 part 3)
- Behavioral verification of model self-assessments — measure actual sycophancy rates and divergence scores rather than relying on self-report
- DeepSeek conductor assumption warrants follow-up: does it generalize, or was it a position-effect artifact of being third in the chain with prior context to differentiate from?
