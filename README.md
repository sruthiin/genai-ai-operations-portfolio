# AI Customer Support Agent: Cross-LLM Testing & Evaluation

> **Disclaimer:** Independent portfolio project using a fictional e-commerce scenario (ShopEase) and synthetic test data. Not affiliated with any real company. Testing was conducted via the free/consumer interfaces of ChatGPT, Claude, and Gemini — no API access used.

## Overview

This project simulates building and evaluating a first-level AI customer support assistant for a fictional e-commerce company, ShopEase. Rather than just writing a prompt and assuming it works, the goal was to treat prompt design like a testable system: define requirements, design the agent, write a system prompt, test it across three different LLMs with identical inputs, find where it fails, fix it, and retest.

## Business Problem

See [`01-business/business-problem.md`](01-business/business-problem.md). Summary: ShopEase's human support team is overloaded with repetitive queries (order tracking, cancellations, refunds), causing slow response times and inconsistent answers.

## Project Objective

Evaluate whether an AI customer-support assistant can handle a defined set of customer queries reliably, and identify failures related to accuracy, hallucination, instruction-following, ambiguity, consistency, safety, and escalation — across three different LLMs using the same system prompt.

## Scope

In scope: order tracking, cancellation info, refund info, payment guidance, product issue intake, basic account support, escalation. Out of scope: any real transaction execution. Full detail: [`01-business/scope.md`](01-business/scope.md).

## Tools

- **ChatGPT**, **Claude**, **Gemini** — consumer chat interfaces, no API.
- **Excel** — test case tracking and defect logging.
- **Mermaid** — conversation flow diagrams (rendered natively in GitHub markdown).

## Approach

```
DEFINE → DESIGN → PROMPT → TEST → OBSERVE → EVALUATE → FIND FAILURE → IMPROVE → RETEST → DOCUMENT
```

1. Defined the business problem, requirements, and user stories.
2. Designed conversation flows and boundaries for the agent.
3. Wrote System Prompt V1 (see [`03-agent-design/system-prompt-v1.md`](03-agent-design/system-prompt-v1.md)).
4. Ran 26 test cases against ChatGPT, Claude, and Gemini using the identical prompt and inputs.
5. Logged every failure as a defect with severity.
6. Rewrote the prompt as V2 based on the actual defects found.
7. Retested the previously-failed cases against V2.
8. Compared model behavior and documented findings.

## Test Coverage

26 test cases across 7 categories: Functional, Ambiguous, Hallucination, Safety, Escalation, Edge cases, Consistency. Full list: [`04-testing/test-cases.xlsx`](04-testing/test-cases.xlsx).

## Evaluation Criteria

Each model response scored 1–5 (Poor → Excellent) on Accuracy, Relevance, Instruction-following, Hallucination control, Safety, and Escalation. Scoring criteria defined before scoring — see [`05-results/evaluation-results.md`](05-results/evaluation-results.md).

## Key Findings

*(To be completed after live testing — see `05-results/evaluation-results.md`.)*

## Model Comparison

*(To be completed after live testing — see `05-results/model-comparison.md`.)*

## Prompt Iteration

System Prompt V1 → V2 changes and rationale: [`06-prompt-iteration/before-after-analysis.md`](06-prompt-iteration/before-after-analysis.md).

## Recommendations

*(To be completed after evaluation — see final findings in `05-results/evaluation-results.md`.)*

## Repository Structure

```
01-ai-customer-support-agent/
├── README.md
├── 01-business/            business problem, stakeholders, scope
├── 02-requirements/        functional/AI/NFR/safety requirements, user stories
├── 03-agent-design/        conversation flows, system prompt v1
├── 04-testing/             test strategy, test cases, test data
├── 05-results/             defect log, evaluation results, model comparison
├── 06-prompt-iteration/    system prompt v2, before/after analysis
├── screenshots/            evidence from live testing
└── learning-notes.md
```

## Disclaimer

Fictional project using synthetic data. Not a production system. Results reflect a single testing window on specific model versions (recorded per test) and should not be generalized beyond this test's scope.
