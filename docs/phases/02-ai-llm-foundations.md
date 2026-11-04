# Phase 2 — AI literacy, LLM fundamentals, and ChatGPT mastery

## Purpose

Develop an accurate mental model of generative AI and large language models (LLMs), then practice using conversational AI deliberately and safely. Provider-specific interfaces are examples; transferable reasoning and verification are the goal.

## Outcomes

- Explain how language-model generation works at a useful conceptual level and where it is unreliable.
- Design and document controlled model-use experiments.
- Select appropriate tasks, provide useful instructions, and independently verify outputs.

## Learning objectives

- Describe tokens, context windows, next-token generation, sampling, embeddings, retrieval, and model training/inference at an introductory level.
- Recognize hallucination, nondeterminism, stale knowledge, prompt sensitivity, and limits of benchmark results.
- Use ChatGPT or an equivalent assistant with clear goals, relevant context, constraints, and iterative refinement.
- Consider data, privacy, cost, latency, and human review before use.

## Prerequisites

Phase 1 baseline; basic ability to assess information sources.

## Core competencies

AI literacy, prompt design, controlled experimentation, output verification, model/task fit, and safe data handling.

## Concepts and terminology

LLM, tokenization, context window, inference, sampling temperature, embedding, retrieval-augmented generation (RAG), hallucination, grounding, fine-tuning, evaluation, and model drift. These terms describe distinct mechanisms; prompting alone does not guarantee factuality.

## Learning progression

- **Foundational:** explain core terms, uncertainty, and common limitations; use an assistant for low-risk bounded tasks.
- **Intermediate:** compare prompts or model settings with a fixed task set and human-rated criteria.
- **Advanced:** assess model selection and evaluation trade-offs, including privacy, latency, cost, and domain risk.

## Practical exercises

1. Ask a model the same bounded question in multiple ways. Save safe inputs/configuration, compare outputs, and check claims against primary sources.
2. Build a small set of representative questions and a rubric for correctness, completeness, and uncertainty.
3. Test an answerable and an unanswerable question; assess whether the model expresses uncertainty appropriately.
4. Practice ChatGPT for explanation, critique, summarization, and ideation. For each task, state what the model must not decide and how you verify it.
5. Compare model-assisted and unaided completion time and quality for a low-risk task; report the actual measurement and limitations.

## Implementation project

Produce a reproducible model behavior study for one low-risk task. Include the question, task context, system/provider/model identifier where available, date, settings, scoring rubric, results, verification sources, and limitations. Do not use sensitive data.

## Deliverables

- Concept map or short explanation of LLM behavior and limitations.
- Experiment record with a small evaluation set and independently checked results.
- Safe-use checklist covering task selection, data, verification, and escalation.

## Evaluation criteria

- Correctly explains generation and distinguishes prompting, retrieval, and fine-tuning.
- Identifies uncertainty and checks factual claims using sources independent of the model.
- Experiment can be repeated and its scoring method is explicit.
- Conclusions do not overgeneralize from a small sample; privacy and cost are considered.

## Dependencies and next phase

Builds on Phase 1. Phase 3 applies these foundations to context selection and testable specifications.

## Recommended resources

- [OpenAI documentation](https://platform.openai.com/docs/) — primary documentation for OpenAI products; provider-specific.
- [Google Machine Learning: Large Language Models](https://developers.google.com/machine-learning/resources/intro-llms) — introductory concepts.
- [Stanford CS324: Large Language Models](https://stanford-cs324.github.io/winter2022/) — deeper technical course material.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) — risk-based AI lifecycle guidance.
