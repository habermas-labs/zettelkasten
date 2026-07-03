# Kirsh & Maglio (1994) — Epistemic vs. Pragmatic Action

**Type:** Literature note
**Tags:** #epistemic-action #cognitive-offloading #cognitive-geography #finite-infinite-games #hac-design #literature
**Related:** distributed-metacognition.md · literature-cluster-ai-learning-metacognition.md · workload-outsourcing.md · fleeting-irony-of-agency.md · fleeting-arch-ttt-ai-tool-literacy.md
**Date:** 2026-07-03 (capture originated 2026-06-23)
**Origin:** Claude thread "Epistemic actions as cognitive offloading bridge" (2026-06-23). Reference surfaced by ChatGPT; verified and corrected by Claude.

---

## Citation

Kirsh, D., & Maglio, P. (1994). On distinguishing epistemic from pragmatic action. *Cognitive Science, 18*(4), 513–549.

Provenance note: ChatGPT surfaced the reference but misidentified the experimental domain as Scrabble; the study was **Tetris**. The correction matters substantively — Tetris's time pressure is part of the experimental logic. The game demands split-second decisions with a premium on minimizing moves, so if epistemic actions appear *there*, they are likely to appear almost everywhere. (Also a small live data point for the multi-model provenance theme: cross-model reference-passing with verification caught a factual drift that would otherwise have propagated.)

## Core distinction

- **Pragmatic actions:** performed to move closer to a goal state in the world.
- **Epistemic actions:** performed to uncover information that is hidden or hard to compute mentally — changing the world in order to simplify the problem-solving task.

Signature finding: expert Tetris players routinely rotate falling pieces more than placement requires. The extra rotations aren't positioning the piece; they're restructuring the perceptual problem so internal pattern recognition operates more efficiently.

Sharpening (from reading the 1995 abstract, 2026-07-03): the "simplification" in epistemic action is always simplification of *cognition*, and it is often purchased with *additional* physical action. The over-rotating player spends motoric effort to buy perceptual ease. Kirsh is therefore not a friction-minimizer in the workload-outsourcing sense — action is expended to serve internal computation, never to replace it. "Minimizing friction" underdescribes even the fluent expert's workspace; what is minimized is a specific kind of friction, and which frictions to preserve is a developmental variable (see pointer under Connections).

## Companion text — Kirsh (1995)

Kirsh, D. (1995). The intelligent use of space. *Artificial Intelligence, 73*(1–2), 31–68. (Kirsh solo; citation verified against abstract 2026-07-03.)

Extends the framework from game contexts to workplace management: how agents set up and continuously manage their workspace as an integral part of thinking, planning, and behaving — spatial arrangement as cognition, not afterthought. Proposes a three-category classification of intelligent spatial arrangement:

1. Arrangements that simplify **choice**
2. Arrangements that simplify **perception**
3. Spatial dynamics that simplify **internal computation**

Data drawn from cooking, assembly, packing, supermarkets, workshops, playrooms, and the Tetris studies. The workplace-management framing is what opens the developmental question (novice vs. master workspace organization) — developed separately, not here.

## Operationalizing the distinction for AI-assisted work — the subtraction test

Emerged 2026-07-03, in a session working the workspace-friction fleeting note. The question: why does "student asks AI to write the paper" fail to be Kirshian, when "student assesses which tool best serves quality while optimizing time-on-task" looks like it should count?

First pass (Skooter): the tool-selection move is a min-max — assess available tools, choose the one serving work quality while also optimizing other outcomes like time spent on task. That's real, but on inspection it sits one level up from what Kirsh's Tetris data documents. Tetris rotation is continuous, in-task, situated — restructuring the perceptual field moment to moment so the player's own fit-recognition stays easy. Tool selection is a meta-level decision made *about* the task before it starts; it maps to Kirsh's "arrangements that simplify choice" category, not to the in-task epistemic action itself. Necessary, but not yet the thing.

The sharper test, pushing "action expended to serve, not replace, internal work" one notch further: **does the AI's output leave something for the student's own cognition to still do — recognize, integrate, judge, transform — before it becomes the finished work? Or does it arrive as the finished cognitive product, such that the only work remaining is transcription or submission?**

Operationalized as a subtraction test: take the AI's output away and ask what the student would still have to do. "Recompute the whole thing from scratch" → pragmatic replacement dressed as help. "Lose a useful prompt but still have to do the actual work of integrating it" → epistemic scaffolding. Concretely: asking the AI for the strongest counterargument to a drafted paragraph, then deciding whether and how to fold it in, passes — something rotated into view that the student still has to *see* and use. Asking the AI to write the paragraph outright fails — nothing is left to fit.

Tool selection (the min-max move) is upstream of the test: it's how a Kirshian chooses well among available instruments. The subtraction test is what tells you whether a given use, once made, actually behaved like a rotation or like a finished piece dropped straight into place. Directly operationalizes the workload-outsourcing distinction and gives the Irony of Agency's "residue of learning" claim a checkable form.

## Not a bridge — an orthogonal axis

ChatGPT's original framing ("missing bridge between Clark/Chalmers and Risko/Gilbert") was refined in discussion to something stronger:

The Hutchins → Clark/Chalmers → Risko/Gilbert sequence is a true **nesting** organized by *scale of system*: sociotechnical ensemble → individual-plus-tool dyad → individual cognitive economy. Its organizing question is **cognitive geography** — *where does cognition live, and at what scale?*

Kirsh/Maglio ask a different question: *what is the agent doing to manage the relationship between world and mind in real time?* That is a question about **action type**, not system boundary. The Tetris player isn't extending mind into the piece (Clark/Chalmers) or offloading computation to it (Risko/Gilbert) — the locus of cognitive work stays internal, and the environment is manipulated to *serve* that internal work, not replace it. This is **cognitive strategy**, and it operates across all three levels of the geography nesting: a navigator repositioning a chart (Hutchins scale), a dyad, or a purely individual context.

Orthogonality also explains why Kirsh/Maglio doesn't slot into the temporal sequence as a bridge despite sitting between them chronologically (1994, predating Clark & Chalmers 1998): it isn't on the same axis. It's a different theoretical instrument, measuring something the geography framework doesn't capture.

## Mapping to Carse

Proposed in-thread (Skooter) and judged to have real traction: **pragmatic actions map to finite-game moves** (executed to reach a defined terminal state, closing the problem down) and **epistemic actions map to infinite-game moves** (executed to improve the conditions for play — restructuring the space so better moves become visible, maintaining capacity to continue playing well). The rotation that is "unnecessary" by pragmatic standards is necessary by infinite-game standards; it is meta-level relative to the pragmatic action.

## The three-instrument synthesis

A clean division of theoretical labor for the HAC framework:

1. **Kirsh/Maglio — strategy (the how).** An actionable design criterion: to promote learning over task completion, design for epistemic action. Interfaces, prompting structures, role rotation can all be evaluated by whether they induce users to manipulate the cognitive environment in ways that serve internal development, or whether they just move pieces to final position efficiently. Technology-independent: Socratic dialogue and well-kept lab notebooks are full of epistemic actions.

2. **Carse — values (the why).** Task completion is the finite game; learning is the infinite game. Not a design criterion but a normative orientation that precedes design.

3. **The geography nesting — mechanism and consequence.** What including technology does to the system: expanding it (Hutchins), extending the dyad (Clark/Chalmers), or quietly contracting individual capacity (Risko/Gilbert). This is where **cognitive onboarding** lives — the inward flow the geography framework has no canonical name for.

None of the three does another's job, which is what makes the combination productive rather than redundant.

## Connections and open items

- **Irony of Agency:** epistemic action is precisely the friction that the low-friction "write my paper" case eliminates. Workload outsourcing is the zero-epistemic-action limit — all pragmatic, no restructuring, no internal work served.
- **Distributed metacognition:** epistemic actions are candidate triggers for the metacognitive loop; the disfluency connection deserves explicit development.
- **Developmental thread:** the 1995 workspace framing generated the novice→master workspace question (desirable difficulties, apprenticeship as inhabiting the master's arrangement, AI as removing the master's shop) — captured in fleeting-workspace-friction-development.md, not developed here.
- **Still to acquire:** Risko & Gilbert (2016) flagged as not yet in hand; get the paper before the synthesis is promoted.
- **Promotion path:** the three-instrument synthesis is a strong candidate for its own permanent note (tracker Proposed Writings, next open slot); this literature note stays in /literature regardless.
