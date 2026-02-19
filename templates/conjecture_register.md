# Conjecture Register

This is the intellectual spine of the research. Every conjecture the project generates lives here, with its status, lineage, and implications.

## Status Key

- **OPEN**: Stated but not yet worked on
- **IN PROGRESS**: Currently being investigated
- **PROVED**: Formally verified (must have VERIFIED-tier evidence in current_state.md)
- **ARGUED**: Informally proved with complete reasoning chain (ARGUED-tier)
- **DISPROVED**: Shown to be false (record the counterexample or proof of negation)
- **REFORMULATED**: Original version was wrong or imprecise; replaced by a successor conjecture
- **ABANDONED**: No longer considered relevant or tractable (moved to dead_ends.md with post-mortem)

---

## C-001: The Explanatory Functor Conjecture

**Status:** OPEN **Introduced:** Scoping document, February 2026 **Statement:** A "good explanation" in Deutsch's sense can be formally characterized as a faithful, essentially surjective functor E: T → P from a minimal source category T (theoretical structure) to a target category P (empirical phenomena). **Lineage:** Direct formalization of Deutsch's qualitative criterion. Core thesis of the project. **If true:** Provides the first formal definition of explanatory goodness. Unlocks everything downstream. **If false:** The entire framework needs rethinking. But _how_ it fails will be informative — does it fail because functors are too rigid, too loose, or the wrong kind of morphism entirely? **Dependencies:** Requires rigorous construction of P and T for at least one physical theory.

---

## C-002: The Universality Conjecture

**Status:** OPEN **Introduced:** Scoping document, February 2026 **Statement:** Mathematical structures that recurrently appear across disparate physical theories correspond to universal constructions (terminal objects, limits, adjunctions) in the categories relevant to explanation. **Lineage:** Proposed resolution of Wigner's puzzle via C-001. **If true:** Wigner's puzzle dissolves — mathematics is exactly as effective as it should be, because universal constructions are unique solutions to structural constraints. **If false:** Either the framework is wrong (C-001 fails) or universality is not the right categorical concept. Check whether representability or Kan extensions would work instead. **Dependencies:** Depends on C-001. Cannot be meaningfully investigated until the explanatory functor is well-defined.

---

## C-003: The Minimality-Complexity Conjecture

**Status:** OPEN **Introduced:** Scoping document, February 2026 **Statement:** The "minimality" condition on the source category T (in C-001) corresponds to — or can be made precise via — Kolmogorov complexity of the categorical presentation. **Lineage:** Attempt to connect the framework to algorithmic information theory. **If true:** Provides a computable (in principle) measure of explanatory goodness and connects to MDL/Solomonoff tradition. **If false:** Need an alternative notion of minimality. Likely candidates: minimality in the sense of having no non-trivial quotient categories, or initial objects in some category of explanations. **Dependencies:** Independent of C-002. Can be investigated in parallel with C-001.

---

## C-004: The Hardness-Rigidity Conjecture

**Status:** OPEN **Introduced:** Scoping document, February 2026 **Statement:** Deutsch's "hard to vary" criterion corresponds to a topological or homotopical rigidity property of the explanatory functor — specifically, that small perturbations of T necessarily destroy the functorial property. **Lineage:** Attempt to make "hard to vary" precise using HoTT or related tools. **If true:** Provides a quantitative measure of explanatory goodness (how rigid is the functor?) and connects to homotopy type theory. **If false:** "Hard to vary" may not be a topological property at all. Consider whether it's better captured as a logical property (e.g., the theory has few models) or a combinatorial one. **Dependencies:** Somewhat independent of C-001 — can be explored even with a provisional definition of the functor.

---

_When adding new conjectures, use the next sequential number (C-005, C-006, ...). Never reuse a number, even if the conjecture is abandoned. The numbering is a permanent record._