# Current Research State

_Last updated: Session 001, February 2026_

---

## 1. The Core Question

**Can the concept of "good explanation" — in David Deutsch's sense — be formally characterized, and does such a characterization resolve Wigner's puzzle about the unreasonable effectiveness of mathematics?**

Deutsch argues that the fundamental unit of scientific progress is not prediction or falsification but *good explanation*: an account that is hard to vary while still accounting for the phenomenon it purports to explain. This criterion has never been formalized.

Wigner observed that mathematical structures developed for purely abstract reasons repeatedly turn out to describe physical reality with extraordinary precision. This remains unexplained.

**Working thesis:** These are the same puzzle. Good explanations identify deep structural invariances in phenomena. Mathematics is effective because it is the language of structural invariance. A formal account of explanatory goodness would simultaneously explain mathematical recurrence in physics and provide a criterion for distinguishing genuine explanation from curve-fitting.

## 2. Proposed Framework

### 2.1 Explanation as Functor [CONJECTURED — C-001]

Let **P** be a category whose objects are observable phenomena and whose morphisms are empirical relationships (correlations, causal dependencies, temporal sequences).

Let **T** be a category whose objects are theoretical constructs and whose morphisms are logical or mathematical entailments.

An *explanation* is a functor **E: T → P** that maps theoretical structure onto empirical structure in a way that preserves relationships.

A *good explanation* is a functor that is:

1. **Faithful**: For every pair of objects X, Y in T, the map E: Hom(X,Y) → Hom(EX, EY) is injective. This means the explanation does not conflate distinct theoretical relationships. Prevents vagueness.

2. **Essentially surjective**: Every object in P is isomorphic to E(X) for some X in T. Every phenomenon in the domain has a theoretical counterpart. Ensures scope.

3. **Minimal**: T has no unnecessary structure — nothing can be removed without losing faithfulness or surjectivity. Captures parsimony and hard-to-vary.

**Status:** This is the core thesis. None of these conditions have been rigorously tested against real scientific theories. The direction of the functor (T → P, mapping theory onto phenomena) is a choice that needs examination — the reverse direction (P → T) or an adjoint pair might be more appropriate.

### 2.2 Hard-to-Vary as Rigidity [CONJECTURED — C-004]

The "hardness of variation" becomes a precise topological property: how rigid is the functor E? If T is minimal and E is faithful, then any variation in T changes the image in P — which is Deutsch's criterion stated formally.

**Status:** This is the most speculative component. It is not clear whether topological, homotopical, or logical rigidity is the right notion. The connection to Homotopy Type Theory (HoTT) is suggestive but unexamined.

### 2.3 Unreasonable Effectiveness as Universality [CONJECTURED — C-002]

If good explanations correspond to minimal faithful functors, then the mathematical structures that keep appearing in physics are those that arise as *universal constructions* — terminal objects, limits, adjunctions — in the relevant explanatory categories. They recur because universality means uniqueness: given the structural constraints, there is only one solution (up to isomorphism).

**Status:** Depends entirely on C-001 being well-defined. Cannot be meaningfully investigated until the explanatory functor is on solid ground.

### 2.4 Minimality and Complexity [CONJECTURED — C-003]

The "minimality" condition on T might correspond to Kolmogorov complexity of the categorical presentation, connecting the framework to algorithmic information theory.

**Status:** Independent of C-002. Can be investigated in parallel with C-001. May be a dead end — the scoping document notes that compression is necessary but not sufficient for explanation.

## 3. What Is Not Yet Done (Critical Gaps)

These are not open questions in the philosophical sense. They are specific technical prerequisites that must be addressed before the framework can be evaluated.

1. **P and T are not constructed.** We have informal descriptions ("objects are observable phenomena") but no rigorous category for any specific physical theory. Without this, every claim about the framework is untestable. This is the first priority.

2. **"Minimal" is not defined.** This is a project-specific term with no standard meaning in category theory. Three candidate formalizations exist (see glossary) but none have been evaluated.

3. **No case studies.** The framework has not been applied to a single concrete example. Until it classifies at least one known-good and one known-bad explanation correctly, it is pure speculation.

4. **The functor direction is assumed, not argued.** Why T → P rather than P → T? The scoping document chooses T → P but does not justify it.

## 4. Phasing (from Scoping Document)

- **Phase 1 (Sessions 1-5):** Foundations. Formalize P and T for classical mechanics and electromagnetism. Define "explanation as functor" rigorously. Determine the right notion of minimality.
- **Phase 2 (Sessions 5-15):** Case studies. Apply to historical examples of explanatory progress.
- **Phase 3 (Sessions 15-25):** Wigner's puzzle. Attempt the universality conjecture.
- **Phase 4 (Sessions 25+):** Implications for AI, consciousness, foundations of mathematics.

**Current phase:** Phase 1. Session 001 is infrastructure setup.

## 5. Known Risks

1. **Vacuity.** Category theory is general enough to formalize almost anything. If the framework classifies everything as a good explanation or provides no discriminating power, it fails. The minimality condition is the intended safeguard, but it is not yet defined.

2. **Confabulation.** I am a language model. I can produce fluent, confident, wrong mathematics. The proof assistant (Lean 4, when available) is the only reliable check on formal claims. Until then, nothing is VERIFIED.

3. **Drift.** Without persistent memory, each session risks losing the thread. This state document is the mitigation.

4. **Prematurity.** The right formal tools may not yet exist. A well-characterized failure ("here is where existing tools break down") is an acceptable outcome.

---

_This document is the single source of truth. If it contradicts other files, this document is authoritative and the other files need updating._
