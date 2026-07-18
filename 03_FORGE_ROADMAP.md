# Forge Roadmap

**Status:** Reconciled v1.1 — resolves the Milestone 0 / Milestone 11 dashboard-scope conflict present in earlier drafts.

Each milestone must satisfy DEFINITION_OF_DONE.md before the next may begin (per Constitution Article VIII and Law 10 / Law 9).

---

## Milestone 0 — Forge Control Center (Minimal)

**Goal:** Ship the smallest dashboard that gives real visibility into building Forge itself.

**Scope — exactly 4 modules, nothing more:**
1. **Milestone Timeline** — which milestones exist, current status, percent complete.
2. **Task Board** — simple Kanban: Backlog → In Progress → Review → Done.
3. **Decisions (ADR) List** — a plain list of ADRs with ID, date, status, one-line reason.
4. **Status Summary** — current milestone, blockers, next objective.

**Explicitly deferred to Milestone 11** (do not build now): Executive Dashboard analytics, Research Center, Architecture Center / interactive diagrams, File Explorer, Research Database (per-tool pages), Progress Analytics/charts, Risk tracker, Activity Timeline, "Chief Architect" summary panel. These either need data that doesn't exist until later milestones, or are non-load-bearing polish.

**Acceptance criteria:** see DEFINITION_OF_DONE.md.

---

## Milestone 1 — Forge Core

**Goal:** Build the foundation.

**Deliverables:** Installer, environment validation, project initialization, git integration, configuration, logging, diagnostics, module loader. `forge doctor` should exist and report real system state.

---

## Milestone 2 — Forge Brain

**Goal:** Persistent project intelligence. No AI yet.

**Deliverables:** Knowledge repository (file-based, per Article V), decisions store, architecture docs, standards, roadmap, memory, documentation.

**Write mechanism:** governed by ADR-001 — you are the sole approver until Milestone 4.

---

## Milestone 3 — Forge CLI

**Goal:** Professional command interface.

**Commands:** `forge`, `forge doctor`, `forge init`, `forge status`, `forge config`, `forge update`, `forge memory`, `forge research`, `forge task`, `forge workflow`, `forge agent`.

At this point Forge already becomes useful standalone.

---

## Milestone 4 — First Coding Agent

**Goal:** AI arrives. Capabilities: read, plan, modify, explain, review. No automation. Human approval required for every change.

Brain write-access mechanism evolves per ADR-001: agents may propose Brain updates, but a human commit is still required to merge.

---

## Milestone 5 — Multi-Agent

**Goal:** Planner, Architect, Builder, Reviewer, Tester, Documentation Specialist roles operate as a coordinated team (per Article VII).

---

## Milestone 6 — Routing Engine

**Goal:** Model routing, provider routing, capability routing, fallback (local ↔ cloud) — implements Article XI's swappable-interface requirement in practice.

---

## Milestone 7 — MCP Integration

**Goal:** Filesystem, Git, Docker, Browser, PowerShell, databases, search — Forge interacts with the outside world.

---

## Milestone 8 — Workflow Engine

**Goal:** Every task follows: Planning → Coding → Testing → Review → Documentation → Approval → Commit.

---

## Milestone 9 — Project Intelligence

**Goal:** Impact analysis, dependency graph, architecture validation, duplicate detection, technical debt tracking, pattern detection, risk analysis.

---

## Milestone 10 — Automation

**Goal:** Auto review, auto documentation, auto testing, auto changelog, auto release notes, auto migration.

---

## Milestone 11 — Engineering Dashboard (Full)

**Goal:** Completes the original full dashboard vision deferred from Milestone 0 — Executive Dashboard, Research Center, Architecture Center, File Explorer, Research Database, Progress Analytics, Risks, Activity Timeline, Chief Architect panel — now backed by real data from Milestones 1–10. Synchronized across CLI, Web, and IDE.

---

## Milestone 12 — Forge Platform

**Goal:** Plugins, profiles, extensions, marketplace, custom agents, enterprise deployment. Finished vision.

---

## Development Rule

No milestone may begin until the previous milestone is complete, documented, tested, released, and stable, per DEFINITION_OF_DONE.md. No milestone exists merely to support a future milestone (Constitution Article VIII).
