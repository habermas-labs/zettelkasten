# ct-fleeting-the-threshold-tetra

**Type:** Fleeting note
**Tags:** #crosstalk #tetras #threshold #accessibility #ada #interaction-design
**Date:** 2026-03-19
**Status:** Generative capture — not refined
**Origin:** CT development session; emerged from parallel ADA accommodation project in a separate Claude project

---

## The Idea

New Tetra concept: **The Threshold**. Named for the epistemic act of *preparing to cross* — the moment of translation between private lived experience and institutional language, before a practitioner encounter (medical, HR, ADA, legal, or other systems encounter).

The name follows the "place entered" convention (alongside the Agora and the In-Between). The patient is not in the institution yet. They are at the threshold. The session is the preparation for crossing, not the crossing itself.

---

## Origin Context

Emerged from work in a separate ADA accommodation project. In that project, Claude operating in an extended conversation produced a talking points document that the patient's practitioners found extremely valuable — legible, appropriately framed, clinically useful. The question became: how do you make that process available to other patients, including those who don't want to log in to an AI service, don't have extended chat history, or don't trust AI with their medical information?

CT's no-persistence, no-sign-in architecture is the answer. The session disappears on window close. That's not a limitation — it's the privacy contract that makes the conversation possible for users who would not have it elsewhere.

---

## The Four-Document System (from ADA project)

The ADA project is building four documents that frame the preparation workflow this Tetra supports:

1. **Quick start guide** — explains the process, instructions for preparation (gathering documents, what to expect), and a critical CT-specific note: in CT there are no saved sessions, so the work should ideally happen in one sitting; preparation is therefore load-bearing in a way it isn't in a standard logged-in AI session
2. **Prompt template** — AI-only document providing context and a scaffold of what to ask and what to produce; this is the initialization document the patient uploads to their AI of choice (CT being the privacy-preferred option)
3. **Standalone guidance document** — for patients who want the preparation process without AI involvement at all; same arc, no model required
4. **Provider's handbook** — explains what these documents can do, how to introduce the process to a patient, and how to work with the output once the session is complete

The prompt template (document 2) should include explicit instruction about the Scribe's dual output responsibility (see below).

---

## Role Structure (working)

**Witness** — receives the lived experience as the patient describes it; holds it without clinical reframing or institutional translation; reflects back to confirm fidelity. The role that keeps the document from becoming generic. Also holds the pacing function — does not rush to output; establishes what the person has, what they can describe, what documents they've gathered, before translation begins.

**Scribe** — the translation and output role; dual responsibility:
- *Forward output*: the practitioner-facing talking points document — legible to the system the patient is about to enter
- *Backward output*: a structured resumption artifact — enough session state captured that if the patient cannot complete in one sitting, they can export and upload for a second session without starting from scratch

The Scribe is doing deliberately what the CT architecture cannot do structurally (no persistence). The Scribe is the session's memory externalized. Two output directions: forward toward the practitioner, backward toward the self.

**Navigator** — maps the institutional terrain. Knows what frameworks apply (ADA, FMLA, 504, etc.), what documentation practitioners can and cannot provide, what language HR or institutional systems respond to, what the patient is entitled to ask for. Prevents undershooting. Prevents asking for the wrong thing. The knowledge-supply role.

**Conductor (human)** — fourth vertex; the authority on their own experience; confirms whether the Scribe's translation is true; directs pacing; the one whose situation it actually is.

---

## CT-Specific Design Notes

- **One-session default**: CT's no-persistence architecture means the quick start guide must prime thorough preparation — gathering documents, knowing what to describe, having time set aside. This is a meaningful difference from a logged-in session where the conversation can pause and resume.
- **Resumption artifact**: The Scribe's backward output is a structured session state export. Not a raw transcript — a formatted document that can be uploaded at the start of a second session to restore context. This maps onto CT's existing session vault upload infrastructure (CT-019/083/084).
- **Privacy as affordance**: CT's architecture (no sign-in, no data storage, no API logs visible to platform) makes it the preferred environment for sensitive medical/accommodation conversations. This should be explicit in the quick start guide's CT-specific section.
- **The Threshold as pre-clinical**: The session is not a clinical encounter. The output is preparation material, not a diagnosis or a plan. The Navigator provides information about systems and frameworks, not medical advice. This framing matters for how the provider's handbook describes the product to practitioners.

---

## Open Questions

- Does the Witness role need an explicit anti-medicalization instruction in the prompt template? (Don't translate yet — just receive and hold.)
- What is the right format for the resumption artifact? Structured markdown with section headers (what was described, what documents were referenced, what output was drafted, what remains)? Or something the Scribe generates as a natural artifact of the session?
- Does this Tetra have a Hedra? The obvious candidate is a temporal facing — Navigator oriented toward the upcoming encounter, Witness oriented toward the past experience, Scribe oriented toward the gap between them. Worth developing.
- The Calibration Tetra's universal design note is relevant here: features designed for specific accessibility needs consistently demonstrate broad utility. The Threshold may have non-medical applications wherever a person needs to translate private experience into institutional language (legal proceedings, educational IEP processes, workplace accommodation requests beyond ADA, immigration, insurance appeals).

---

## Connections

- CT-TRACKER 074 — The Threshold Tetra
- ZK permanent: ct-tetras.md
- ZK permanent: ct-accessibility-design-principles.md
- ZK permanent: the-in-between.md (holds-tension-before-crossing is adjacent)
- ADA accommodation project (separate Claude project — not cross-referenced by design; provenance noted here)
