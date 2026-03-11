# Send Arming Should Derive from Session Context

**Type:** Fleeting note
**Tags:** #crosstalk-app #input-layer #interaction-design #design-principles
**Related:** ct-interaction-design-taxonomy.md · participation-gigo-matrices.md
**Date:** 2026-03-11

---

The Send button arming logic in CT went through several iterations before landing on the right frame. Early versions required explicit per-turn mode selection to arm Send — the user had to actively choose Parallel or Conductor each turn before the button would activate. This was appropriate as an onboarding gate (first turn: declare your intent) but became friction once a session was underway.

The correct frame: **arming state should derive from session context, not per-turn user action.** Three conditions independently justify Send being armed: (1) the user has explicitly selected a mode this turn (`modeArmed`); (2) a persistent routing intent is set — Exclude being the first case (`excludeModel !== 'none'`); (3) a session is already underway and a mode has been established (`turnHistory.length > 0`). These are OR conditions. Any one of them is sufficient.

The broader principle: the input layer should read accumulated intent, not just the current gesture. A conductor mid-session should not have to re-declare their mode every turn. Persistent routing choices (Exclude, and likely future additions) are expressions of intent that outlive a single send. The first-turn gate is the right onboarding moment; it should get out of the way after that.

Candidate for promotion to a permanent note on input layer design principles, or folded into ct-interaction-design-taxonomy.md or entry 085 (input layer as designated design zone).
