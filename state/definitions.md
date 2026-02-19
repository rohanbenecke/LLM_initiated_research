# Formal Definitions

All definitions used in this project, versioned and tagged with confidence tiers. Never silently overwrite — when revising, create a new version and note what changed and why.

_Last updated: Session 001, February 2026_

---

## Definition 1.1v1: The Empirical Category P

**Introduced:** Session 001 (from scoping document)
**Confidence:** SPECULATIVE — described informally, not yet rigorously constructed

A category **P** whose:
- **Objects** are observable phenomena (states of a physical system accessible to measurement).
- **Morphisms** are empirical relationships between phenomena: correlations, causal dependencies, temporal successions, or experimental transformations.
- **Composition** is the sequential application of empirical relationships.
- **Identity** morphisms represent "no change" — the trivial empirical relationship of a phenomenon to itself.

**Open issues:**
- "Observable phenomena" is imprecise. For a concrete theory, objects might be: measurement outcomes, points in phase space, field configurations, etc. The right choice depends on the theory.
- What counts as a morphism? If morphisms are causal relations, P is a preorder (at most one morphism between any two objects). If morphisms are dynamical transitions, P may be richer. This choice matters.
- Category axioms have not been verified for any specific instantiation.

---

## Definition 1.2v1: The Theoretical Category T

**Introduced:** Session 001 (from scoping document)
**Confidence:** SPECULATIVE — described informally, not yet rigorously constructed

A category **T** whose:
- **Objects** are theoretical constructs (mathematical objects postulated by a theory to explain phenomena).
- **Morphisms** are logical or mathematical entailments between theoretical constructs.
- **Composition** and **identity** are standard mathematical composition and identity maps.

**Open issues:**
- Same imprecision as P. For classical mechanics, objects might be: elements of a Lie algebra, Hamiltonians, Lagrangians, etc.
- The relationship between T and the mathematical formalism of a physical theory needs clarification. Is T the formalism itself, or a category derived from it?

---

## Definition 1.3v1: Explanation (as Functor)

**Introduced:** Session 001 (from scoping document)
**Confidence:** CONJECTURED — the core thesis, C-001

An **explanation** of phenomena in P by a theory T is a functor **E: T → P** that maps theoretical structure onto empirical structure while preserving relationships (composition and identities).

**Open issues:**
- Why T → P and not P → T? The direction encodes a claim: the theory maps onto the phenomena, not the other way around. This may be wrong.
- An adjoint pair (a functor T → P left adjoint to a functor P → T) might better capture the bidirectional nature of explanation: theory predicts phenomena, and phenomena constrain theory.

---

## Definition 1.4v1: Good Explanation

**Introduced:** Session 001 (from scoping document)
**Confidence:** CONJECTURED — the core thesis, C-001

A **good explanation** is a functor E: T → P that is simultaneously:

1. **Faithful** — for every pair of objects X, Y in T, the induced map Hom_T(X,Y) → Hom_P(EX, EY) is injective. Distinct theoretical relationships map to distinct empirical relationships.

2. **Essentially surjective** — every object in P is isomorphic to E(X) for some X in T. The theory covers all phenomena in its domain.

3. **Minimal** — T has no unnecessary structure. Nothing can be removed from T without losing faithfulness or essential surjectivity.

**Open issues:**
- Conditions (1) and (2) are standard categorical properties. Condition (3) is not. It is the least understood and most important condition — see Definition 1.5v1.
- A faithful and essentially surjective functor is sometimes called a "surjective equivalence" in some contexts. The relationship to categorical equivalences should be examined.
- Should we also require fullness? A full and faithful functor is a fully faithful embedding. Adding fullness would mean every empirical relationship between theoretically-described phenomena arises from a theoretical relationship. This might be too strong (there could be empirical correlations not explained by the theory) or exactly right (a complete explanation should account for all relationships in its domain).

---

## Definition 1.5v1: Minimality of a Category (Preliminary)

**Introduced:** Session 001 (from scoping document)
**Confidence:** SPECULATIVE — not yet formalized, multiple candidate definitions

The source category T in a good explanation is **minimal** if it contains no unnecessary structure — nothing can be removed without destroying the functor's faithfulness or essential surjectivity.

**Candidate formalizations (all untested):**

(a) **Complexity minimality:** T has minimal Kolmogorov complexity among all categories admitting a faithful, essentially surjective functor to P. (Connects to algorithmic information theory. See C-003.)

(b) **Quotient minimality:** T has no non-trivial quotient category T' such that E factors through the quotient map T → T' as a faithful, essentially surjective functor T' → P. (A purely categorical formulation.)

(c) **Initiality:** T is an initial object in some category of explanations — i.e., the simplest explanation that works, in a precise universal sense. (Most elegant if it works. Requires defining a "category of explanations," which is meta-level machinery.)

**Open issues:**
- None of these have been tested against examples.
- Candidates (a) and (b) may not be equivalent. Determining their relationship is an open question.
- Candidate (c) requires defining what morphisms between explanations are, which is itself non-trivial.

---

## Definition 1.6v1: Hard-to-Vary (Preliminary)

**Introduced:** Session 001 (from scoping document)
**Confidence:** SPECULATIVE — not yet formalized

An explanation E: T → P is **hard to vary** if small perturbations of T necessarily destroy the functorial property of E. "Perturbation" here is informal — it might mean: changing a morphism in T, removing an object, modifying composition.

**Proposed formalization direction:** Rigidity in the sense of homotopy theory or deformation theory. If the functor E has no non-trivial deformations (the deformation space is a point), then the explanation is maximally hard to vary. See C-004.

**Open issues:**
- "Perturbation of a category" is not a standard notion. Defining it precisely is a prerequisite.
- The connection to HoTT is suggestive but has not been developed.

---

_When adding new definitions, use the next sequential major number (2.1, 2.2, ...). When revising, increment the version (e.g., 1.3v1 → 1.3v2) and note what changed._
