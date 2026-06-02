# CT Multi-User Co-Conduct — Design Document

**Type:** Design document
**Tags:** #crosstalk #multi-user #co-conduct #webrtc #cloudflare #durable-objects #education
**Related:** CT-123, CT-124, CT-032
**Date:** 2026-05-31
**Status:** Draft — pre-implementation

---

## Concept

Multi-user co-conduct is a mode in which two human participants share a single live CT session. Both participants can see the same model responses in real time. Both can send prompts. A private backchannel — invisible to the models — allows the two humans to coordinate, deliberate, and communicate without contaminating the model context.

This is not screensharing. Both participants have genuine send authority. It is not a traditional two-person chat. The AI models are a shared object of inquiry, not participants in the human communication layer.

The primary motivation is educational: a teacher and student can conduct a joint AI session, with the teacher using the backchannel to coach the student's prompting decisions without those coaching moves entering the model context. The pedagogical structure becomes visible in the interface rather than happening off to the side.

The secondary motivation is research: two-conductor sessions create a structurally distinct form of human-human-AI dialogue that CT is uniquely positioned to support and study.

---

## Architectural Overview

The architecture has three layers:

**Shared session layer** — synchronized state visible to both participants and sent to the AI models. This is the existing CT session, extended to support two simultaneous clients.

**Human backchannel layer** — private communication between the two humans. Text and voice. Invisible to models. Operates in parallel with the shared session.

**Session initiation layer** — invite/token model controlling who can join. One human initiates, one joins. No public access during proof-of-concept phase.

---

## Infrastructure Requirements

### Current stack

CT is deployed on Cloudflare Pages (static HTML). A Cloudflare Worker serves encrypted `.ctk` key files from an R2 bucket. Authentication is via Cloudflare Access (email OTP). There is no persistent server-side state.

### What multi-user requires

**Cloudflare Durable Objects** — the minimum addition. A Durable Object is a single-instance stateful entity that multiple WebSocket clients can connect to simultaneously. It handles: session state synchronization (prompts and responses visible to both participants), text backchannel relay, and WebRTC signaling for voice. A single Durable Object class handles all three jobs.

Durable Objects require the **Workers Paid plan** (~$5/month). This is the only billing change required.

**WebRTC peer-to-peer** — browser-native audio between the two participants. The Durable Object acts as the signaling channel (exchanging SDP offers/answers and ICE candidates). Once the peer connection is established, audio travels directly between browsers and the Worker is out of the picture. No audio passes through Cloudflare infrastructure.

No additional services, no third-party dependencies.

---

## Session Initiation Model

The initiating participant creates a session. The Durable Object is instantiated with a unique room ID. The initiator receives an invite link containing the room ID. This link is shared out-of-band — by text, email, or any other channel the two humans already have.

The joining participant opens the invite link, which presents a join screen. CT validates the room ID against the Durable Object. If the room exists and has fewer than two participants, the join is permitted.

Two-participant maximum is a hard constraint enforced at the Durable Object level.

During the PoC phase, session creation itself is gated behind the existing Cloudflare Access authentication. Only users with approved email addresses can initiate sessions. This is the existing access control mechanism repurposed.

---

## Shared Session Layer

Both participants see the same model responses rendered in their respective CT interfaces. When either participant sends a prompt, the Durable Object broadcasts the prompt and the model responses to both clients.

The conversation history panel reflects the shared session state. Turn attribution shows which human sent each prompt — a small label or color distinction in the history chips (e.g. H1 / H2, or configurable display names).

Model context sees both participants' prompts in sequence. The models are not aware of the human backchannel. From the model perspective, the session appears to be a single conductor with occasionally varying prompt style.

Open question: should participants be able to optionally surface a backchannel exchange into the model context — a deliberate "bring this into the session" action? This has research value but adds complexity. Deferred to post-PoC evaluation.

---

## Human Backchannel Layer

### Text

A sidebar panel, clearly visually separated from the main CT interface. Messages appear in a simple chronological thread. Neither participant's messages are logged to the session transcript or sent to any model.

The Durable Object relays text backchannel messages between the two clients. Messages are not persisted — they exist only in the live session and in each client's rendered UI.

### Voice

Browser-native WebRTC peer-to-peer audio. The Durable Object handles signaling only (SDP and ICE exchange). After connection establishment, audio is peer-to-peer.

UI controls: a mic button in the backchannel panel. Push-to-talk for PoC (simpler, avoids echo and feedback issues). Open mic as a later option.

Voice and text backchannel coexist. A participant can type while the other speaks.

---

## UI Surface

The backchannel panel should feel deliberately distinct from the main CT interface — it is a different epistemic layer. Suggested treatment: a collapsible panel on the right side (adjacent to or replacing the existing right sidebar in co-conduct mode), with a visual language that reads as "between us, not in the session."

Session initiation UI: a new entry point in the CT interface — "Start shared session" — which generates the invite link. A corresponding join screen for the invited participant.

Participant indicators: both participants see each other's presence — a small status indicator showing that the second human is connected. If a participant disconnects, the remaining participant sees this clearly.

---

## Implementation Roadmap

### Phase 1 — Infrastructure (Cloudflare)

1. Upgrade to Workers Paid plan
2. Write a minimal Durable Object class: accepts WebSocket connections, relays messages between connected clients, enforces two-client maximum
3. Deploy the Durable Object alongside the existing Worker
4. Smoke test: two browser tabs connect to the same DO instance, exchange a message

No CT UI changes in this phase. Goal is to confirm the plumbing works.

### Phase 2 — Shared Session

1. Modify CT to optionally connect to a Durable Object WebSocket on session start
2. Session creation: generate room ID, instantiate DO, produce invite link
3. Session join: validate room ID, connect second client to existing DO
4. Sync: prompts sent by either participant broadcast to both; model responses broadcast to both
5. Turn attribution in history chips (H1 / H2 label)
6. Test: two browser windows, one initiator, one joiner, shared prompt/response cycle confirmed

### Phase 3 — Backchannel Text

1. Add backchannel message type to the DO relay protocol (distinct from session sync messages)
2. Backchannel panel UI in CT — collapsible, visually distinct
3. Text input in backchannel panel sends to DO, DO relays to the other client only
4. Confirm backchannel messages do not appear in session transcript or model context
5. Test: backchannel exchange while shared session is active

### Phase 4 — Backchannel Voice

1. Implement WebRTC signaling through the DO (SDP offer/answer, ICE candidates as relay messages)
2. Browser-side WebRTC connection setup on both clients
3. Mic button UI in backchannel panel — push-to-talk
4. Test: voice between two participants while shared session and text backchannel are both active

### Phase 5 — Polish and PoC Evaluation

1. Participant presence indicators
2. Disconnect handling (graceful degradation if one participant drops)
3. Session close behavior (initiator can end the session, notifying the joiner)
4. Structured PoC test with actual teacher/student or two-conductor use case
5. Evaluate open questions: optional backchannel-to-session surfacing, display name configuration, session export attribution

---

## Open Questions

**Backchannel-to-session surfacing** — can a human deliberately move a backchannel exchange into the model context? Deferred.

**Display names** — should participants set names (Teacher / Student, H1 / H2, custom)? Relevant for history chip attribution and backchannel thread readability. Probably yes, but kept simple for PoC.

**Session export** — how does the transcript export handle two-conductor attribution? Does the backchannel export at all (probably not by default — it's private by design)?

**Model context framing** — should the system prompt be modified in co-conduct mode to inform the models that two conductors are present? This is an interesting epistemic question. The models' behavior may shift if they know. Deferred to post-PoC experiment.

**Access control longevity** — Cloudflare Access email OTP gating works for PoC. Any future expansion needs a more formal access model.

---

## Relationship to Existing CT Architecture

The single HTML file architecture is preserved. Co-conduct mode is additive — a new optional connection layer that activates when a session is initiated or joined. Single-user CT sessions remain unchanged.

The existing Cloudflare Worker for R2 key distribution is unaffected. The Durable Object is a new Worker class deployed alongside it.

Browser-only architecture is maintained for the client. The Durable Object introduces server-side state, but this is session-scoped and ephemeral — it exists only while the session is live. No persistent user data is stored server-side.

---

*Forward: ZK note on human-human-AI dialogue as a structurally distinct mode · CT-114 (Committee mode) adjacency · reciprocal-teaching-ct-preset.md connection (teacher/student co-conduct maps directly onto the reciprocal teaching framework)*
