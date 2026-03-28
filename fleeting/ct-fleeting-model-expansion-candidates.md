# CT Fleeting — Model Expansion Candidates

**Type:** Fleeting note
**Tags:** #crosstalk #model-expansion #byok #provenance #color-system
**Related:** CT-099 · heteroglossia-compression-ai-provenance.md
**Date:** 2026-03-17

---

Current CT implementation uses Claude (Anthropic), ChatGPT (OpenAI), and Gemini (Google) as the three founding vertices. As BYOK architecture matures and model chip selection becomes user-configurable, expansion to additional providers warrants consideration. This note captures the reasoning from the first structured survey (2026-03-17).

**Priority candidates — distinct epistemic provenance:**

*Grok (xAI)* — highest priority. Live web access is architecturally distinct from the other three, not just stylistically different. Brings a recency dimension none of the founding models have natively. A genuinely different kind of compression, not just a fourth voice.

*Mistral (Mistral AI)* — European provenance, genuinely open-weights, no commercial guardrails of the same kind as the founding three. Cultural and regulatory context is distinct in ways that may surface on contested or policy-adjacent topics. The heteroglossia argument applies: this is a different compression of the corpus, not just a different style.

*DeepSeek* — Chinese institutional provenance. Competitive with closed Western models on benchmarks. Whether provenance produces substantively different epistemic posture on non-politically-loaded topics is an open empirical question — CT is well positioned to test it. Open weights are also architecturally interesting for the same reasons as Mistral.

**Considered, lower priority for now:**

*Perplexity* — live search like Grok, but redundant if Grok is already in play. No distinct provenance advantage over Grok.

*Cohere* — developer-friendly, strong enterprise positioning, but no clear epistemic differentiation from the founding three. More of a deployment alternative than a genuine new vertex.

*Llama (Meta, via third-party hosting)* — open weights are interesting but requires routing through an intermediary (Together AI, Fireworks, Groq, etc.) rather than a first-party API. Adds integration complexity without a clear provenance argument beyond open-weights, which Mistral already covers with a cleaner first-party API story.

**On model branding and color system:**

CT's color system for the founding three derives from each model's established brand palette — Claude's amber, ChatGPT's green, Gemini's blue. This is not arbitrary: the colors carry provenance signal. When a user sees a response tinted amber, they know it came from Anthropic's model with Anthropic's training decisions behind it. The color is part of the attribution system, not decoration.

Any expansion to additional models should follow the same principle: research the model's established brand color before assigning one. Grok/xAI uses a stark white-on-black identity; Mistral uses a deep orange; DeepSeek uses a blue-teal. These should inform chip and card colors when those models are added, maintaining the system's internal logic. Arbitrary color assignment breaks the provenance argument the color system is implicitly making.

This also has a practical implication: the light mode palette adjustments made for the founding three (darkening accents to read against light backgrounds) will need to be applied consistently to any new model colors.

**Tracker:** CT-099 — model expansion candidates.
