# Glossary

This document defines how terms are used in this project. When a term has both a standard mathematical meaning and a project-specific meaning, both are noted.

Update this whenever you introduce a new term or discover that you're using an existing term in a way that could be ambiguous. Semantic drift across sessions is a real danger — this glossary is the defense against it.

---

### Category

**Standard meaning:** A collection of objects and morphisms (arrows between objects) satisfying associativity and identity laws. **Project usage:** Standard. No modification.

### Morphism

**Standard meaning:** A structure-preserving map between objects in a category. **Project usage:** Standard. When we say an explanation "preserves structure," we mean there exists an appropriate morphism.

### Functor

**Standard meaning:** A map between categories that preserves the categorical structure (sends objects to objects, morphisms to morphisms, and respects composition and identity). **Project usage:** The central formal object of the project. We propose that an explanation _is_ a functor from theoretical structure to empirical structure.

### Faithful (functor)

**Standard meaning:** A functor F: C → D is faithful if for every pair of objects X, Y in C, the map F: Hom(X,Y) → Hom(FX,FY) is injective. **Project usage:** In our framework, faithfulness means the explanation does not conflate distinct theoretical relationships. It is one of the three conditions we propose for "good explanation." See C-001.

### Essentially Surjective (functor)

**Standard meaning:** A functor F: C → D is essentially surjective if every object in D is isomorphic to F(X) for some X in C. **Project usage:** In our framework, essential surjectivity means every phenomenon in the domain has a theoretical counterpart (up to isomorphism). Second condition for "good explanation." See C-001.

### Minimal (source category)

**Standard meaning:** No standard meaning in category theory. This is a project-specific term that needs formal definition. **Project usage:** Informally: the source category T has no unnecessary structure — nothing can be removed without losing faithfulness or surjectivity. **THIS TERM IS NOT YET FORMALLY DEFINED.** Making it precise is a core open problem. See C-003. **Candidate formalizations:** (a) Kolmogorov complexity of categorical presentation; (b) no non-trivial quotient categories preserving the functor; (c) initial object in a category of explanations. All untested.

### Good Explanation

**Standard meaning (Deutsch):** An account that is hard to vary while still explaining the phenomenon. Qualitative criterion. **Project usage:** Proposed formalization: a faithful, essentially surjective functor from a minimal source category. See C-001. **This identification is the core thesis, not an established result.**

### Hard to Vary

**Standard meaning (Deutsch):** The components of the explanation are tightly integrated such that changing any element destroys explanatory power. **Project usage:** Proposed formalization: rigidity of the explanatory functor under perturbation. See C-004. **Not yet formalized.**

### Universal Construction

**Standard meaning:** A construction characterized by a universal property — roughly, it is the unique (up to isomorphism) solution to a categorical constraint. Examples: products, limits, adjunctions, Kan extensions. **Project usage:** We conjecture that the mathematical structures recurring across physics are universal constructions in explanatory categories. See C-002.

### P (category)

**Project-specific term.** The target category in an explanatory functor. Objects are observable phenomena; morphisms are empirical relationships. **Not yet rigorously constructed for any specific theory.** This is a priority item.

### T (category)

**Project-specific term.** The source category in an explanatory functor. Objects are theoretical constructs; morphisms are logical or mathematical entailments. **Not yet rigorously constructed.** Same priority as P.

### Confidence Tiers

**Project-specific term.** A four-level tagging system for claims in the state document:

- VERIFIED: Machine-checked
- ARGUED: Complete informal proof
- CONJECTURED: Believed on partial evidence
- SPECULATIVE: Worth exploring, no strong evidence

---

### Terms To Define (Parking Lot)

These terms will likely need glossary entries as the project develops:

- Natural transformation (in project context)
- Adjunction (in project context)
- Representability
- Kan extension
- Topos
- Homotopy type / HoTT concepts
- Computational irreducibility (if Wolfram's work becomes relevant)
- Presentation (of a category)

---

_When adding entries, maintain alphabetical order within the main section. Date your additions in the commit message or session log._