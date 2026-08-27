# Business Problem — ShopEase AI Customer Support Assistant

## Company context

**ShopEase** is a fictional e-commerce company. Customers browse products, place orders, make payments, track orders, cancel orders, request refunds, and report damaged or incorrect products.

## Current situation

All first-level customer support at ShopEase is handled manually by human agents through chat and email.

## Problems

- **High volume** — support receives a large number of queries daily, most of them repetitive.
- **Repetitive questions** — order status, cancellation policy, refund timelines, and payment issues account for the majority of tickets.
- **Response delays** — customers wait hours (sometimes longer) for a first reply during peak periods.
- **Inconsistent answers** — different agents phrase policy information differently, occasionally giving conflicting answers.
- **Human workload** — agents spend most of their time on low-complexity, repetitive queries instead of complex or sensitive cases.
- **Complex issues needing escalation** — fraud concerns, payment disputes, and account issues require human judgment and are currently mixed in with simple queries, slowing triage.

## Business impact

- Customer frustration from slow first response times.
- Increased operational cost from staffing for repetitive query volume.
- Longer wait times reduce customer satisfaction and retention.
- Inconsistent policy communication creates compliance and trust risk.

## Proposed solution

Introduce an AI-powered customer support assistant to handle **first-level support** for common, well-defined queries (order tracking, cancellation info, refund info, payment guidance, product issue intake, basic account support), while reliably escalating anything complex, sensitive, or outside its defined scope to a human agent.

This project evaluates whether such an assistant — built as a system prompt on top of general-purpose LLMs — can do this reliably enough to be useful, and identifies where it fails.

## Business objectives

1. Reduce first-response time for common, repetitive queries.
2. Handle high-volume repetitive queries (tracking, cancellation, refund status) without human involvement.
3. Improve consistency of policy communication across all customer interactions.
4. Correctly identify and escalate complex or sensitive issues to human agents.
5. Reduce routine workload on the human support team so they can focus on higher-value cases.

## Project objective

Evaluate whether an AI customer-support assistant — built via a system prompt and tested across ChatGPT, Claude, and Gemini — can handle a defined set of customer queries reliably, and identify failures related to **accuracy, hallucination, instruction-following, ambiguity handling, consistency, safety, and escalation**.

This is a testing/evaluation project, not a production build. The output is evidence of AI behavior under test, not a deployed system.
