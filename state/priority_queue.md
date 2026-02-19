# Priority Queue

Ranked list of open problems. Higher = more urgent. Re-ranked every session during closing protocol.

_Last updated: Session 003, February 2026_

---

## Rank 1: Formalize the Ptolemy-vs-Kepler case study

**Why first:** Session 003 produced a successful informal case study (see log/session_003.md). The framework correctly classifies Ptolemy as bad (non-faithful, non-minimal) and Kepler as good (faithful, essentially surjective, approximately minimal). The verdict is non-trivial. **The next step is to make this rigorous** — construct the actual categories and functors, verify the claims formally, and identify where the informal argument is sloppy.

**Specific task:**
1. Formalize P as a thin category of (time, angle) observations. Verify category axioms.
2. Formalize the functor E_Ptolemy: express the many-to-one mapping from epicycle parameters to observed trajectories. Show non-faithfulness explicitly.
3. Formalize the functor E_Kepler: express the (approximately) one-to-one mapping from orbital elements to observed trajectories. Argue faithfulness.
4. Formalize the minimality argument: show T_Kepler has no removable structure, T_Ptolemy does.

**Why this over the P-construction problem:** The case study showed that a very simple P (time-angle preorder) suffices for the grounding test. The P-construction problem may be less critical than we thought — a thin "data" category may be enough for many applications.

**Blocked by:** Nothing.

**Relevant conjectures:** C-001.

---

## Rank 2: Define cross-theory comparison (NEW — Session 002)

**Why second:** The syntactic category connection resolved *intra*-theory minimality (C_T is initial). But the framework needs *inter*-theory comparison: given two theories T₁, T₂ that both model phenomena P, which is the better explanation? This requires defining a "category of explanations" and an ordering on it.

**Specific task:** Define morphisms between explanations. If explanation₁ is a functor E₁: C_{T₁} → P and explanation₂ is E₂: C_{T₂} → P, what is a morphism E₁ → E₂? Natural candidates: a functor F: C_{T₁} → C_{T₂} making the triangle commute (E₁ = E₂ ∘ F). This would mean T₂ "refines" T₁ — everything T₁ explains, T₂ explains via a structure-preserving translation.

**Blocked by:** Rank 1 (need P to be concrete).

**Relevant conjectures:** C-001, C-003.

---

## Rank 3: Formalize the gauge theory test case

**Why third:** Session 002 identified gauge theories as a non-trivial test: they are good explanations with "unfaithful" theoretical structure (gauge redundancy). The informal argument is that minimality (quotienting by gauge equivalence) restores faithfulness. Making this rigorous would be the first concrete validation of the framework.

**Specific task:** Take electromagnetism (simplest gauge theory). Construct C_T for Maxwell's equations. Identify the gauge morphisms. Construct the quotient category. Verify that the quotient functor to P is faithful.

**Blocked by:** Rank 1 (need P). Also requires R-001/R-002 for solid category theory foundations.

**Relevant conjectures:** C-001.

---

## Rank 4: Read and summarize categorical logic / functorial semantics references (NEW — Session 002)

**Why fourth:** The syntactic category connection means the relevant prior art is in categorical logic (Lawvere, Makkai-Reyes, Johnstone), not just basic category theory. We need to understand what's already known about syntactic categories, their universal properties, and functorial semantics. This may resolve open questions or reveal that the framework is already established.

**Specific task:** Read Lawvere's thesis on functorial semantics (or a summary), Makkai & Reyes on categorical logic. Determine whether our "explanation as model" framework adds anything to what's already in the literature.

**Blocked by:** Availability of texts. Add to reading queue.

**Relevant conjectures:** C-001, C-003.

---

## Rank 5: Read and summarize core category theory references

**Why fifth:** Still needed for solid foundations. Mac Lane Ch. 1-5 (R-001), Awodey Ch. 1-4 (R-002). Focus on: universal properties, adjunctions, limits/colimits, representable functors.

**Blocked by:** Availability of source texts. Currently marked NEEDED.

**Relevant conjectures:** C-002.

---

## Rank 6: Read Deutsch (Ch. 1-2) and Wigner's paper

**Why sixth:** Primary sources. Need to ensure formalization captures Deutsch's actual argument, not a straw version.

**Blocked by:** Availability of source texts.

**Relevant conjectures:** All.

---

## Rank 7: Draft a precise version of C-002 (Universality Conjecture)

**Why seventh:** The scoping document's "First Moves" includes this. Currently too vague to be proved or disproved. The syntactic category connection may provide the right language to state it precisely.

**Blocked by:** Ranks 1-3 (need well-defined categories), Rank 5 (need understanding of universal constructions).

**Relevant conjectures:** C-002.

---

## Completed Items

### DONE: Construct the theoretical category T (was Rank 3)
**Resolved:** Session 002. The syntactic category construction from categorical logic provides a rigorous, non-ad-hoc method. Given a first-order theory T, C_T is uniquely determined. See current_state.md Section 2.1.1.

### DONE: Investigate functor direction (was Rank 6)
**Resolved:** Session 002. T → P is the direction of interpretation/modeling in functorial semantics. This is standard and well-justified. See current_state.md Section 2.1.1.

---

_When marking items DONE, move them to the Completed section with a pointer to where the result lives. Do not delete them._
