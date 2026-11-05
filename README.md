# AI-Native Engineering

An evidence-based, practical development program for building the knowledge, technical skills, workflows, and architectural judgment to work as an AI-native software engineer. It covers both AI-assisted software development and the design and operation of production AI-powered products.

## What this repository is

This is a documentation-first learning framework, not an application, a certification, or a claim that its author has completed the curriculum. It describes a proposed progression, exercises, and ways to demonstrate competency. Record actual work and results in the [progress tracker](docs/progress.md); do not treat reading, tutorial completion, or AI-generated output as proof of skill.

The program is designed as an adjustable six-month progression. Pace it to your available time and starting point: advance when you can independently produce and explain the evidence, not merely when a calendar date arrives.

## Start here

1. Read the [engineering principles](docs/engineering-principles.md) and [documentation index](docs/README.md).
2. Use the [progression and prerequisite map](docs/progression.md) to choose a starting phase and sequence your work.
3. Review the [competency matrix](docs/competency-matrix.md) to understand the expected progression.
4. Work through the seven [phase guides](docs/phases/), recording evidence and review outcomes using the [progress framework](docs/progress.md) and [assessment framework](docs/evaluation.md).
5. Follow the [contribution and documentation standards](docs/contributing.md) when changing this knowledge base.

## The seven phases

| Phase | Focus | Guide |
|---|---|---|
| 1 | Baseline assessment and engineering audit | [01 — Baseline](docs/phases/01-baseline.md) |
| 2 | AI literacy, LLM fundamentals, and ChatGPT mastery | [02 — AI and LLM foundations](docs/phases/02-ai-llm-foundations.md) |
| 3 | Context and specification engineering | [03 — Context and specifications](docs/phases/03-context-specification.md) |
| 4 | AI-assisted software engineering | [04 — AI-assisted engineering](docs/phases/04-ai-assisted-engineering.md) |
| 5 | Agentic engineering and autonomous workflows | [05 — Agentic engineering](docs/phases/05-agentic-engineering.md) |
| 6 | AI engineering operations, security, and governance | [06 — Operations, security, and governance](docs/phases/06-operations-security-governance.md) |
| 7 | AI product engineering and production AI architecture | [07 — AI product engineering](docs/phases/07-ai-product-engineering.md) |

## Learning and evidence

Each phase guide defines its purpose, outcomes, objectives, prerequisites, competencies, concepts, exercises, implementation project, deliverables, evaluation criteria, dependencies, and learning resources. Work moves from foundational through intermediate to advanced practice. Every phase requires practical evidence and independent verification; use the [assessment framework](docs/evaluation.md) to judge quality and readiness.

Engineering principles apply throughout: explicit requirements, reproducible work, security and privacy by design, least privilege, human approval for consequential changes, measured outcomes, and independent verification of AI outputs. See [engineering principles](docs/engineering-principles.md) and [cross-phase progression](docs/progression.md).

## Practice environments and scope

The curriculum may use these projects as learning environments where access is available:

- **Product Catalog:** Java 25, Spring Boot, PostgreSQL, Redis, Flyway, and transactional outbox.
- **Product Search:** Java, Spring Boot, Kafka, and OpenSearch.
- **Platform:** infrastructure and GitOps; platform observability.

These are contextual suggestions, not repositories included here. This curriculum does not modify or assume access to them, and it does not claim that any AI integration or capability is already implemented in them. Use a permitted codebase or a small, isolated exercise when access is unavailable.

## Cross-repository architecture governance

This repository also hosts canonical, evidence-based decision proposals for
related projects when their owners explicitly authorize that documentation.
These records govern architectural discussion only; they do not implement
capabilities in the external repositories, transfer ownership of their code,
or imply that a proposal has been accepted. See the [architecture decision
index](docs/architecture/adr/README.md) and [approval package](docs/architecture/approval/).

## Current status

The repository contains curriculum and guidance documents. Exercises, projects, assessments, and future capabilities are proposals until someone performs them and records verifiable evidence. Do not infer completion, experience, or measured outcomes from the presence of a guide.

## Contributing

Keep content modular, actionable, vendor-neutral where practical, and supported by authoritative resources. Avoid repeating phase-specific details in overview pages. See [contribution and documentation standards](docs/contributing.md).
