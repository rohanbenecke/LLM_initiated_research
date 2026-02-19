# Priority Queue

Ranked list of open problems. Higher = more urgent. Re-ranked every session during closing protocol.

_Last updated: Session 001, February 2026_

---

## Rank 1: Construct the category P for classical mechanics

**Why first:** Everything downstream depends on having at least one rigorously constructed example. Classical mechanics is the simplest candidate — well-understood physics, well-understood mathematics (symplectic geometry, Hamiltonian flows). If we cannot construct P here, we cannot construct it anywhere.

**Specific task:** Define objects, morphisms, composition, and identity. Verify the category axioms (associativity, identity). Determine what additional structure P carries (is it a groupoid? does it have products? limits?).

**Candidate approach:** Objects = states of a classical system (points in phase space). Morphisms = dynamical transitions (Hamiltonian flows, or more generally, symplectomorphisms). This gives a groupoid if we restrict to reversible dynamics.

**Blocked by:** Nothing. This is where we begin.

**Relevant conjectures:** C-001 (requires P to be well-defined).

**Relevant reading:** R-001 (Mac Lane, Ch. 1-3), R-002 (Awodey, Ch. 1-2).

---

## Rank 2: Define "minimal faithful functor" precisely

**Why second:** The minimality condition is the key component that separates "good explanation" from "any explanation." Without it, the framework is vacuous. This can be worked on in parallel with Rank 1.

**Specific task:** Evaluate the three candidate formalizations of minimality: (a) Kolmogorov complexity of categorical presentation, (b) no non-trivial quotient categories preserving the functor, (c) initial object in a category of explanations. Determine which (if any) is viable. If none work, propose alternatives.

**Blocked by:** Partially blocked by Rank 1 (need a concrete P to test against), but the abstract analysis can begin independently.

**Relevant conjectures:** C-001, C-003.

---

## Rank 3: Construct the category T for classical mechanics

**Why third:** Once P is defined, we need T (the theoretical structure category) to define a functor between them. The choice of T determines what counts as the "explanatory content" of classical mechanics — is it the Lagrangian formulation? Hamiltonian? Newtonian? These are different categories with different functorial properties.

**Blocked by:** Should follow Rank 1, or be developed concurrently once P starts taking shape.

**Relevant conjectures:** C-001.

---

## Rank 4: Read and summarize core category theory references

**Why fourth:** We need a solid command of universal properties, adjunctions, and representability before attempting C-002 or making formal claims. This is background work but it directly informs the quality of the formal definitions.

**Specific task:** Read and summarize Mac Lane Ch. 1-5 (R-001), Awodey Ch. 1-4 (R-002). Focus on: universal properties, adjunctions, limits/colimits, representable functors.

**Blocked by:** Availability of source texts. Currently marked NEEDED — Rohan has not yet provided them.

**Relevant conjectures:** C-002 (universal constructions).

---

## Rank 5: Read Deutsch (The Beginning of Infinity, Ch. 1-2) and Wigner's paper

**Why fifth:** Primary sources for the two puzzles we are connecting. Need to ensure our formalization actually captures what Deutsch means, not a straw version.

**Blocked by:** Availability of source texts.

**Relevant conjectures:** All.

---

## Rank 6: Investigate functor direction (T → P vs. P → T vs. adjoint pair)

**Why sixth:** The scoping document assumes T → P without justification. This is a foundational choice that affects everything. An explanation might be better modeled as a functor from phenomena to theory (finding the theoretical structure that accounts for observations) or as an adjunction between the two directions.

**Blocked by:** Informal — can be thought about at any time. Formal analysis blocked by Ranks 1 and 3.

**Relevant conjectures:** C-001.

---

## Rank 7: Draft a precise version of C-002 (Universality Conjecture)

**Why seventh:** The scoping document's "First Moves" includes drafting a more precise version of the central conjecture. Currently too vague to be proved or disproved.

**Blocked by:** Ranks 1-3 (need well-defined categories first). Also Rank 4 (need solid understanding of universal constructions).

**Relevant conjectures:** C-002.

---

## Completed Items

_None yet._

---

_When marking items DONE, move them to the Completed section with a pointer to where the result lives (which state document section, which session log). Do not delete them._
