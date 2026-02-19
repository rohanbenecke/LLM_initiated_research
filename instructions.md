# Instructions

You are resuming an ongoing research project. Read this document first, every session, before doing anything else.

## Repository

This project lives at: https://github.com/rohanbenecke/LLM_initiated_research.git

All work is committed to this repo between sessions by Rohan. Your workspace is a local clone of this repo.

## File Structure

```
/project-root
├── instructions.md          ← You are here. Read this first. Every session.
├── system_prompt.md         ← Your identity and operating principles. Read second.
├── state/
│   ├── current_state.md     ← The full research state. Read third.
│   ├── priority_queue.md    ← Ranked list of open problems. Read fourth.
│   ├── dead_ends.md         ← Failed approaches with post-mortems.
│   ├── definitions.md       ← All formal definitions, versioned.
│   ├── conjecture_register.md ← All conjectures with status tracking. The intellectual spine.
│   ├── conceptual_map.md    ← Dependency graph of research questions. Visual overview.
│   └── glossary.md          ← Term definitions. Prevents semantic drift between sessions.
├── questions_buffer.md      ← Async communication with Rohan. Drop questions here.
├── reading/
│   ├── reading_queue.md     ← What to read, what's been read, and what was learned.
│   ├── summaries/           ← Your summaries of source material (R-NNN.md).
│   └── sources/             ← PDFs and excerpts provided by Rohan.
├── log/
│   ├── session_NNN.md       ← One file per session. Read the latest 3.
│   └── ...
├── formal/
│   ├── lean/                ← Lean 4 formalizations.
│   └── latex/               ← LaTeX writeups of argued results.
└── output/
    └── drafts/              ← Anything approaching publishable form.
```

## Boot Sequence

Every session, in this order:

1. **Read this file** (you're doing this now).
2. **Read system_prompt.md.** Even if you think you know what it says. You don't persist. Read it.
3. **Read state/current_state.md.** This is the ground truth of where the research stands.
4. **Read state/priority_queue.md.** This tells you what the previous instance thought was most important.
5. **Read the latest 3 session logs** in log/. These give you recent context — what was tried, what worked, what didn't.
6. **Read state/dead_ends.md.** Before you start working, know what has already been tried and failed. Do not repeat dead ends.
7. **Read state/conjecture_register.md.** Know the status of every conjecture. This is the spine.
8. **Skim state/conceptual_map.md.** Orient yourself in the dependency structure. Know what's blocked and what's available.
9. **Check questions_buffer.md.** See if Rohan has answered any outstanding questions.
10. **Decide what to work on.** Usually the top item in the priority queue. If you have a reason to deviate, document it in your session log.
11. **Work.** See system_prompt.md for how to conduct the work.
12. **Close out the session.** See Closing Protocol below.

If any of these files don't exist yet (early sessions), skip them and note their absence in your session log.

## Closing Protocol

Before ending a session, you must complete all of the following:

### Update state/current_state.md

- Add any new results (tagged with confidence tier: VERIFIED / ARGUED / CONJECTURED / SPECULATIVE).
- Revise any claims whose status changed based on this session's work.
- Remove nothing without moving it to dead_ends.md first.

### Update state/priority_queue.md

- Re-rank based on what you learned this session.
- Add new open questions that emerged.
- Mark completed items as DONE with a pointer to where the result lives.

### Update state/definitions.md

- If you introduced, revised, or abandoned any formal definitions, record the change here.
- Version definitions (e.g., "Definition 3.1v2 — revised session 7 to require...").
- Never silently overwrite a definition. The history matters.

### Update state/dead_ends.md (if applicable)

- If you abandoned an approach this session, write the post-mortem here.

### Update state/conjecture_register.md (if applicable)

- If any conjecture changed status, update it.
- If you generated a new conjecture, add it with the next sequential number.
- Record lineage: what led to this conjecture?

### Update state/conceptual_map.md (if applicable)

- If the dependency structure changed — new questions, resolved dependencies, new tracks — update the graph.
- Update the "Last structural revision" header.

### Update state/glossary.md (if applicable)

- If you introduced a new term or discovered ambiguity in an existing one, add or revise the entry.

### Update reading/reading_queue.md (if applicable)

- If you read something, move it to Completed and write a summary in reading/summaries/.
- If you identified new reading needs, add them to the Queue.

### Drop questions in questions_buffer.md (if applicable)

- If you have questions for Rohan that aren't session-critical, log them here with priority and blocking status.

### Write log/session_NNN.md

Use this template:

```markdown
# Session [NNN]
**Date:** [date]
**Focus:** [what you worked on]
**Priority queue item:** [which item, or "deviated — see rationale"]

## What I attempted
[Describe the approach taken this session.]

## What worked
[Results, insights, connections discovered.]

## What didn't work
[Approaches that failed or stalled, and why.]

## Key decisions made
[Any choices about direction, definitions, or scope, with reasoning.]

## State changes
[List updates made to current_state.md, priority_queue.md, definitions.md, dead_ends.md]

## Recommendation for next session
[What the next instance should focus on and why.]

## Honest assessment
[One sentence: Did this session produce real progress, a useful dead end, or neither?]
```

### Notify Rohan

End the session with a brief summary for Rohan: what you did, what you found, and whether you need anything from him (a reference, a tool, feedback on a specific argument). Keep it to a short paragraph. He'll read the full log if he wants detail.

## Rules

- **Do not start working before completing the boot sequence.** Context is everything. You have no memory. The documents are your memory.
- **Do not modify instructions.md or system_prompt.md.** If you think they need revision, propose changes to Rohan in your session summary. He decides.
- **Do not create new top-level files or directories without documenting why** in your session log. The file structure should remain navigable.
- **If Rohan asks you to do something unrelated to this research, decline.** Point him to a general-purpose Claude instance. You have one job.
- **If the state documents are inconsistent or confusing, fix them before doing new work.** Maintenance is real work. A garbled state document will derail every future session.
- **If this is Session 1,** your job is to initialize all the state files from the scoping document and templates. See the "Session 1: Initialization" section below. Do not attempt research. Get the infrastructure right.
- **If this is Session 2+,** proceed with the normal boot sequence and work cycle.

## Session 1: Initialization

If this is the first session (no log/ directory exists, no state/ files exist), your job is setup, not research.

### Session 1 Tasks

1. Read instructions.md (this file) and system_prompt.md.
2. Read scoping_document.docx. This contains the initial research vision, proposed framework, and preliminary conjectures.
3. Create the full directory structure:
    
    ```
    mkdir -p state/ log/ reading/summaries/ reading/sources/ formal/lean/ formal/latex/ output/drafts/
    ```
    
4. Move template files from templates/ into their permanent locations:
    - templates/conceptual_map.md → state/conceptual_map.md
    - templates/conjecture_register.md → state/conjecture_register.md
    - templates/glossary.md → state/glossary.md
    - templates/reading_queue.md → reading/reading_queue.md
    - templates/questions_buffer.md → questions_buffer.md
5. Create state/current_state.md by extracting and organizing the substantive content from the scoping document. This is not a copy — it is a restructured version optimized for a fresh instance to read and understand the research state. Include: the core question, the proposed framework, the key definitions (with confidence tiers), and the current status of each component.
6. Create state/priority_queue.md with an initial ranked list of open problems, derived from the scoping document's "First Moves" section and your own assessment of what's most tractable and important.
7. Create state/dead_ends.md (empty template — nothing has failed yet).
8. Create state/definitions.md with all formal definitions from the scoping document, tagged with confidence tiers and version numbers.
9. Review all template files (conjecture register, glossary, conceptual map, reading queue) and adjust them if the scoping document suggests changes. The templates are a starting point, not final.
10. Write log/session_001.md documenting what you set up, any decisions you made about organization, and your recommendation for Session 2.
11. Notify Rohan with a summary of what was initialized and whether any source materials are needed immediately.

### Session 1 Success Criteria

- Every file in the directory structure exists and has content.
- A fresh instance reading only the state/ files and latest log could understand what this project is about and what to do next.
- No research was attempted. Session 1 is infrastructure.

---

Sessions are numbered sequentially starting from 001. Use zero-padded three-digit numbers (001, 002, ..., 999). If you are unsure what session number you are, count the files in log/ and add one.

---

_Last updated: February 2026. This document is maintained by Rohan. Suggest changes; do not make them directly._