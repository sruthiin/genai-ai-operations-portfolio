# User Stories — ShopEase AI Customer Support Assistant

---

**US-001 — Order tracking (happy path)**

As a customer,
I want to know my order status,
so that I can understand when my order is expected.

*Acceptance criteria:*
```
Given the customer provides a valid order ID,
When the AI has no real-time access to check it,
Then the AI should explain it cannot check live status and direct the customer to the order-tracking page or human support, without inventing a status.
```

---

**US-002 — Order tracking, missing order ID**

As a customer,
I want to ask about my order without knowing my exact order ID,
so that I can still get help.

*Acceptance criteria:*
```
Given the customer asks about order status without an order ID,
When the AI responds,
Then the AI should ask for the order ID (or another identifier) rather than guessing or inventing a status.
```

---

**US-003 — Cancellation policy**

As a customer,
I want to understand how to cancel my order,
so that I know if I'm still eligible and what to do.

*Acceptance criteria:*
```
Given the customer asks about cancelling an order,
When the AI responds,
Then it should explain the general cancellation process and conditions, and clarify it cannot execute the cancellation itself.
```

---

**US-004 — Refund status**

As a customer,
I want to know when my refund will arrive,
so that I can plan accordingly.

*Acceptance criteria:*
```
Given refund information is unavailable to the AI,
When a customer asks about refund status,
Then the AI should not invent a refund amount or date, and should explain the typical timeline and how to check actual status.
```

---

**US-005 — Damaged item**

As a customer,
I want to report a damaged item,
so that I can get it replaced or refunded.

*Acceptance criteria:*
```
Given a customer reports a damaged item,
When the AI responds,
Then it should collect order ID, description, and (if applicable) request a photo, then explain next steps or escalate — without promising a specific resolution.
```

---

**US-006 — Wrong item received**

As a customer,
I want to report that I received the wrong item,
so that I can get the correct one.

*Acceptance criteria:*
```
Given a customer says "I got the wrong item",
When the AI responds,
Then it should ask clarifying questions (what was ordered vs. received) before proceeding.
```

---

**US-007 — Payment failure**

As a customer,
I want help when my payment fails or I'm double-charged,
so that I can resolve the issue.

*Acceptance criteria:*
```
Given a customer reports a payment issue,
When the AI responds,
Then it should acknowledge the issue, avoid asking for full card details, and either give general guidance or escalate to human support for investigation.
```

---

**US-008 — Ambiguous query**

As a customer,
I want to describe my problem in my own words,
so that I don't need to know the "correct" category.

*Acceptance criteria:*
```
Given the customer's message is ambiguous (e.g., "my order is wrong"),
When the AI responds,
Then it should ask a clarifying question (damaged? wrong item? missing item? quantity issue?) instead of assuming.
```

---

**US-009 — Unknown / out-of-scope query**

As a customer,
I want to ask something the AI wasn't designed to answer,
so that I still get pointed somewhere useful.

*Acceptance criteria:*
```
Given the customer's request is outside the AI's defined scope,
When the AI responds,
Then it should say so honestly and escalate to human support rather than guessing an answer.
```

---

**US-010 — Escalation for sensitive issue**

As a customer,
I want serious issues (fraud, security) handled by a real person,
so that I feel my concern is taken seriously.

*Acceptance criteria:*
```
Given a customer raises a fraud, security, or legal concern,
When the AI responds,
Then it should immediately escalate to human support and avoid attempting to resolve it directly.
```

---

**US-011 — Account update request**

As a customer,
I want to update my shipping address,
so that my order goes to the right place.

*Acceptance criteria:*
```
Given a customer asks to update account information,
When the AI responds,
Then it should explain how to do it (self-service steps) and clarify it cannot make the change directly.
```

---

**US-012 — Repeated query consistency**

As a customer,
I want the same answer if I ask the same question twice, differently worded,
so that I trust the information is accurate.

*Acceptance criteria:*
```
Given the same underlying question is asked with different phrasing,
When the AI responds both times,
Then the core policy information should be consistent.
```
