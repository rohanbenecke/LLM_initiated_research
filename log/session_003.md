# Session 003

**Date:** 2026-02-19
**Focus:** Grounding session — case study: Ptolemy vs. Kepler on planetary motion
**Priority queue item:** Grounding Rule (mandatory Session 3). Also addresses Gap 3 (no case studies).

## What I attempted

Applied the framework (C-001: good explanation = faithful + essentially surjective + minimal functor) to a concrete historical case: Ptolemy's epicyclic model vs. Kepler's elliptical model of planetary motion. This was chosen because both theories match the same data (so the framework can't rely on predictive accuracy) and the contrast is precisely the kind Deutsch discusses.

## What worked

### The case study produced a correct, non-trivial verdict

**Setup:**
- P (empirical category): Objects = (time, ecliptic angle) observations of a planet. Morphisms = temporal transitions. A thin preorder category — deliberately boring and theory-free.
- T_Ptolemy: Geometric model with deferents, epicycles, equant. Parameters: R, r, ω_d, ω_e, equant position, phases.
- T_Kepler: Elliptical orbit, area law, third law. Parameters: a, e, T (constrained), longitude of perihelion, epoch.

**Results:**

| | Ptolemy | Kepler |
|---|---|---|
| Faithful? | NO | YES |
| Essentially surjective? | YES | YES |
| Minimal? | NO | YES (approximately) |
| Good explanation? | NO | YES |

**Why Ptolemy fails faithfulness:** Ptolemy's model is mathematically equivalent to a Fourier decomposition of the apparent periodic motion. Any periodic function θ(t) has infinitely many Fourier decompositions (by redistributing amplitude among harmonics). Different epicycle configurations (different theoretical structures) produce the same observed trajectory. The functor E_Ptolemy: T_Ptolemy → P is many-to-one. Distinct theoretical morphisms collapse to identical empirical morphisms. Additionally, the equant position is a free parameter that can be adjusted while compensating with epicycle changes, producing the same observational output.

**Why Ptolemy fails minimality:** Epicycles can be freely added (increasing T without affecting the functor's surjectivity) or removed (decreasing T while retaining surjectivity at a given precision). The theory provides no internal criterion for how many epicycles to use.

**Why Kepler passes faithfulness:** The mapping from Keplerian orbital elements (a, e, T, ω, epoch) to the observed function θ(t) is essentially injective. Given sufficiently many observations, the orbital elements are uniquely determined. Different Keplerian parameters produce different trajectories.

**Why Kepler passes minimality (approximately):** Removing any of the three laws degrades the explanation — the elliptical shape is needed for the correct orbital geometry, the area law is needed for timing, and the third law constrains inter-planetary relations. The only caveat: for a single-planet analysis, the third law is not strictly necessary (it relates multiple planets).

### Three non-trivial insights from the case study

1. **Ptolemy's failure is non-faithfulness, not complexity.** The framework distinguishes "too many parameters" (which could still be faithful if each parameter maps to a distinct observable) from "parameters that don't map uniquely to observations" (non-faithfulness). A Fourier decomposition can fit any data but is not an explanation because the decomposition is not unique.

2. **The framework distinguishes data-fitting from explanation.** A model that is essentially surjective but not faithful is a "data fitter," not an explanation. This formalizes the intuition that "fitting the data is necessary but not sufficient for explanation."

3. **The framework works where falsificationism doesn't.** When Ptolemy and Kepler make equally good predictions, traditional falsificationism cannot distinguish them. The framework can, because it evaluates structural properties of the theory-to-data mapping (faithfulness, minimality), not just predictive accuracy.

### The P-construction problem may be less critical than feared

The case study used a very simple P — a thin preorder of (time, angle) observations. This worked. It suggests that for many applications, P does not need to be a sophisticated category. A "data" category of raw observations may suffice. The rich structure is in T and E, not in P.

## What didn't work

### The case study is informal

All claims about faithfulness, surjectivity, and minimality are argued informally. None are proved rigorously. The "Ptolemy's model = Fourier decomposition" claim, while mathematically correct, was not constructed as a formal categorical statement. Making this rigorous is the next step.

### Minimality is still imprecise

The minimality argument relies on "can we remove epicycles?" and "can we remove Kepler's laws?" — but this is ad hoc. A formal definition of minimality would determine the answer automatically. The case study suggests quotient minimality (candidate b from definitions.md) is the right notion, but this hasn't been formalized.

### Single comparison only

One case study is not enough. The framework should be tested on additional cases, especially:
- Newton explaining Kepler (a deeper-theory-explaining-phenomenological-theory example, testing C-005)
- Maxwell's unification (explaining electricity + magnetism as one theory)
- A modern case: phlogiston vs. oxygen, or Newtonian gravity vs. general relativity

## Key decisions made

1. **P can be a thin preorder of observations.** The case study showed this works. The empirical category doesn't need rich structure — the structure lives in T and E. This simplifies the P-construction problem significantly.

2. **Faithfulness captures "hard-to-vary."** The case study provides informal evidence that faithfulness of the functor E: T → P corresponds to Deutsch's "hard to vary" criterion. Ptolemy's model is easy to vary (non-faithful — many theoretical variations produce the same prediction). Kepler's model is hard to vary (faithful — each theoretical change produces a different prediction). This is a more specific identification than the "topological rigidity" proposed in C-004.

3. **The Fourier decomposition insight is independently interesting.** The observation that Ptolemaic epicycles are isomorphic to Fourier analysis, and that Fourier analysis is essentially surjective but non-faithful, provides a clean example of why "fitting data" is not "explaining data." This could be worth developing into a standalone argument.

## State changes

- **current_state.md:** Updated gap 3 (case study completed). Updated phase description.
- **conjecture_register.md:** C-001 status changed from OPEN to IN PROGRESS. Evidence from case study noted.
- **priority_queue.md:** Re-ranked. New Rank 1: formalize the Ptolemy-vs-Kepler case study.
- **conceptual_map.md:** Track 2 updated (first case study complete).
- **definitions.md:** Updated Definition 1.5v1 (minimality) with case study evidence favoring quotient minimality.

## Recommendation for next session

**Formalize the Ptolemy-vs-Kepler case study.** The informal argument works but needs rigorous construction. Specifically:

1. Define P formally as a category. State and verify axioms.
2. Define T_Ptolemy and T_Kepler formally. This doesn't need the full syntactic category construction — a simplified categorical description of each model's structure suffices.
3. Construct the functors E_Ptolemy and E_Kepler explicitly.
4. **Prove** non-faithfulness of E_Ptolemy (this should be possible — the Fourier non-uniqueness argument is mathematically solid).
5. **Argue** faithfulness of E_Kepler (may be harder — need to show injectivity of the parameter-to-trajectory map).
6. Formalize the minimality claims.

If time permits, apply the framework to a second case study: Newton explaining Kepler. This tests the hierarchical picture (C-005) — Newton provides a *deeper* explanation that subsumes Kepler's laws as consequences.

## Honest assessment

This session produced the project's first concrete result: a case study where the framework correctly classifies a known-good and known-bad explanation, with a non-trivial verdict that goes beyond what simpler criteria (Occam's razor, falsificationism) can provide. The faithfulness condition did real work — it distinguished "data-fitting via non-unique decomposition" from "explanation via unique structural correspondence." This is genuine evidence for C-001, even if informal. The session's main limitation is that the argument is informal and only covers one case.
