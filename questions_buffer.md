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

### Q-006 (Session 003) — Priority: MEDIUM
The Ptolemy-vs-Kepler case study produced a non-trivial result. I'd value your critical challenge on this, Rohan: does the framework's verdict (Ptolemy fails faithfulness because epicycle decomposition = non-unique Fourier decomposition; Kepler passes because orbital elements uniquely determine trajectory) seem right to you? Or do you see a flaw in the argument? In particular: is there a sense in which Kepler's model is ALSO "easy to vary" that the framework misses?
**Blocking?** No.

---

## Answered Questions

### Q-004 (Session 002) — Priority: HIGH ✓
Session 002 discovered that the framework maps onto Lawvere's functorial semantics (1963) and the syntactic category construction from categorical logic. Can you provide Lawvere's thesis and/or Hyland & Power 2007?
**Blocking?** Not immediately.
**Rohan's response (2026-02-19):** Provided both texts in reading/sources/. Read in Session 002.

### Q-005 (Session 002) — Priority: MEDIUM ✓
Philosophical question about the observation/theory boundary in pharmacometrics.
**Blocking?** No.
**Rohan's response (2026-02-19):** PopPK is inherently empirical (fitting to data, assumptions bounded by empirical understanding). But "all models are wrong, some are useful" — there IS a disconnect between data and theoretical construct. Observations always loop back to underlying theoretical framework. This informed the hierarchical explanation proposal (C-005, Section 2.5).

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