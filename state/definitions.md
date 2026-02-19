# Formal Definitions

All definitions used in this project, versioned and tagged with confidence tiers. Never silently overwrite — when revising, create a new version and note what changed and why.

_Last updated: Session 002, February 2026_

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

## Definition 1.2v1: The Theoretical Category T [SUPERSEDED by 1.2v2]

**Introduced:** Session 001 (from scoping document)
**Confidence:** SPECULATIVE — described informally, not yet rigorously constructed

A category **T** whose:
- **Objects** are theoretical constructs (mathematical objects postulated by a theory to explain phenomena).
- **Morphisms** are logical or mathematical entailments between theoretical constructs.
- **Composition** and **identity** are standard mathematical composition and identity maps.

**Open issues:**
- Same imprecision as P. For classical mechanics, objects might be: elements of a Lie algebra, Hamiltonians, Lagrangians, etc.
- The relationship between T and the mathematical formalism of a physical theory needs clarification. Is T the formalism itself, or a category derived from it?

**Superseded by 1.2v2** — Session 002 identified the syntactic category as the right construction.

---

## Definition 1.2v2: The Theoretical Category as Syntactic Category

**Introduced:** Session 002
**Confidence:** CONJECTURED — construction is standard in categorical logic; its application to explanatory goodness is the conjecture

Given a first-order theory T (a set of axioms in a formal language), the **syntactic category** C_T is:

- **Objects:** Equivalence classes of formulas-in-context {x : phi(x)} under provable equivalence in T. Two formulas phi(x) and psi(x) are equivalent if T proves: for all x, phi(x) if and only if psi(x).
- **Morphisms {x : phi(x)} → {y : psi(y)}:** Equivalence classes of provably functional relations. A morphism is (represented by) a formula theta(x,y) such that T proves: for all x, if phi(x) then there exists a unique y such that psi(y) and theta(x,y).
- **Composition:** Given theta₁: {x:phi} → {y:psi} and theta₂: {y:psi} → {z:chi}, their composite is {(x,z) : exists y, theta₁(x,y) and theta₂(y,z)}: {x:phi} → {z:chi}.
- **Identity:** The equality formula: id_{x:phi} is represented by "x = y and phi(x)."

**Key property:** C_T is the **initial** object in the category of T-models in categories with appropriate structure. For any model M of T in a category C, there exists a unique (up to iso) structure-preserving functor C_T → C. Source: Lawvere's functorial semantics, Makkai & Reyes categorical logic.

**What this means for the project:** T is no longer ad hoc. Given any scientific theory that can be stated as first-order axioms, C_T is uniquely determined. The explanatory functor E: C_T → P is then a model of the theory in the empirical category.

**Open issues:**
- Requires the scientific theory to be expressible in first-order logic. Some theories may require higher-order or type-theoretic formulations. The construction generalizes (e.g., to typed theories, essentially algebraic theories) but each generalization needs checking.
- The syntactic category can be enormous (proper-class-sized if the language is). In practice, we work with small subcategories relevant to specific explanatory contexts.
- The initiality property gives minimality of the syntactic presentation. But is this the right kind of minimality for explanatory goodness? A syntactic category with redundant axioms is still initial (the redundant axioms don't change the provability relation). So "minimal" might mean: minimal *axiomatization* of the theory, not just minimal category.

---

## Definition 1.3v1: Explanation (as Functor)

**Introduced:** Session 001 (from scoping document)
**Confidence:** CONJECTURED — the core thesis, C-001

An **explanation** of phenomena in P by a theory T is a functor **E: T → P** that maps theoretical structure onto empirical structure while preserving relationships (composition and identities).

**Open issues:**
- ~~Why T → P and not P → T?~~ **Resolved, Session 002.** The T → P direction is the standard direction of interpretation in functorial semantics. A model of a theory T in a category P is a functor C_T → P. This is how mathematical logic has always worked: theories map *into* their models.
- The adjoint pair idea is not dead but is now reframed: there may be an adjunction between the "free theory on observations" and the "model of theory in observations," but the primary explanatory functor is T → P.

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
- **Session 003 update:** Minimality was tested informally in the Ptolemy-vs-Kepler case study. Ptolemy fails minimality (epicycles can be added/removed freely). Kepler passes (each law is necessary). The relevant notion of minimality here is closest to candidate (b) — quotient minimality — because the question was "can we remove structure and still have a faithful, essentially surjective functor?"
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
