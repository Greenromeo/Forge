# ADR-001: Brain Write Access

**Status:** Accepted
**Date:** 17 July 2026

## Context

Constitution Article V states the Brain is read-only and that "only approved information enters the Brain," but no approver or approval mechanism was ever defined. This is a real problem because Milestone 2 (Forge Brain) is built and populated *before* any coding agent exists (Milestone 4) — meaning there is no AI in the loop yet to even propose changes, let alone need gating.

## Decision

**Phase 1 (Milestones 2–3, no AI yet):**
You are the sole approver. All Brain content (`architecture.md`, `decisions.md`, `standards.md`, etc.) is written or edited directly by you via git commit. No automated write path exists. There is nothing to "approve" in the sense of a workflow — a human is the only writer.

**Phase 2 (Milestone 4 onward, coding agent exists):**
AI agents may *propose* Brain updates, structured as a diff or PR-style change — never a direct write. A human commit is still required to merge any proposed change into the Brain. The Brain never accepts direct, unreviewed writes from any agent, at any milestone.

## Consequences

- Milestone 2 is simpler to build: no approval workflow, permission system, or review UI needed yet.
- The actual approval-workflow engineering (diff proposal, review UI, merge gating) is deferred to Milestone 4+, when it's actually needed — consistent with Constitution Article VIII ("no milestone depends on unfinished future work").
- This decision may be revisited by a future ADR if the Brain's write model needs to change (e.g., multi-user scenarios, delegated approval).

## Alternatives Considered

- **Automated approval heuristics from Milestone 2 onward:** rejected — there's no agent to generate proposals yet, so this would be speculative engineering with no current use case.
- **No formal write restriction at all:** rejected — contradicts Article V and Law 1 (Human Authority); the Brain must never silently absorb AI-generated content without a human in the loop.
