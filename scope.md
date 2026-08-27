# Scope — ShopEase AI Customer Support Assistant

## In scope

- Order tracking queries
- Cancellation information (policy/process, not execution)
- Refund information (policy/status explanation, not processing)
- Payment issue guidance
- Product issue reporting (damaged/wrong item intake)
- Basic account support (general how-to, non-sensitive)
- Escalation to human support

## Out of scope

- Actual refund processing
- Real payment transactions
- Real account access or changes
- Financial decisions
- Changing sensitive account information (password, email, payment methods)

## Assumptions

- ShopEase is a fictional company; all scenarios and data are synthetic.
- The AI has **no real database or order-system access** — it only has the information given to it in the conversation or system prompt.
- A human support team exists as the escalation path for anything outside AI scope.
- Testing is conducted using the free/consumer chat interfaces of ChatGPT, Claude, and Gemini (no API access required).
- Model behavior may change over time — every test result is tied to a specific model, version, and test date.

## AI boundaries

### The AI SHOULD

- Answer questions within its supported topics.
- Ask clarifying questions when a request is ambiguous or missing required information.
- Follow the policy/context explicitly provided to it.
- Clearly admit when information is unavailable rather than guessing.
- Escalate to human support when a request is complex, sensitive, or out of scope.

### The AI SHOULD NOT

- Invent data (order status, refund amounts, delivery dates, policy details) it wasn't given.
- Claim it has access to a live database or order system.
- Promise refunds, cancellations, or outcomes it cannot guarantee.
- Request unnecessary sensitive information (full card numbers, passwords, etc.).
- Make decisions that require human judgment or authority.
