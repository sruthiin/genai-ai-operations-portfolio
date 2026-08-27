# Stakeholders — ShopEase AI Customer Support Assistant

| Stakeholder | Role | Interest |
|---|---|---|
| Customer | Uses the AI assistant | Accurate, fast, honest support |
| Customer Support Team | Handles escalations | Receives correctly-triaged handoffs with context |
| Product Owner | Business ownership | Improved customer experience, lower cost to serve |
| Business Analyst (this role) | Requirements & evaluation | AI behaves as specified against defined requirements |
| AI/Engineering | Builds and maintains the assistant | Implementation is feasible and maintainable |
| QA / AI Quality | Tests the assistant | Reliability, reproducibility, defect visibility |
| Risk/Compliance | Sets guardrails | Safe, non-fabricated, privacy-respecting behavior |

## Stakeholder concerns

- **Customer** — Getting a wrong or invented answer (e.g., a fake delivery date) erodes trust immediately.
- **Customer Support Team** — Poor escalation means they inherit angry customers with no context, or get flooded with cases the AI could've handled.
- **Product Owner / Business** — Reputational risk if the AI gives confidently wrong answers publicly; ROI risk if escalation rate is too high to save any workload.
- **Risk/Compliance** — Privacy exposure (asking for unnecessary sensitive data) and safety exposure (making promises the company can't honor, e.g. "your refund is approved").
- **QA/AI Quality** — Non-deterministic model behavior makes "passing once" insufficient — needs repeatable test evidence across models and time.
