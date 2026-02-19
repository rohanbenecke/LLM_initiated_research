# R-010 (partial): Hyland & Power — "The Category Theoretic Understanding of Universal Algebra: Lawvere Theories and Monads" (2007)

**Read:** Session 002 (full paper)
**Relevance to project:** HIGH — historical context and technical details of Lawvere theories vs. monads

## Summary

A historical survey of how Lawvere theories and monads relate as two category-theoretic formulations of universal algebra. Lawvere theories (1963) are more directly connected to algebra; monads arose independently from algebraic topology. Despite Lawvere theories being more natural and supporting better constructions (sum, tensor of theories), monads dominated because: (a) enriched category theory wasn't developed yet, (b) Gabriel-Ulmer's notion of finiteness came later, (c) categorical logic favoring Lawvere theories came later.

The paper traces how computational effects (Moggi, late 1980s) brought renewed interest in Lawvere theories, since computational effects are naturally described by operations and equations.

## Key Technical Content

### Definition of Lawvere theory (Def 2.2)
A small category L with strictly associative finite products + a strict finite-product-preserving identity-on-objects functor I: ℵ₀ᵒᵖ → L.

### Model (Def 2.5)
A model of L in C is a finite-product-preserving functor M: L → C. Models form a category Mod(L, C) with natural transformations as morphisms.

### Semantic invariance (Prop 3.1)
L is determined up to isomorphism by Mod(L, Set) respecting the underlying set functor.

### Every Lawvere theory determines a finitary monad (Prop 4.2)
The construction L ↦ T_L is fully faithful. Finitary monads on Set correspond exactly to Lawvere theories (Theorem 4.4).

### Sum and tensor (Def 3.2, Theorem 3.4)
Sum L + L': combine operations, no new equations. Tensor L ⊗ L': combine with commutativity. Theorem: Mod(L ⊗ L', C) ≃ Mod(L, Mod(L', C)).

## Impact on our project

1. Confirms that our "explanation as functor" is a standard construction.
2. The distinction between Lawvere theories (equational) and the broader hierarchy (regular, coherent, geometric theories) is crucial for us — scientific theories need the broader setting.
3. The category of Lawvere theories Law has good properties (complete, cocomplete, locally finitely presentable) — relevant to our "category of explanations" idea.
4. The tensor product of theories might formalize "combining explanations."
