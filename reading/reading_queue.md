# Reading Queue

Tracks what needs to be read, what has been read, and what was learned.

## Queue (Unread)

Priority: HIGH / MEDIUM / LOW Status: AVAILABLE (in reading/sources/) or NEEDED (Rohan should provide)

|#|Text|Specific Sections|Priority|Status|Why Needed|
|---|---|---|---|---|---|
|R-001|Mac Lane — _Categories for the Working Mathematician_|Ch. 1–5 (Categories, Functors, Natural Transformations, Universal Properties, Limits)|HIGH|NEEDED|Core mathematical toolkit. Cannot define framework without this.|
|R-002|Awodey — _Category Theory_|Ch. 1–4, Ch. 8 (Functors, Limits, Adjoints)|HIGH|NEEDED|More accessible complement to Mac Lane. Good for building intuition.|
|R-003|Leinster — _Basic Category Theory_|Full book (it's short)|MEDIUM|NEEDED|Third perspective. Leinster is known for clarity.|
|R-004|Deutsch — _The Beginning of Infinity_|Ch. 1–2 (Reach of Explanations, Closer to Reality)|HIGH|NEEDED|Primary source for the qualitative theory we're formalizing.|
|R-005|The HoTT Book|Ch. 1–3 (Type Theory, Homotopy, Sets and Logic)|MEDIUM|NEEDED|Relevant to C-004 (hardness as rigidity). Not urgent until foundations are set.|
|R-006|Wigner — "The Unreasonable Effectiveness of Mathematics in the Natural Sciences"|Full paper|HIGH|NEEDED|Primary source for the puzzle we're trying to resolve. Short paper.|
|R-007|Baez & Dolan — "From Finite Sets to Feynman Diagrams"|Full paper|MEDIUM|NEEDED|Example of category-theoretic structure appearing across physics. Relevant to C-002.|
|R-008|Li & Vitányi — _An Introduction to Kolmogorov Complexity_|Ch. 1–2|LOW|NEEDED|Relevant to C-003 (minimality-complexity conjecture). Not urgent.|
|R-009|Lawvere — _Functorial Semantics of Algebraic Theories_ (thesis, 1963)|Author's comments + Ch. II overview (partial read)|HIGH|AVAILABLE|Session 002 identified functorial semantics as the existing framework closest to ours. Partial read completed — need to finish formal details in Ch. II-III.|
|R-010|Makkai & Reyes — _First Order Categorical Logic_|Ch. 1–3 (Syntactic categories, models, completeness)|HIGH|NEEDED|The syntactic category construction is central to our framework. Need the precise definitions and theorems.|
|R-011|Johnstone — _Sketches of an Elephant_ (Vol. 1)|Part D (Categorical logic sections)|MEDIUM|NEEDED|Comprehensive modern treatment of categorical logic. Reference for syntactic categories and their properties.|

## Completed Readings

|#|Text|Session Read|Summary Location|Key Takeaway|
|---|---|---|---|---|
|R-009|Lawvere — _Functorial Semantics of Algebraic Theories_|Session 002 (partial)|reading/summaries/R-009.md|Our framework is an instance of functorial semantics. Lawvere theories too narrow for scientific theories — need broader categorical logic.|
|R-010p|Hyland & Power — _Lawvere Theories and Monads_|Session 002 (full)|reading/summaries/R-010-partial.md|Historical context. Confirmed framework is standard. Identified doctrinal hierarchy as key: equational → regular → coherent → geometric.|

## Notes

- When you read something, move it from Queue to Completed and write a summary in reading/summaries/R-NNN.md.
- Summaries should focus on what's relevant to this project, not general content. Answer: "What from this text changes or informs our framework?"
- If a text turns out to be irrelevant, say so in the summary. Don't force connections.
- Rohan: when you add a source to reading/sources/, update the Status column here.

---

_Additions to the queue can be made by either the agent or Rohan. Use the next R-number sequentially._