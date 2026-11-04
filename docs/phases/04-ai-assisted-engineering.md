# Phase 4 — AI-assisted software engineering

## Purpose

Use AI as a bounded engineering aid while retaining human ownership of design, code, tests, security, and delivery. Optimize for verified outcomes rather than code volume or apparent speed.

## Outcomes

- A reviewed software change produced with documented AI assistance.
- A repeatable workflow for planning, implementation, testing, and review.
- Evidence of quality and productivity trade-offs, including failure or rework.

## Learning objectives

- Select tasks suitable for AI assistance and divide them into reviewable units.
- Supply a Phase 3 specification and context with explicit constraints.
- Inspect generated changes for correctness, maintainability, security, licensing, and fit.
- Run existing tests and relevant checks; add or update focused tests when warranted.
- Measure impact without treating correlation or a single task as general proof.

## Prerequisites

Phases 1–3; ordinary software development and test practices.

## Core competencies

AI-assisted coding, code comprehension, test design, review, safe tool use, and measurement.

## Concepts and terminology

Human-in-the-loop, code completion, agent mode, change decomposition, test oracle, regression, technical debt, and independent review. AI-generated code has no special presumption of correctness.

## Learning progression

- **Foundational:** use AI for explanation, test ideas, or a small isolated change; verify each result.
- **Intermediate:** deliver a bounded feature/refactor with explicit tests and human review.
- **Advanced:** define team workflows, appropriate gates, and a credible evaluation of impact and risk.

## Practical exercises

1. Ask an AI assistant to explain an unfamiliar module, then verify every material claim against source and tests.
2. Implement a small change from a reviewed specification; inspect the full diff and test failure paths.
3. Ask the assistant to critique the diff, then independently assess the critique and document false positives/misses.
4. Compare AI-assisted and baseline approaches on similar tasks with quality and rework measures.

## Implementation project

Deliver one small, authorized software change with a traceable specification, AI-use record, human-reviewed diff, test evidence, and risk notes. Suggested contexts include Product Catalog or Product Search, but these external projects are not provided here; verify access and actual stack before choosing. Do not modify unrelated repositories as part of this curriculum.

## Deliverables

- Specification and scoped implementation diff.
- Focused test and validation results.
- Review record covering AI contribution, human decisions, defects found, and security/privacy considerations.
- A cautious reflection on time, quality, and rework.

## Evaluation criteria

- Change meets acceptance criteria and relevant existing checks pass.
- Learner explains every material change and identifies generated content.
- Tests independently exercise behavior; output is not validated only by the generating model.
- Diff is appropriately scoped, and security, data handling, and license concerns are considered.
- Productivity conclusions are limited to observed evidence and disclose rework.

## Dependencies and next phase

Builds on Phases 1–3. Phase 5 extends assistance to bounded multi-step tool workflows; Phase 6 deepens governance and operating controls.

## Recommended resources

- [GitHub Copilot documentation](https://docs.github.com/en/copilot) — tool-specific guidance; verify current product behavior and policy.
- [Google Testing Blog](https://testing.googleblog.com/) — testing practice and test quality.
- [NIST Secure Software Development Framework](https://csrc.nist.gov/Projects/ssdf) — secure development practices.
