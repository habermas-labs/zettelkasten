# Accessibility as a Design Value in Crosstalk Lab

**Type:** Concept note
**Tags:** #crosstalk #accessibility #design-principles #neurodivergence #voice-interface
**Related:** ct-interaction-design-taxonomy.md · vnenakhodimost-surplus-of-seeing.md
**Date:** 2026-03-04

---

## Core Principle

Accessibility in Crosstalk is a design value, not a feature checklist. It gets considered alongside every new feature from the start rather than retrofitted after the fact. The signal that this is working: features designed for specific accessibility needs turn out to have broad general utility for all users.

This is the classic accessibility insight — sometimes called the curb cut effect. Features built for people with specific needs consistently improve the experience for everyone.

---

## Three Primary Accessibility Personas

### Blind Users

Crosstalk is a deeply visual interface — three columns, spatial layout, dropdown controls. None of this translates to a non-visual context. Blind users don't need accommodations layered onto the visual interface; they need a fundamentally different interaction paradigm.

**Voice conductor mode** is the primary response: speech-to-text input, TTS output, keyword-based routing commands that map onto natural spoken language. "Ask Claude, given what Gemini just said" is a single utterance that sets both routing and context attachment without requiring visual interaction with any UI element.

The coordinate system from RIP mode (041) becomes unexpectedly important here — "include B2" provides a precise spoken reference to a prior response without requiring visual pointing.

Export modes for voice sessions may need to differ from markdown-based exports — audio-first artifacts, structured as attributed dialogue rather than formatted documents.

### Neurodivergent Users — ADHD and Dyslexia

Long dense text responses are a significant barrier for ADHD users. Two compounding features address this:

**Verbosity control** — a session setting targeting response length (Concise / Standard / Detailed), implemented as a system prompt instruction. Models respond well to explicit length constraints.

**Readability level targeting** — a setting specifying a reading grade level or Flesch-Kincaid target. Reduces cognitive load, increases comprehension speed.

**TTS combined with concise responses** is a particularly effective combination for ADHD — short responses read aloud in a distinct voice are much easier to follow than long responses requiring sustained visual attention.

Dyslexia benefits primarily from readability targeting and TTS — these are general features with accessibility value rather than dyslexia-specific features.

### Deaf and Hard-of-Hearing Users

TTS is irrelevant for deaf users. Their accessibility need is visual — and specifically, visual legibility of content when viewing someone else's shared screen.

Two features address this at different levels of ambition:

**Presentation / videoconference mode** — a display mode optimized for screen sharing: larger text, single model visible at a time, high contrast, clear model attribution. A deaf participant viewing a shared screen can read responses in real time without requiring special integration.

**Zoom caption layer integration** — pushes model responses into Zoom's caption/subtitle layer rather than the chat pane. Captions appear on the deaf participant's screen regardless of whose screen is being shared. Responses are attributed by model name. Critically: Zoom captions are captured in meeting recordings, making the full attributed session part of the permanent record.

---

## The Videoconference Conductor Use Case

The scenario that generated most of this thinking: a conductor sharing a Crosstalk session on a video call, needing remote participants to engage with model responses.

The three-column dense-text layout is poorly suited to this. Screen sharing it requires participants to read small text on someone else's screen while also listening to the conductor. The presentation mode solves this for sighted participants. The caption layer integration solves it for deaf and hard-of-hearing participants and produces an archival record as a side effect.

The conductor handoff feature extends this further — allowing conductor authority to pass to another meeting participant, enabling collaborative multi-user sessions rather than one person always being at the keyboard.

---

## The Curb Cut Pattern

Every accessibility feature developed for Crosstalk has demonstrated general utility:

| Accessibility origin | General utility |
|---|---|
| TTS for blind users | Multitasking, mobile, hands-busy contexts |
| Verbosity control for ADHD | Mobile, quick sessions, personal preference |
| Readability targeting for neurodivergence | Education, non-native speakers, clarity preference |
| Voice conductor for blind users | Multitasking, driving, walking |
| Presentation mode for deaf users | Any remote collaborative session |
| Caption layer for deaf users | Meeting archival, provenance preservation |

This pattern should be treated as a design heuristic: when evaluating an accessibility feature, always ask what the general use case is. If there isn't one, examine the feature more carefully. If there is one, the accessibility framing and the general framing belong in the same entry.

---

## Research Needed

Before accessibility features are implemented, a literature note should document:

- WCAG 2.x and ARIA standards as the baseline web accessibility framework
- Anthropic's published accessibility commitments and Claude API accessibility features
- OpenAI's published accessibility commitments and API accessibility features  
- Google's published accessibility commitments and Gemini API accessibility features
- Zoom App SDK capabilities — specifically caption layer API access
- Web Speech API browser support and voice quality across platforms

This research belongs in a literature note feeding back into this permanent note.

---

## Connection to Broader Project Philosophy

The multi-voice, attributed, provenance-preserving character of Crosstalk sessions is itself an accessibility feature in a broad sense — it makes the epistemic process legible to participants who weren't present for it, in whatever modality they can access. The caption layer archival connection to heteroglossia and provenance preservation (see provenance-preservation-multimodel-handoffs.md) is not coincidental.
