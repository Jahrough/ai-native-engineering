# Phase 6 — AI engineering operations, security, and governance

## Purpose

Apply security, privacy, evaluation, observability, lifecycle, cost, and human-oversight controls to AI-enabled engineering workflows and systems. Controls should be proportionate to impact and continuously reassessed.

## Outcomes

- A risk assessment and threat model for a defined AI use case.
- An operational plan covering quality, reliability, privacy, incident response, and change management.
- Lifecycle and governance decisions that are traceable to evidence and ownership.

## Learning objectives

- Identify threats including prompt injection, data leakage, insecure tool use, supply-chain exposure, and harmful or unreliable outputs.
- Establish data classification, minimization, retention, access, and provider review requirements.
- Define evaluation gates, monitoring, incident handling, rollback, and model/prompt change control.
- Measure and manage quality, latency, availability, cost, and drift.
- Clarify human accountability and escalation for consequential decisions.

## Prerequisites

Phases 2–5; basic software security and production operations knowledge.

## Core competencies

Threat modeling, privacy engineering, governance, operational readiness, evaluation, observability, lifecycle management, and cost control.

## Concepts and terminology

AI risk management, data governance, threat model, model card, evaluation set, drift, observability, incident response, retention, supply chain, and human oversight. A policy document is not an effective control unless responsibilities and evidence are defined.

## Learning progression

- **Foundational:** identify data and threat boundaries; document owners and basic controls.
- **Intermediate:** produce an evaluation plan, runbook, and monitoring design for a bounded AI workflow.
- **Advanced:** design continuous assurance and incident learning across a changing model/system lifecycle.

## Practical exercises

1. Perform a data-flow inventory and threat model for an assistant or proposed AI feature.
2. Design a privacy-conscious logging schema that supports debugging without retaining unnecessary prompt or user data.
3. Define release gates using task quality, safety, latency, availability, and cost; test a regression scenario.
4. Write an incident exercise for data exposure, model behavior regression, provider outage, or a compromised tool.
5. Review the lifecycle impact of changing model, prompt, retrieval index, tool, or policy.

## Implementation project

Create an operational readiness package for a hypothetical or authorized low-risk AI capability. Clearly label unimplemented controls and assumptions. Do not deploy or connect to a real service unless authorized and separately approved.

## Deliverables

- Data-flow diagram, risk register, and threat model.
- Evaluation and release plan with measurable thresholds and owners.
- Security/privacy controls and retention/access decisions.
- Monitoring, incident response, rollback, and lifecycle/change procedures.
- Cost and reliability assumptions with methods to validate them.

## Evaluation criteria

- Material risks have owners, mitigations, and explicit residual-risk decisions.
- Evaluation criteria represent intended users and meaningful failure modes.
- Monitoring supports action while minimizing sensitive data.
- Model and prompt changes trigger suitable regression checks and review.
- Incident response, human escalation, rollback, and cost limits are actionable and tested or clearly marked as proposed.

## Dependencies and next phase

Integrates Phases 2–5 and reinforces controls across the curriculum. Phase 7 uses this package to design a production AI product.

## Recommended resources

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST Privacy Framework](https://www.nist.gov/privacy-framework)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [Google SRE Book](https://sre.google/sre-book/table-of-contents/)
- [NIST Secure Software Development Framework](https://csrc.nist.gov/Projects/ssdf)
