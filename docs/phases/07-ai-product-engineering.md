# Phase 7 — AI product engineering and production AI architecture

## Purpose

Design an AI-powered product around validated user needs, choosing an AI approach only where it improves outcomes. Integrate software architecture, data, evaluation, security, operations, and human oversight into an evidence-based product proposal.

## Outcomes

- A validated problem statement and product hypothesis with measurable success criteria.
- A production-oriented architecture with an explicit AI boundary and non-AI fallback.
- A lifecycle plan for data, models, evaluation, safety, operations, and cost.

## Learning objectives

- Discover user needs and decide whether AI is appropriate for the task.
- Compare prompting, retrieval, fine-tuning, conventional software, and human workflows at a conceptual trade-off level.
- Design data flows, system boundaries, failure behavior, interfaces, and governance.
- Define offline and production evaluations, rollout strategy, monitoring, and ongoing ownership.
- Communicate assumptions, residual risks, and evidence gaps.

## Prerequisites

Phases 2–6; software architecture and data fundamentals. Phase 1 baseline and Phase 3 specification skills remain relevant.

## Core competencies

Product discovery, AI solution selection, system architecture, data engineering, evaluation design, security, operations, and decision communication.

## Concepts and terminology

AI product fit, human-centered design, RAG, inference boundary, offline/online evaluation, fallback, model lifecycle, data lineage, service-level objective, rollout, and build/buy trade-off. A prototype demonstrates feasibility only within its tested conditions; it does not establish production readiness.

## Learning progression

- **Foundational:** define a user problem and compare an AI option with a simpler baseline.
- **Intermediate:** design a bounded feature with data flow, evaluation, failure handling, and operational ownership.
- **Advanced:** create an end-to-end architecture and rollout proposal with assurance, economics, governance, and lifecycle evidence.

## Practical exercises

1. Interview or use authorized research to identify user tasks and harms; record what evidence supports the need.
2. Compare AI and non-AI approaches using quality, safety, privacy, latency, cost, and maintainability.
3. Design an architecture and trace a request through model, data, tools, persistence, monitoring, and fallback.
4. Create an evaluation plan covering representative cases, edge cases, regressions, and human review.
5. Define phased rollout, kill switch, ownership, incident handling, and model/prompt retirement.

## Implementation project

Produce a product architecture proposal and, if safe and feasible, a small non-production proof of concept. Suggested contexts include product catalog enrichment/search or platform observability, but actual repositories and capabilities are not included or assumed here. Keep prototype results separate from production claims.

## Deliverables

- User/problem statement, evidence, success metrics, and non-AI baseline.
- Architecture/data-flow diagrams and decision record for AI approach.
- Evaluation, threat, privacy, and human-oversight plan.
- Operational, cost, rollout, fallback, and lifecycle plan.
- Prototype evidence and explicit limitations if a prototype is built.

## Evaluation criteria

- User problem and expected value are supported by evidence, not model novelty.
- AI approach is compared with simpler alternatives and has a justified boundary.
- Architecture addresses data quality, privacy, security, failures, monitoring, and human responsibility.
- Evaluation represents real usage and is independent of model self-assessment.
- Rollout and lifecycle controls are actionable; unimplemented capabilities and assumptions are labeled.
- Cost and quality trade-offs are measurable and have an owner/review cadence.

## Dependencies and next phase

Integrates Phases 1–6. This is the capstone phase, not proof of mastery by completion alone. Use program-level review in the [evaluation framework](../evaluation.md), reassess against the [competency matrix](../competency-matrix.md), and continue iterating.

## Recommended resources

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [Google Cloud Architecture Framework](https://cloud.google.com/architecture/framework) — architecture principles; cloud-provider perspective.
- [Martin Fowler: Data Mesh principles](https://martinfowler.com/articles/data-mesh-principles.html) — data architecture perspective.
- [Google SRE Book](https://sre.google/sre-book/table-of-contents/)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
