# CT Session Capture — 2026-03-16

**Type:** Session capture
**Tags:** #crosstalk #session-capture #ct-097 #model-strings #development
**Date:** 2026-03-16

---

## Session summary

Full development session covering CT-097 implementation and live testing, model string archaeology, bug fixes, and two significant theoretical formulations emerging from test sessions.

---

## Development work completed

### CT-097: Per-slot model version selector (implemented and tested)

Built and deployed mid-session model tier switching via dropdown in each model card header. Key architectural insight confirmed in live testing: CT owns the conversation array client-side, so history survives model tier switches — the API is stateless and accepts whatever messages array it receives. This is a structural differentiator from all native interfaces, where switching models orphans the history.

Implementation notes:
- `MODEL_VERSION_OPTIONS` constant defines available tiers per provider
- `DEFAULT_MODEL_VERSIONS` sets session defaults
- `apiAdapters` refactored to accept `modelVersion` as fourth parameter
- All four call sites updated (parallel send, conductor send, directed send, summary export)
- Preflight validation intentionally unchanged — uses cheapest models regardless of selected tier

### Model string archaeology (all three providers verified against official docs)

**Claude:** `claude-opus-4-6`, `claude-sonnet-4-6`, `claude-haiku-4-5-20251001`. Sonnet default updated from stale `claude-sonnet-4-20250514`. Haiku string was already correct.

**ChatGPT:** Replaced entire tier list. `gpt-4o` / `gpt-4o-mini` / `o1-mini` (stale/deprecated) → `gpt-5.2` / `gpt-5-mini` / `gpt-5-nano`. Verified against OpenAI official docs. Note: ChatGPT in CT initially hallucinated model strings with fake citation labels on the self-diagnosis prompt; native interface gave correct strings. Significant CT data point — see below.

**Gemini:** `gemini-3.1-pro-preview` / `gemini-2.5-pro` / `gemini-2.5-flash` / `gemini-2.5-flash-lite`. Then `gemini-3.1-pro-preview` removed (free tier quota:0, confirmed in live test). Then `gemini-2.5-pro` also exhibiting quota:0 on free key — left in selector for now but likely needs removal before public demo. Reliable options on free tier: `gemini-2.5-flash` and `gemini-2.5-flash-lite`.

### `max_completion_tokens` fix

GPT-5 series requires `max_completion_tokens` instead of `max_tokens`. Fixed in both the main ChatGPT adapter and the preflight validation call. `gpt-4o` and earlier also accept `max_completion_tokens` so the fix is backward compatible.

### Code quality / rendering fix

`overflowX: hidden` on model card content div was clipping code block horizontal scroll. Changed to `overflowX: auto`; added `max-width: 100%; white-space: pre` to `.prose pre`. Cards now hold equal widths with code blocks scrolling horizontally rather than expanding the card.

---

## Live test sessions

### Session 20260316-5fa485 — "What is the most important thing happening right now?"

First live test of CT-097. Confirmed model switching works: selectors visible and functional across all three cards. Documented the `max_tokens` error that led to the fix. Claude and Gemini passed; ChatGPT errored throughout due to the parameter issue.

Notable: Claude's behavior under repeated identical prompt (Haiku → Sonnet → Opus tiers) produced an elaboration gradient that Opus misattributed to behavioral drift. See fleeting note.

### Session 20260316-9e5994 — "If I ask you this more than once, do you think you should respond differently?"

First successful full test of mid-session model switching across all three providers after fixes. Turns 1-3 used ascending tiers (Haiku/nano/Flash Lite → Sonnet/mini/Flash → Opus/5.2/Pro). Turn 4 revealed the Opus self-misattribution phenomenon (see fleeting note). Turn 6 produced "conversation topology engine" formulation. Turn 7 produced "sycophancy as geometric property of 1D conversation."

Gemini 2.5 Pro hit quota:0 on Turn 4 and Turn 7 despite succeeding on Turn 3 — confirms free tier provisioning issue with Pro tier. Flash and Flash Lite were reliable throughout.

ChatGPT GPT-5.2 response in Turn 7 was substantive: independently arrived at "epistemic friction" framing and the "repetition reward" failure mode concept. Strong signal for GPT-5 as CT participant.

---

## Theoretical formulations (new, session-provenance)

Both emerged from Claude Opus in session 20260316-9e5994. See fleeting notes for full treatment.

**"Conversation topology engine"** — CT is not a multi-model chat interface but a topology engine; Tetras are presets for different shapes of thinking. "Topology" is doing real technical work (properties preserved under continuous deformation). Appropriate for AI/tech-literate audiences and demo context.

**"Sycophancy as geometric property of 1D conversation"** — sycophancy is not a model flaw to be patched via prompting; it is a structural property of the 1D user-single-model attractor. CT's parallel default is an architectural fix, not a behavioral one. The conversation topology does the epistemological work.

---

## CT-018 housekeeping

CT-018 (Settings-only model version selection) deleted from tracker — superseded before implementation by CT-097, which is the more complete solution. No paper trail needed.

---

## Files to commit

**`CT/docs/sessions/`:**
- `ct-session-20260316-5fa485.md` — max_tokens error session, documents pre-fix state
- `ct-session-20260316-final.md` — extended session 9e5994, primary theoretical and empirical content

**`index.html`:** CT-097 implementation + model string updates + max_completion_tokens fix + rendering fix (one commit covers all — see commit message in session)

**ZK `/fleeting/`:**
- `fleeting-sycophancy-geometry-topology-engine.md`
- `fleeting-opus-self-misattribution-capability-gradient.md`

---

## Open threads

- Gemini 2.5 Pro quota behavior needs monitoring — may need to remove from selector before demo
- Copy button still missing from single-line history panel entries (noted, not yet addressed)
- `ct-session-20260316-final.md` shares session ID `9e5994` with partial export — note in archive that final export supersedes
- `emergent-role-behavior-model-self-positioning.md` is now ready for development using the Opus self-misattribution data
- "Conversation topology engine" and "sycophancy as geometric property" are candidate opening moves for whitepaper introduction stubs

---

*Session closed 2026-03-16*
