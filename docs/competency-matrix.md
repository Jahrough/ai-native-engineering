# Competency matrix

Use this matrix to identify learning targets, not to self-award proficiency from exposure. The [evaluation framework](evaluation.md) defines acceptable evidence and review. A competency is demonstrated only when the learner can perform it in context, explain decisions, and independently verify the result.

| Competency area | Foundational | Intermediate | Advanced | Primary phases |
|---|---|---|---|---|
| Baseline and reflective practice | Identify skills, gaps, goals, and constraints | Reassess using evidence and update priorities | Mentor or design a repeatable evidence-based development loop | 1, all |
| AI and LLM literacy | Explain tokens, context, generation, uncertainty, and common limitations | Compare models and prompting strategies with a controlled evaluation | Select and justify model/system trade-offs against risk, quality, latency, and cost | 2, 4, 6, 7 |
| Context and specification engineering | State intent, constraints, context, and acceptance criteria | Build concise task-specific context and testable specifications | Design reusable context pipelines and assess context quality and risk | 3–5, 7 |
| AI-assisted software engineering | Use AI for bounded tasks and inspect output | Integrate changes with tests, review, security checks, and human ownership | Establish reliable team workflows and evaluate impact without weakening controls | 4, 6 |
| Agentic engineering | Explain tools, state, autonomy, and failure boundaries | Build a constrained, observable, approval-gated workflow | Architect and evaluate resilient multi-step systems with least privilege and recovery | 5–7 |
| Software architecture and data | Describe system boundaries and data flow | Design integrations, persistence, consistency, and failure handling | Evaluate end-to-end architecture and evolutionary trade-offs | 1, 3, 6–7 |
| Security, privacy, and governance | Identify sensitive data, threats, and access boundaries | Apply threat modeling, least privilege, retention, and review controls | Establish risk-based governance, assurance, response, and continuous oversight | 1–7 |
| Testing and evaluation | Verify deterministic behavior and recognize uncertainty | Build representative test/evaluation sets and regression checks | Validate evaluation validity, monitor drift, and make deployment decisions from evidence | 2, 4–7 |
| Operations and observability | Identify service health, errors, and ownership | Define useful metrics, traces, alerts, and incident procedures | Operate model-dependent services with lifecycle, rollback, and cost controls | 1, 5–7 |
| Product engineering | Identify users, tasks, and value hypotheses | Validate user needs and select an appropriate AI boundary | Deliver a production architecture with quality, risk, and lifecycle evidence | 3, 6–7 |

## Evidence examples

- A scored baseline and reassessment with a rationale for changed priorities.
- A reproducible model behavior experiment, including prompts, configuration, expected outcome, observations, and limitations.
- A specification and context package reviewed against acceptance criteria.
- A code change with tests, security considerations, human review, and independently observed behavior.
- An agent workflow with permission boundaries, logs/traces, adversarial or failure tests, and an approval/stop path.
- A threat model, operational runbook, evaluation report, or product architecture decision record.

Evidence must be attributable to actual work, dated where useful, and safe to share. Redact secrets and personal or customer data. A polished artifact alone is insufficient if the learner cannot explain and reproduce the decisions.
