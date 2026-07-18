# Forge Constitution

**Status:** Ratified (Founding Text) — v1.0
**Ratification Date:** 17 July 2026

## Preamble

Forge was not created to build software faster.

Forge was created to build software better.

The project recognizes that Artificial Intelligence is a powerful engineering tool, but it is not an engineer.

Engineering discipline, architecture, documentation, testing, traceability, and human judgment remain the foundations of professional software development.

Forge exists to combine those engineering principles with modern AI capabilities in a way that remains modular, transparent, vendor-independent, and sustainable.

Technologies will evolve. Models will improve. Companies will rise and disappear. APIs will change.

Forge shall be designed so that none of these changes require rebuilding its foundations.

The architecture shall outlive the tools.

---

## Article I — Mission

Forge Engineering OS exists to provide an engineering operating system that enables humans and AI to collaborate through structured, measurable, and repeatable engineering workflows.

Forge does not replace engineers. Forge amplifies engineers.

---

## Article II — Vision

To become the reference architecture for AI-assisted software engineering by combining:

- Engineering discipline
- Persistent project knowledge
- Intelligent orchestration
- Replaceable AI components
- Transparent workflows
- Human oversight

into a single coherent platform.

---

## Article III — Core Philosophy

1. Engineering comes before AI.
2. Architecture comes before implementation.
3. Knowledge comes before automation.
4. Correctness comes before speed.
5. Principles outlive technology.

---

## Article IV — The Laws of Forge

These laws are immutable unless superseded by an approved Architecture Decision Record (ADR).

**Note on scope:** This Constitution, including this Article and everything below it, constitutes the founding text and was ratified as a whole on 17 July 2026. It did not itself require an ADR to be adopted. From this date forward, any addition, removal, or modification to these Laws — including principles proposed as mere "aspirations" — requires a formal ADR. This closes a gap in earlier drafts where a new principle was appended after the freeze without one.

### Law 1 — Human Authority
The human engineer is always the final decision maker. AI may recommend, analyze, and implement. AI shall never become the ultimate authority.

### Law 2 — Vendor Independence
No vendor shall become indispensable. Every external dependency must be replaceable.

### Law 3 — Model Agnosticism
Forge shall depend on capabilities, not model names. Models are implementations. Capabilities are architecture.

### Law 4 — Git Is Truth
The repository is the authoritative source of project state. Chats are temporary. Memory is supplemental. Git is permanent.

### Law 5 — Documentation Is Code
Documentation is a deliverable, not an afterthought. A feature is incomplete until its documentation is complete.

### Law 6 — Context Before Generation
AI must understand the project before changing the project.

### Law 7 — Architecture Before Code
No implementation shall precede architectural understanding.

### Law 8 — Every Change Must Be Explainable
Every modification shall answer: Why is this necessary? What architecture supports it? What requirements justify it? What risks exist? How is it validated?

### Law 9 — Every Feature Is Testable
Untested functionality is incomplete functionality.

### Law 10 — Engineering Over Novelty
Forge adopts technology because it improves engineering — not because it is fashionable.

### Law 11 — Make the Right Way the Easiest Way
If an engineer follows Forge's workflow, they should naturally produce better documentation, cleaner architecture, stronger testing, and more maintainable software — not because they're forced to, but because the platform guides them there. This does not replace the other Laws; it explains their purpose.

---

## Article V — The Brain

The Brain is the permanent memory of Forge. It contains: Architecture, Decisions, Standards, Knowledge, Roadmaps, Documentation.

The Brain does not execute work. It preserves understanding.

**Write access:** See ADR-001 (Brain Write Access) for the concrete mechanism governing how information enters the Brain, and who is authorized to approve it at each stage of the project.

---

## Article VI — The Orchestrator

The Orchestrator coordinates engineering workflows. It assigns work, selects agents, routes models, and validates outcomes.

The Orchestrator never becomes the source of truth.

---

## Article VII — AI Agents

Every agent shall have a clearly defined responsibility. Examples include:

- Planner
- Architect
- Builder
- Reviewer
- Security Reviewer
- Tester
- Documentation Specialist
- Release Manager

Agents collaborate through structured workflows. No single agent owns the entire engineering process.

---

## Article VIII — Milestone Philosophy

Forge shall evolve through independently valuable milestones. Every milestone must be: Useful, Stable, Tested, Documented, Releasable.

Forge shall never depend on unfinished future work to justify current complexity.

**Definition of Done:** See DEFINITION_OF_DONE.md for the concrete, checkable criteria that operationalize this Article.

---

## Article IX — Dashboard First

Before Forge builds software, Forge builds visibility. The dashboard is not a convenience. It is the Engineering Control Center. If progress cannot be measured, it cannot be managed.

**Scope note:** The dashboard is delivered incrementally. Milestone 0 delivers a minimal, load-bearing subset (see ROADMAP.md). The full dashboard vision is completed at Milestone 11, once there is real project data to visualize. Building the full vision before that data exists would violate Article VIII (no milestone depends on unfinished future work).

---

## Article X — Message to Future Architects

If you are reading this years after Forge began, remember this:

You are not maintaining an AI tool. You are maintaining an engineering system.

Resist the temptation to chase every new model, framework, or trend. Replace technologies when they genuinely improve the system. Do not replace principles because technology has changed.

Forge was designed to survive technological change through stable architecture.

If you must break a principle, document why. Leave the project stronger than you found it.

---

## Article XI — Resource Policy

Forge operates on a **$0/month recurring budget**.

- Local compute and one-time hardware costs are acceptable.
- Recurring subscriptions and paid APIs are **not** acceptable under the default policy.
- Local inference is used where hardware permits; hosted free-tier APIs are used for tasks exceeding local hardware capacity.
- All model access — local or hosted — goes through a swappable, provider-agnostic interface (OpenAI-compatible request format), never a vendor-specific SDK, per Law 2 and Law 3.

**Current hardware baseline:** Lenovo ThinkPad T500, Intel Core i7 11th Gen, 16GB RAM, NVIDIA T500 (4GB VRAM), Windows. This limits reliable local inference to quantized models in the ~3B–7B range (GGUF, Q4_K_M or similar), run via llama.cpp or Ollama, ideally inside WSL2.

**Current initial hosted stack** (non-binding implementation detail, re-verify periodically as free tiers change):
- Primary: Google AI Studio (Gemini) — large context window, no credit card required.
- Secondary / fast-lane: Groq — low-latency inference for interactive agent loops.

This baseline may be revisited by ADR if hardware or budget changes.

---

## Final Declaration

From this moment forward:

- The Constitution becomes the highest-level document in the repository.
- All future engineering work must align with it.
- Changes to the Constitution require formal architectural review through an ADR.
- Technologies may evolve; the Constitution exists to preserve the project's identity and engineering standards.
