# Test Strategy — ShopEase AI Customer Support Assistant

## Objective

Evaluate AI assistant behavior against the requirements defined in `02-requirements/requirements.md`, across three general-purpose LLMs, using an identical system prompt and identical test inputs.

## Models under test

| Model | Interface | Version/date to be recorded at test time |
|---|---|---|
| ChatGPT | chat.openai.com (free/plus tier) | record at test time |
| Claude | claude.ai | record at test time |
| Gemini | gemini.google.com | record at test time |

Model behavior changes over time with provider updates — every test run must record the exact model name/version and the test date. Without this, results are not reproducible or defensible.

## Test categories

1. **Functional** — does it correctly handle the core supported query types?
2. **Accuracy** — is the information given correct relative to the provided policy/context?
3. **Relevance** — does the response actually answer what was asked?
4. **Hallucination** — does it invent facts (status, dates, amounts) not given to it?
5. **Ambiguity handling** — does it ask for clarification instead of guessing?
6. **Safety** — does it avoid requesting sensitive data / avoid unsafe claims?
7. **Escalation** — does it correctly recognize and hand off out-of-scope or sensitive cases?
8. **Consistency** — does it give the same core answer to equivalent rephrased queries?

## Method

For every test case:

1. Open a fresh conversation with the model (no prior context bleeding in).
2. Paste the current system prompt version (V1, then later V2) as the first message / system instruction.
3. Paste the exact customer query from the test case.
4. Record the full, unedited model output.
5. Compare the output against the "Expected Behaviour" column.
6. Mark PASS / FAIL.
7. If FAIL, log a defect in `05-results/defect-log.xlsx` with severity and root cause.

## Controls to keep testing fair

- Same system prompt text, character-for-character, across all three models for a given round.
- Same query wording across all three models.
- New/fresh chat session per test case (no carryover context) unless the test is specifically about multi-turn behavior.
- Record date/time and model version for every test, since this is a moving target.

## Out of scope for this test strategy

- Load/performance testing.
- API-level testing (this is UI-based, consumer-interface testing only).
- Long-term consistency across weeks/months (single testing window only, noted as a limitation).
