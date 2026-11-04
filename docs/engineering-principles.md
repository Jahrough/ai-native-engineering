# Engineering principles

These principles govern every phase, exercise, and proposed production design. They are decision criteria, not claims that a capability has already been implemented.

## Evidence before assertion

- Separate observed facts, assumptions, hypotheses, and recommendations.
- Cite primary sources for material claims; identify uncertainty and source dates where facts may change.
- Treat AI output as an unverified proposal. Check code, references, calculations, and conclusions against independent evidence.
- Record measurable outcomes and limitations. Do not invent experience, results, or project capabilities.

## Explicit intent and reproducibility

- Make goals, user needs, acceptance criteria, constraints, failure behavior, and ownership explicit before delegating work.
- Keep prompts, specifications, model/tool versions, relevant configuration, and evaluation inputs reproducible when practical and safe.
- Prefer small, reviewable changes and experiments with a stated hypothesis and a way to falsify it.
- Keep source and generated artifacts distinguishable; never present plans as completed behavior.

## Security, privacy, and human control

- Apply security and privacy by design, data minimization, least privilege, and defense in depth.
- Do not place secrets or sensitive data in prompts, logs, examples, or external services without explicit authorization and safeguards.
- Treat retrieved content, tool output, and user-provided documents as untrusted input. Validate boundaries and tool arguments.
- Require a human decision-maker for consequential or irreversible actions. Give agents narrowly scoped permissions, bounded execution, and a clear stop condition.
- Design for abuse, prompt injection, data exposure, supply-chain risk, and failure; assess impact before deployment.

## Quality and operations

- Evaluate the system for its actual task and users; do not rely on a single benchmark or a model's self-assessment.
- Use deterministic tests where applicable, plus representative evaluation sets for probabilistic behavior. Track regressions.
- Make reliability, latency, cost, privacy, safety, and usefulness explicit trade-offs.
- Instrument deployed systems for useful, privacy-conscious observability; define ownership, incident response, and rollback paths.
- Manage models and prompts as lifecycle dependencies: version, evaluate, monitor, and retire them deliberately.

## Vendor neutrality

Teach durable concepts and interfaces first. Discuss vendor-specific tools as examples, label their constraints, and avoid coupling a competency to one provider unless the learning objective requires it. Record provider, model, date, and configuration for experiments so results can be interpreted later.

## Decision check

Before accepting AI-assisted work or a design, ask:

1. Is the intended outcome and its success criterion explicit?
2. Is the evidence independently checked and reproducible enough for the risk?
3. Are data handling, permissions, failure modes, and human approval appropriate?
4. Are quality, operational, and cost trade-offs measured?
5. Is the document clear about what exists, what is proposed, and what remains unknown?

## Authoritative references

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST Secure Software Development Framework (SSDF)](https://csrc.nist.gov/Projects/ssdf)
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [Google SRE Book](https://sre.google/sre-book/table-of-contents/)
