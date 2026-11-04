# Learning progression and prerequisite map

## Progression model

The curriculum builds from self-knowledge to foundations, workflow design, assisted implementation, bounded autonomy, operational controls, and finally product architecture. Skills overlap: revisit earlier phases as system complexity and risk increase. The [competency matrix](competency-matrix.md) describes expected depth; the phase guides specify practice and evidence.

```text
1 Baseline and audit
        ↓
2 AI / LLM foundations
        ↓
3 Context and specifications
        ↓
4 AI-assisted engineering
        ↓
5 Agentic engineering ─────────┐
        ↓                       │
6 Operations, security,         │
  and governance ←──────────────┘
        ↓
7 Production AI product engineering
```

Phase 6 draws on phases 2–5 and applies throughout, not only after agents. Phase 7 integrates all prior phases. A learner with existing skills may test out of familiar material only by supplying equivalent evidence, not by skipping verification.

## Prerequisites and entry criteria

| Phase | Prerequisites | Ready to advance when… |
|---|---|---|
| 1. Baseline | None; willingness to reflect candidly | A baseline, risk-aware learning priorities, and a feasible practice environment are recorded. |
| 2. Foundations | Phase 1 baseline | You can explain core LLM behavior and limitations, and verify model claims using a controlled exercise. |
| 3. Context/specification | Phases 1–2; basic ability to read and describe software behavior | A bounded task has a testable specification, relevant context, exclusions, and acceptance criteria. |
| 4. AI-assisted engineering | Phases 1–3; ordinary software development and testing practice | You can deliver and review a small change, explain it, and independently validate behavior and risks. |
| 5. Agentic engineering | Phases 2–4; comfort with tools, permissions, and failure handling | A bounded agent workflow has explicit controls, observed traces, and tested stop/escalation behavior. |
| 6. Operations/security/governance | Phases 2–5; basic security and production operations knowledge | You can produce a risk-based operating plan with measurable evaluations, controls, monitoring, and response actions. |
| 7. AI product engineering | Phases 2–6; software architecture and data fundamentals | A product design has validated user value, a justified AI boundary, system architecture, evaluation, and lifecycle plan. |

## Adjustable six-month pacing

This is a planning aid, not a deadline or competency guarantee. A possible 24-week allocation is:

| Weeks | Focus |
|---|---|
| 1–2 | Phase 1 baseline, audit, and setup of a progress log |
| 3–5 | Phase 2 LLM fundamentals and controlled experiments |
| 6–8 | Phase 3 context and specification practice |
| 9–12 | Phase 4 AI-assisted software engineering |
| 13–15 | Phase 5 bounded agent workflows |
| 16–19 | Phase 6 security, governance, and operations |
| 20–24 | Phase 7 product architecture, evaluation, and capstone review |

Reallocate time based on evidence, available hours, and project access. Revisit phases when evaluation reveals gaps. Do not compress safety, testing, or independent review to meet a date.

## Cross-cutting threads

| Thread | Introduced | Applied and deepened |
|---|---|---|
| AI/LLM behavior and limits | 2 | 4–7 |
| Software architecture and explicit requirements | 1, 3 | 4–7 |
| Context and specification engineering | 3 | 4–7 |
| Data quality and lifecycle | 2 | 6–7 |
| Security, privacy, and human oversight | 1–2 | Every phase; deeper in 5–7 |
| Testing and evaluation | 1–2 | Every phase; operationalized in 4–7 |
| Observability and incident response | 1 | 5–7 |
| Cost and performance | 2 | 4–7 |
| Model lifecycle and reproducibility | 2 | 6–7 |

## Practice environment selection

Prefer an existing, authorized project with meaningful tests and review practices. The Product Catalog (Java 25, Spring Boot, PostgreSQL, Redis, Flyway, transactional outbox), Product Search (Java, Spring Boot, Kafka, OpenSearch), platform infrastructure/GitOps, and platform observability are suggested contexts only. Their repositories are not included here; access, state, and implemented capabilities must be verified by the learner. If unavailable, use a small local example and document its limited realism.
