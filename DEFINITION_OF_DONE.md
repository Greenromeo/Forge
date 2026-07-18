# Forge — Definition of Done

**Status:** Ratified v1.0

This document operationalizes Constitution Article VIII (Milestone Philosophy) and Laws 5, 8, and 9. It applies to every milestone, and to every individual feature or task within a milestone.

## A milestone (or task) is Done when all six criteria below are satisfied:

### 1. Functional
Every deliverable listed for the milestone works end-to-end on the actual target environment (currently: Windows laptop, T500/4GB VRAM, WSL2 where applicable) — not just in a description or diagram.

### 2. Tested
- If the deliverable is code: automated tests exist and pass for its core behavior.
- If the deliverable is a process or workflow (not code): manual verification steps are written down, have been executed at least once, and passed.

### 3. Documented
A short document exists, written **before** the milestone is marked done, describing:
- What it does
- How to run/use it
- How to verify it still works

### 4. Git-Committed and Tagged
Work is committed to the repository and tagged (e.g. `milestone-0-v1`), per Law 4 — Git Is Truth. Nothing is "done" if it only exists in chat history or a local uncommitted state.

### 5. Explainable
You can state, in one paragraph, why this milestone/feature exists and which architecture document or ADR justifies its scope (Law 8).

### 6. No Open Blocking Questions
Nothing required for this milestone is marked "TBD," "to decide later," or dependent on an unresolved decision. Open questions that don't block current scope may exist, but must be logged (e.g. in an ADR or a tracked issue) — not silently ignored.

---

## If a milestone can't satisfy all six

**Cut scope until it can.** Do not extend the deadline or "keep the door open" for future completion — that recreates the unfinished-monster-project pattern this document exists to prevent (Constitution Article VIII, last sentence).

## Applying this to Milestone 0 specifically

Using the trimmed scope in ROADMAP.md (4 modules: Milestone Timeline, Task Board, ADR List, Status Summary), Milestone 0 is Done when:
- All 4 modules render real data from the repository (not mock/placeholder data).
- You've manually verified each module updates correctly after a real git commit.
- A short `MILESTONE_0_GUIDE.md` exists explaining how to run and use the dashboard.
- The code is committed and tagged `milestone-0-v1`.
- You can explain in one paragraph why these 4 modules (and not the other 9 originally proposed) were chosen — this document plus ROADMAP.md's deferral note already provides that reasoning.
- No decision about Milestone 0's scope remains open.
