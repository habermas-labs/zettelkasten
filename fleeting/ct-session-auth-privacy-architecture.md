---
title: Session Authentication, Cross-Session Identity, and Privacy by Architecture
type: fleeting
tags: #crosstalk-app #privacy #security #architecture #local-coherence #memory-asymmetry
related: ct-interaction-design-taxonomy.md · temporal-asymmetry-human-ai.md · local-coherence-ai-instantiation.md
date: 2026-03-13
status: capture
---

Core question: Should CT models be aware of the user's identity across sessions? And is there any current mechanism by which they could be?

Current architecture: CT makes direct API calls to Claude, ChatGPT, and Gemini using API keys. The API authentication layer knows only the key, not the account holder. Browser session cookies for claude.ai, chat.openai.com, and gemini.google.com are entirely separate from API call authentication. No pathway exists for browser account sessions to bleed into CT API calls for Claude or ChatGPT.

Gemini/Google note: Google's ecosystem is more deeply integrated than the others (Chrome, Google accounts, Google services share signals). However CT calls the Generative Language API directly with an API key — the endpoint does not read browser cookies or cross-reference Google account sessions. The authentication is the key string in the request header, full stop. No shenanigans in the CT context.

Privacy by architecture: CT's session-blind, stateless design means it never accumulates a profile of the user across sessions. Each session starts clean not because of an explicit delete operation but because there was never anything to persist. The data never existed at the infrastructure level. This is a stronger privacy guarantee than "we delete your data" — it is "we never had it." Architecturally enforced rather than policy-enforced, which means it cannot be quietly changed by a terms-of-service update.

Should CT models be aware of user identity? Open design question requiring careful thought before any implementation. Arguments on both sides:

For: personalization improves conductor experience; models that "know" the conductor could adapt more efficiently; continuity of local coherence across sessions without manual mediation.

Against: personalization introduces sycophancy risk — a model that has learned the conductor's preferences may calibrate toward those preferences rather than maintaining role integrity; CT's epistemic value may partly depend on models not knowing the conductor; the cold start preserves epistemic distance that makes divergence more genuine. A model that has learned your preferences may converge toward them rather than toward its own compression of the heteroglossia.

Connection to memory asymmetry: the human conductor currently mediates the offload/onboard cycle manually — saving files, uploading transcripts, carrying context across the session boundary. This is the existential continuity function. If CT were to implement cross-session identity for models, that mediation would become partially automated. Whether that is desirable or whether it undermines something important about the human role in the collaboration is an open question.

Implication for CT privacy posture: "privacy by architecture" should be explicit in public-facing design rationale (D-15 stub) and devstack security documentation (D-07). It is a meaningful differentiator from cloud-based AI services and the CT design earns it honestly.

Forward: devstack-security.md · ct-wp-design-rationale.md · local-coherence-ai-instantiation.md
