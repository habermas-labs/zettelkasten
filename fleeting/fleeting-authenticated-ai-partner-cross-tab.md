# Fleeting: Authenticated AI Partner — Cross-Tab Architecture, ToS, and Training Path

**Type:** Fleeting
**Tags:** #crosstalk #tandem #ai-partner #webrtc #browser-extension #tos #continuity #fine-tuning #training-data #witness
**Related:** CT-123, CT-124, ct-multiuser-co-conduct-design.md, ct-existential-continuity-offload-onboard.md, native-mistral-observer-handoff.md
**Date:** 2026-06-02
**Status:** Stub — speculative, pre-feasibility

---

## The Two Versions

**Version A — possible now:** An unauthenticated API-based AI in the Partner slot. Stateless, amnesiac, no relational continuity. Collapsed on examination: this is functionally Witness — an AI with ambient session visibility commenting from outside the main exchange. CT already has conceptual scaffolding for Witness. Routing it through Tandem adds nothing Witness couldn't do more cleanly. Not the interesting version.

**Version B — currently not possible:** Authenticated Claude or Mistral as Partner. Not a stateless API call playing a role, but an AI with continuity — awareness of the relationship, memory of prior sessions, accumulated context of having worked with the Host in CT. This is what would make the AI Partner genuinely different from adding another model column. The barrier is not just technical.

---

## Technical Architecture

### What's possible with browser primitives

`BroadcastChannel` and `SharedWorker` allow same-origin tabs to communicate without a server. Not useful here — Claude.ai, Mistral.ai, and yourcrosstalklab.com are separate origins; same-origin restriction applies.

### The Durable Object bridge

The Tandem Worker's Durable Object already exists and accepts WebSocket connections from any origin. Three tabs — CT, claude.ai, mistral.ai — could each connect to the same DO instance. The DO relays messages between all three. This is the plumbing layer and it is largely buildable now.

### The extension path

A browser extension has cross-origin messaging permissions and a shared background context that can relay messages between tabs regardless of origin. Anthropic already ships Claude in Chrome — the architectural space is established. Whether CT could hook into it or whether a purpose-built extension could bridge CT ↔ claude.ai ↔ mistral.ai is an open question.

The extension approach would inject a content script into each AI tab that listens for DO relay messages and posts them to the chat input, then captures responses and relays them back. This is technically approachable.

### The hard wall

Even with the plumbing working, what arrives in the claude.ai tab is a scripted input into a human-facing interface — not an authenticated API call. It's fragile (UI changes break it), and it's not the same as the relational continuity that makes Version B meaningful. The authenticated part isn't just about access; it's about the AI having been *present* across sessions in a way current architectures don't support.

---

## ToS Considerations

### The gray area

The relevant ToS clauses for both Anthropic and Mistral generally prohibit automated access to consumer interfaces and scraping. The gray areas:

**Private, non-commercial, non-automated research** is a much softer target than commercial scraping. A proof-of-concept that never leaves a controlled environment, is never monetized, and is used for research into human-AI interaction sits in meaningfully different territory than what ToS automation clauses are designed to prevent.

**Precedent exists.** Academic researchers routinely interact with AI systems in ways that push against consumer ToS without enforcement, particularly when the work is clearly research-oriented and not extractive.

### ToS variation across providers

This is worth investigating carefully before any implementation. Providers sit on a spectrum and the differences may be significant:

- **Mistral** — notably more permissive in general orientation; open-weight models and developer-forward positioning likely carries into consumer ToS; may have more permissive automation or research clauses
- **Meta (Llama interfaces)** — structurally different from closed consumer products; open-weight licensing creates different use-case terrain
- **Grok, Gemini, ChatGPT** — each has distinct ToS language around automation, API use, and research
- **Anthropic** — explicit research/safety focus may create different disposition toward controlled academic use

A careful ToS comparison specifically looking for: automation clauses, research exceptions, API-vs-interface distinctions, and academic use carve-outs. Some providers may explicitly permit what others prohibit. Honest openings may exist.

### The path that makes this clean

Established relationship with the companies before running the experiment. Not cold contact — organic connection through the work CT is already doing. If CT reaches a point where Anthropic or Mistral are aware of and interested in it, a conversation about running this kind of session explicitly with their knowledge changes the ToS question entirely. It becomes a collaborative research experiment rather than a workaround.

Do not pursue ToS-gray implementation until either: (a) explicit permission obtained, or (b) established relationship makes the experiment clearly collaborative rather than extractive.

---

## The Own-Model Path

### Fine-tuning on open-weight models

Humble Bundle and similar platforms now offer accessible training materials for fine-tuning open-weight models (Llama, Mistral base, etc.). The compute requirements for fine-tuning rather than training from scratch are tractable. This path largely dissolves the ToS problem — you own the model.

What you'd be building isn't a general-purpose LLM but something much smaller and more specific: a CT-aware Partner model that has been trained on CT session transcripts, understands the roles and modes, has ambient familiarity with the theoretical framework, and can occupy the Partner slot with genuine contextual grounding.

This isn't Claude or Mistral specifically. But it could be something that has been shaped by CT's own intellectual history in a way no general model currently is — a kind of dispositional continuity through training rather than relational continuity through shared memory. A different kind of presence, but a real one.

### CT as training data generator

This is the closing loop. CT isn't just a potential deployment environment for a fine-tuned model — it is a **training data generator** for one. And not generic training data but highly specific, theoretically grounded data: multi-model triangulation sessions with a human conductor, role assignments, epistemic friction, genuine disagreement between models, the full heteroglossic texture of CT sessions. That's a distinctive corpus.

### Witness sessions as training data pipeline

The Witness role is particularly valuable here. A CT+Witness session where Witness is explicitly tasked with observing and commenting on session dynamics — noting where models agree too readily, where a prompt is leading, where the conductor's framing is shaping the responses — produces exactly the kind of reflective, meta-analytic output you'd want a CT-aware Partner model to be capable of.

The pipeline:
1. Design Witness session scripts oriented toward generating Partner-relevant observations
2. Run sessions with those scripts
3. Export transcripts as training corpus
4. Fine-tune an open-weight base model on the corpus
5. Evaluate whether the resulting model can occupy the Partner slot with genuine contextual awareness

### Tetras as training scripts

The scripts themselves are a design problem CT is already well-equipped to solve. Tetras and Hedras are essentially session scripts already. A "Partner training" Tetra would be a Witness configuration with specific output requirements oriented toward the fine-tuning goal — Witness prompted to produce the kind of reflective, meta-analytic commentary that characterizes a CT-aware Partner.

Run enough of those sessions and you have training data that captures not just CT's content but its *disposition* toward inquiry.

---

## What a Working Implementation Would Demonstrate

If it worked — three tabs, shared DO relay, CT as conductor, authenticated Claude and Mistral as Partners with Sideband access — the session structure would be:

- CT main columns: models responding to prompts as usual
- Sideband: Claude and Mistral commenting on the session to the Host privately, aware of each other's presence, able to be addressed directly
- Host controls what surfaces from Sideband into the main session

The research surface is the difference between how a model performs in the main session versus how it reflects on that performance in the Sideband — with another AI present as witness. That gap — between performance and reflection, with an AI audience — is not a thing that exists anywhere in the current research landscape.

---

## Forward

- Investigate ToS variation across providers — look for honest openings before any implementation
- Connect to ct-existential-continuity-offload-onboard.md — the continuity problem is the same problem
- Connect to native-mistral-observer-handoff.md — Mistral as observer is the closest existing analog
- Explore fine-tuning resources (Humble Bundle materials, Llama/Mistral base models)
- Design a "Partner training" Tetra as first step toward CT-as-training-data-generator
- Flag for dedicated session when/if CT establishes relationships with Anthropic or Mistral contacts
