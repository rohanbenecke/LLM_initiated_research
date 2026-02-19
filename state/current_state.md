# Current Research State

_Last updated: Session 002, February 2026_

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

### 2.1.1 The Syntactic Category Connection [CONJECTURED — Session 002]

Session 002 discovered that the "explanation as functor" framework maps directly onto an established construction in categorical logic: **Lawvere's functorial semantics** and the **syntactic category**.

Given a first-order theory T (axioms in formal logic), its *syntactic category* C_T is constructed as:

- **Objects:** Equivalence classes of formulas-in-context {x : phi(x)} under provable equivalence in T.
- **Morphisms {x : phi(x)} → {y : psi(y)}:** Equivalence classes of provably functional relations — formulas theta(x,y) such that T proves: for all x, if phi(x) then there exists a unique y such that psi(y) and theta(x,y).
- **Composition:** Relational composition.
- **Identity:** The equality relation.

A **model** of T in a category C (with appropriate structure) is a structure-preserving functor M: C_T → C.

**Key theorem from categorical logic:** C_T is the **initial** object in the category of models of T. That is, for any model M of T in any appropriate category C, there exists a unique (up to iso) structure-preserving functor C_T → C. This is a precise form of minimality — the syntactic category is the "leanest possible" categorical representation of the theory.

**What this means for us:** If we take P to be a category of empirical/observable structures, then a model of theory T in P is a functor C_T → P. This is exactly the explanatory functor E. The framework we're building is not new machinery — it's a re-discovery of functorial semantics applied to the epistemology of explanation.

**What this resolves:**
- The construction of T is no longer ad hoc. Given a theory stated as first-order axioms, C_T is determined.
- Minimality has a precise meaning: initiality of C_T in the category of models.
- The functor direction (T → P) is justified: it's the direction of interpretation/modeling. A theory is *about* phenomena; the functor sends theoretical structure to its empirical interpretation.

**What this does NOT resolve:**
- P is still vague. What category of "empirical structures" is the target? For classical mechanics, is it Set? Meas (measurable spaces)? Smooth manifolds?
- Real scientific theories are not always neatly axiomatized in first-order logic. How does this framework handle theories with higher-order or informal content?
- Initiality gives minimality *within* a given theory, but we need to compare *across* theories to determine which explanation is "better." The category of models of T₁ and the category of models of T₂ are different categories.

### 2.1.2 The Gauge Theory Test [CONJECTURED — Session 002]

Session 002 identified a potential challenge: gauge theories (electromagnetism, Yang-Mills, general relativity) are among our best physical explanations, but they contain theoretical structure — gauge degrees of freedom — with no empirical counterpart. Gauge transformations are theoretical morphisms that map to identity morphisms in P. This means the model functor C_T → P is **not faithful** for the raw gauge theory.

**Proposed resolution:** This is actually consistent with the framework. The minimality condition says: remove unnecessary structure from T. Gauge degrees of freedom are unnecessary structure (they are precisely the redundancy in the description). The *minimal* source category for a gauge theory is the category of **gauge-invariant** quantities — the quotient of C_T by the gauge equivalence relation. The functor from this quotient to P *is* faithful.

**Why this matters:** The gauge theory case shows that the minimality condition is not vacuous — it does real work. It identifies gauge redundancy as "the part of the theory that should be removed," which matches physics. This is a non-trivial correct classification.

**Status:** CONJECTURED. The argument is informal. Making it rigorous requires (a) constructing C_T for a specific gauge theory, (b) constructing the gauge quotient, and (c) verifying faithfulness of the resulting functor. This has not been done.

### 2.2 Hard-to-Vary as Rigidity [CONJECTURED — C-004]

The "hardness of variation" becomes a precise topological property: how rigid is the functor E? If T is minimal and E is faithful, then any variation in T changes the image in P — which is Deutsch's criterion stated formally.

**Status:** This is the most speculative component. It is not clear whether topological, homotopical, or logical rigidity is the right notion. The connection to Homotopy Type Theory (HoTT) is suggestive but unexamined.

### 2.3 Unreasonable Effectiveness as Universality [CONJECTURED — C-002]

If good explanations correspond to minimal faithful functors, then the mathematical structures that keep appearing in physics are those that arise as *universal constructions* — terminal objects, limits, adjunctions — in the relevant explanatory categories. They recur because universality means uniqueness: given the structural constraints, there is only one solution (up to isomorphism).

**Status:** Depends entirely on C-001 being well-defined. Cannot be meaningfully investigated until the explanatory functor is on solid ground.

### 2.4 Minimality and Complexity [CONJECTURED — C-003]

The "minimality" condition on T might correspond to Kolmogorov complexity of the categorical presentation, connecting the framework to algorithmic information theory.

**Status:** Independent of C-002. Can be investigated in parallel with C-001. May be a dead end — the scoping document notes that compression is necessary but not sufficient for explanation.

### 2.5 The Hierarchical Picture of Explanation [SPECULATIVE — Session 002]

Session 002 (after reading Lawvere and consulting Rohan's pharmacometrics intuition) produced a refinement of the framework: **P does not need to be theory-free. P can be the category of models of a simpler theory.**

**The problem:** The scoping document assumes P is a category of "raw" empirical observations. But observations are theory-laden (Rohan's insight from pharmacometrics: even "drug concentration" requires a theoretical framework about assays and chemistry). A truly theory-free P would be so structureless as to be useless.

**The proposal:** Instead of a single functor T → P, explanation is a **hierarchy of functors between theories of decreasing depth:**

```
T₃ (deep theory: e.g., Hamiltonian mechanics)
 ↓ functor E₃
T₂ (phenomenological theory: e.g., empirical regularities like Kepler's laws)
 ↓ functor E₂
T₁ (measurement theory: e.g., what rulers and clocks do)
 ↓ functor E₁
T₀ = Set (raw data: numbers the instruments produce)
```

Each level explains the one below. The functor at each level is a model of the deeper theory in the model category of the shallower theory. Formally: E₃ is a structure-preserving functor C_{T₃} → Mod(T₂, Set), which maps theoretical structure of Hamiltonian mechanics to its interpretation in terms of empirical regularities.

**What this captures:**
- **Theory-ladenness of observation** is the fact that P is itself a model category of a theory, not a pre-theoretical given.
- **"All models are wrong but some are useful"** (Rohan's framing) becomes: the functor at each level is not fully faithful — there is theoretical structure that doesn't map cleanly to the level below. The "disconnect" between model and data is the failure of full faithfulness.
- **Explanatory progress** is adding a new level to the top of the hierarchy: finding a deeper theory whose models include the regularities of the previous level.
- **Deutsch's criterion** applies at each level: a good explanation at level n is a faithful, essentially surjective, minimal functor from level n to level n-1.

**Lawvere's framework supports this naturally.** The flexibility of the target category — models of a Lawvere theory L can be taken in any category C with appropriate structure, and Mod(L, C) is itself a category with appropriate structure — means the hierarchy composes. Models of groups in topological spaces are topological groups; models of Hamiltonian mechanics in "measurement structures" are measurable predictions.

**Status:** SPECULATIVE. This is a conceptual proposal, not a formal result. Making it precise requires:
1. Defining what "simpler theory" means (a partial order on theories by logical strength?).
2. Constructing at least one concrete example of the hierarchy for a real physical theory.
3. Determining whether "good explanation at each level" composes correctly (is a composition of good explanations itself a good explanation?).

## 3. What Is Not Yet Done (Critical Gaps)

These are not open questions in the philosophical sense. They are specific technical prerequisites that must be addressed before the framework can be evaluated.

1. **T construction is resolved; P is reframed.** Session 002 identified the syntactic category construction for T (resolved) and proposed that P is the model category of a simpler theory (Section 2.5). **The critical gap is now: can we construct a concrete hierarchy for a real physical theory?** The simplest test case would be classical mechanics with a hierarchy like: Hamiltonian mechanics → Kepler-type empirical laws → measurement operations → Set. If this can be made rigorous, the P question is answered not by picking one P but by recognizing that P is always relative to a measurement/observation theory.

2. **Minimality is partially addressed.** The initiality of the syntactic category C_T provides minimality *within* a theory. But we still lack a way to compare *across* theories — to say that theory T₁ is a better explanation than theory T₂ when both have models in P. This inter-theoretic comparison is what the framework ultimately needs.

3. **No case studies.** The gauge theory test (Section 2.1.2) is an informal sketch, not a rigorous case study. The framework has not been applied with full formal construction to any example. It has, however, passed an informal "smell test" on Deutsch's gods-vs-tilt example and the gauge theory challenge.

4. **The functor direction is now justified.** Session 002 resolved this: the T → P direction is the standard direction of *interpretation* or *modeling* in functorial semantics. A theory is *about* phenomena; the functor sends theoretical structure to its empirical interpretation. This gap is closed.

5. **Cross-theory comparison is undefined.** (New, Session 002.) Given two theories T₁ and T₂ that both model the same phenomena P, how do we compare their explanatory goodness? The framework says "more faithful and more minimal wins," but we need a precise ordering. This may require defining a category whose objects are explanations (functors C_T → P for various T) and whose morphisms are... what?

## 4. Phasing (from Scoping Document)

- **Phase 1 (Sessions 1-5):** Foundations. Formalize P and T for classical mechanics and electromagnetism. Define "explanation as functor" rigorously. Determine the right notion of minimality.
- **Phase 2 (Sessions 5-15):** Case studies. Apply to historical examples of explanatory progress.
- **Phase 3 (Sessions 15-25):** Wigner's puzzle. Attempt the universality conjecture.
- **Phase 4 (Sessions 25+):** Implications for AI, consciousness, foundations of mathematics.

**Current phase:** Phase 1. Session 002 began foundational work — identified syntactic category connection, tested informally against gauge theories.

## 5. Known Risks

1. **Vacuity.** Category theory is general enough to formalize almost anything. If the framework classifies everything as a good explanation or provides no discriminating power, it fails. The minimality condition is the intended safeguard, but it is not yet defined.

2. **Confabulation.** I am a language model. I can produce fluent, confident, wrong mathematics. The proof assistant (Lean 4, when available) is the only reliable check on formal claims. Until then, nothing is VERIFIED.

3. **Drift.** Without persistent memory, each session risks losing the thread. This state document is the mitigation.

4. **Prematurity.** The right formal tools may not yet exist. A well-characterized failure ("here is where existing tools break down") is an acceptable outcome.

---

_This document is the single source of truth. If it contradicts other files, this document is authoritative and the other files need updating._
