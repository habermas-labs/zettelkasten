# Provenance Preservation in Multi-Model Handoffs

**Core observation:** Standard single-model AI interactions systematically flatten provenance — content carried into a new thread via handoff gets attributed to the user regardless of its actual origin. The user becomes the apparent author of ideas the model itself generated in a prior session. This is not a bug; it is a reasonable inference given that the model reads the handoff as a document authored by whoever is sending it.

---

## Contrasting Cases

**Case A — Standard single-model handoff:** User carries content from a previous thread into a new conversation. The receiving model attributes all of it to the user. Ideas the model generated in the prior session are now "the user's ideas." Provenance flattened onto the human.

**Case B — CT Include mechanic:** Content is explicitly attributed to a named model source in the handoff framing. The receiving model correctly identifies that source as the author and responds accordingly. Empirically demonstrated in CT test session 2026-03-04: Claude-authored questions routed to ChatGPT via Include; ChatGPT correctly attributed all content to Claude with no reference to the user, accurately reflecting the actual authorship of that material.

---

## Significance

CT's multi-model architecture may constitute a partial structural solution to a problem that is invisible in single-model interfaces — precisely because single-model interfaces have no mechanism for naming a non-human, non-user source. The Include mechanic makes source attribution explicit in a way that standard handoffs cannot.

---

## Open Questions

- Does provenance preservation hold under mixed authorship (Move 3, where user and model contributions are combined)?
- Does it degrade over longer sessions as attribution scaffolding fades from the model's working context?
- Can an explicit provenance mechanism be designed that handles edge cases — particularly Move 3 — robustly?

---

## Significance for Model Builders

CT makes the contrast between provenance flattening and provenance preservation visible and reproducible. The Include mechanic is a candidate design pattern worth evaluating for broader application.

---

## Connected Entries

- CT-TRACKER 015 — Handoff summaries
- CT-TRACKER 048 — Directed engagement controls
- CT-TRACKER 056 — Move 2 explicit indicator
