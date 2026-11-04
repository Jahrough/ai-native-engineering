# Phase 5 — Agentic engineering and autonomous workflows

## Purpose

Design workflows in which models use tools or execute multiple steps, while constraining autonomy, permissions, side effects, and recovery. Autonomy is a risk decision, not a goal in itself.

## Outcomes

- A bounded agent workflow with defined task scope, tools, state, and stop conditions.
- A threat- and failure-aware permission and approval design.
- Evidence from normal, adversarial, and failure-path tests, plus observable execution traces.

## Learning objectives

- Distinguish a conversational model from a tool-using agent and a deterministic workflow.
- Identify where model judgment is useful and where deterministic checks or human decisions are required.
- Bound tool access, input/output, runtime, iteration, and side effects.
- Design approval, rollback, escalation, and safe termination behavior.
- Evaluate task success, tool use, policy compliance, cost, and failure recovery.

## Prerequisites

Phases 2–4; familiarity with tools, APIs, permissions, and ordinary failure handling.

## Core competencies

Workflow decomposition, tool design, least privilege, agent evaluation, observability, human oversight, and containment.

## Concepts and terminology

Agent, tool/function calling, orchestration, state, memory, planning, autonomy, guardrail, prompt injection, capability boundary, idempotency, and escalation. Multi-agent patterns add coordination and failure modes; they are not inherently more capable or reliable.

## Learning progression

- **Foundational:** map a simple workflow and identify deterministic versus model-mediated steps.
- **Intermediate:** implement a narrow, read-only or approval-gated workflow with explicit limits and traces.
- **Advanced:** test multi-step recovery, adversarial inputs, concurrency, and operational boundaries; justify whether autonomy is warranted.

## Practical exercises

1. Model a task as a sequence of steps; mark model decisions, deterministic checks, sensitive data, and side effects.
2. Threat-model untrusted instructions in retrieved content and tool outputs.
3. Test timeout, malformed tool arguments, permission denial, duplicate execution, and human rejection.
4. Compare an agent design with a deterministic workflow for safety, quality, cost, and complexity.

## Implementation project

Build or prototype a narrowly scoped, low-risk workflow using read-only tools or a human approval gate before side effects. Include clear stop conditions and safe test fixtures. Avoid real credentials, production systems, autonomous deployment, or consequential actions.

## Deliverables

- Workflow/sequence diagram and tool permission matrix.
- Threat model and failure/abuse test cases.
- Execution traces and evaluation report.
- Human approval, stop, and recovery behavior demonstrated in tests.

## Evaluation criteria

- Tool permissions are least-privilege and bounded by task.
- Untrusted content cannot silently expand scope or authorize consequential action.
- Tests show safe behavior on malformed output, denial, timeout, repeated calls, and rejection.
- Traces support debugging without unsafe sensitive-data logging.
- A human can stop or reject the workflow; autonomy is justified against a simpler alternative.

## Dependencies and next phase

Builds on Phases 2–4. Phase 6 turns workflow-level controls into lifecycle, governance, and operational practice; Phase 7 applies them in product architecture.

## Recommended resources

- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [Anthropic: Building effective agents](https://www.anthropic.com/research/building-effective-agents) — vendor-authored design guidance; compare against alternatives.
- [OpenAI Agents documentation](https://platform.openai.com/docs/guides/agents) — provider-specific tooling; concepts are not provider-neutral.
