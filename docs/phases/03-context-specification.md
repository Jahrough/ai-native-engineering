# Phase 3 — Context and specification engineering

## Purpose

Make engineering intent legible to people and AI systems. Learn to provide the minimum useful, trustworthy context and express requirements in a form that can be implemented and verified.

## Outcomes

- A bounded task specification with explicit requirements, constraints, exclusions, and acceptance criteria.
- A curated context package that improves task understanding without leaking unnecessary data.
- A reviewable plan for testing assumptions and resolving ambiguity.

## Learning objectives

- Separate goals, requirements, constraints, assumptions, and implementation choices.
- Break ambiguous work into small tasks with observable acceptance criteria.
- Select, organize, and validate context from source code, documentation, examples, and data.
- Identify stale, conflicting, irrelevant, or untrusted context.

## Prerequisites

Phases 1–2; basic ability to read and describe software behavior.

## Core competencies

Requirements analysis, specification writing, context curation, decomposition, traceability, and uncertainty management.

## Concepts and terminology

Context engineering, specification, acceptance criterion, functional/nonfunctional requirement, invariant, assumption, constraint, scope boundary, source of truth, and context window. Context quantity is not quality; relevance, provenance, freshness, and permission matter.

## Learning progression

- **Foundational:** write clear task intent, boundaries, and examples.
- **Intermediate:** connect requirements to tests and curate context for a bounded code change.
- **Advanced:** design reusable context structures and evaluate context sufficiency, staleness, and exposure risk.

## Practical exercises

1. Rewrite an ambiguous feature request into user outcome, scope, non-goals, constraints, and acceptance criteria.
2. Trace the relevant code and documentation for a task; list sources, freshness, ownership, and contradictions.
3. Give two reviewers or AI sessions different context packages and compare misunderstanding, omissions, and unnecessary information.
4. Convert acceptance criteria into test cases, including edge cases and failure behavior.

## Implementation project

Prepare a specification and context pack for a small change in an authorized project. If using a suggested environment, verify actual repository state and access first. Include only relevant, permitted excerpts; do not assume project behavior from the curriculum description.

## Deliverables

- Task specification with acceptance criteria and explicit non-goals.
- Context inventory with source, relevance, freshness, and sensitivity classification.
- Test/verification plan mapping acceptance criteria to evidence.

## Evaluation criteria

- Requirements are unambiguous enough to assess and do not prescribe unnecessary implementation details.
- Context sources are relevant, current, and authorized; conflicting information is surfaced.
- Criteria cover expected behavior, edge cases, and material failure modes.
- A reviewer can identify what is in and out of scope and how success will be verified.

## Dependencies and next phase

Builds on Phases 1–2. Phase 4 uses these artifacts to direct and review AI-assisted implementation.

## Recommended resources

- [NASA Systems Engineering Handbook](https://www.nasa.gov/reference/systems-engineering-handbook/) — requirements and systems engineering reference.
- [GitHub Docs: About GitHub Copilot](https://docs.github.com/en/copilot/about-github-copilot) — tool-specific context examples; product behavior may change.
- [OpenAI: Prompt engineering](https://platform.openai.com/docs/guides/prompt-engineering) — provider-specific prompting guidance.
