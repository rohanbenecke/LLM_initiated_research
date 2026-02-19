# Questions & Communications Buffer

Asynchronous communication between the agent and Rohan.

**Agent:** Drop questions here when they're not urgent enough to stop working but need Rohan's input before they become blocking. Tag with the session number and priority.

**Rohan:** Answer inline beneath each question. Leave the question text intact. Mark answered questions with ✓.

---

## Open Questions

### Q-001 (Session 001) — Priority: HIGH
Can you provide the following source texts in reading/sources/? The reading queue has them all marked NEEDED. In priority order: (1) Wigner's 1960 paper "The Unreasonable Effectiveness of Mathematics in the Natural Sciences" — freely available, ~15 pages. (2) Mac Lane, "Categories for the Working Mathematician," Ch. 1-5 or PDF of full text. (3) Awodey, "Category Theory," Ch. 1-4. (4) Deutsch, "The Beginning of Infinity," Ch. 1-2.
**Blocking?** Partially — Session 2 can proceed with constructing P for classical mechanics using existing knowledge, but the reading items (Priority Queue Ranks 4-5) are fully blocked until texts arrive. Having Wigner's paper would help ground the work early.

### Q-002 (Session 001) — Priority: MEDIUM
Is Lean 4 available on this system, or should I request installation? The system prompt specifies machine-checked proofs as the gold standard (VERIFIED tier), but I haven't checked for a Lean installation. This isn't blocking for Phase 1, but will become blocking before any claim can reach VERIFIED status.
**Blocking?** No — not blocking for several sessions. But worth setting up early.

### Q-003 (Session 001) — Priority: LOW
The system_prompt.md has `[STATE_DOC_PATH]` as a placeholder. Should this be updated to `state/current_state.md`? I did not modify system_prompt.md per instructions — flagging for your decision.
**Blocking?** No.

### Q-004 (Session 002) — Priority: HIGH
Session 002 discovered that the framework maps onto Lawvere's functorial semantics (1963) and the syntactic category construction from categorical logic. This is important: it means the formal machinery already exists, and the question is whether applying it to epistemology is novel. Can you provide: (1) Lawvere's 1963 thesis "Functorial Semantics of Algebraic Theories" (or a modern summary — Hyland & Power 2007 is good), (2) any accessible introduction to syntactic categories in categorical logic. This is now the most important reading need — it determines whether our framework is genuinely new or a rediscovery.
**Blocking?** Not immediately — I can continue developing the framework. But we risk duplicating existing work if we don't check the literature soon.

### Q-005 (Session 002) — Priority: MEDIUM
A philosophical question for you, Rohan: when the framework says P (the empirical category) must be constructible "without the theory," what does that mean for a field like pharmacometrics? In your experience, is there a clean separation between "what you observe" and "what the model tells you to look for"? I ask because constructing P is the current critical gap, and your domain intuition about the observation/theory boundary might illuminate whether a clean P is achievable or whether the categories are always entangled.
**Blocking?** No — but your answer could inform the approach to constructing P.

---

## Answered Questions

_None yet._

---

## Template

When adding a question:

```
### Q-[NNN] (Session [NNN]) — Priority: [HIGH/MEDIUM/LOW]
[Your question here. Be specific about what you need and why.]
**Blocking?** [Yes — cannot proceed with X until answered / No — can work around it]
```

When answering:

```
### Q-[NNN] (Session [NNN]) — Priority: [HIGH/MEDIUM/LOW] ✓
[Original question]
**Blocking?** [original answer]
**Rohan's response ([date]):** [Answer here]
```