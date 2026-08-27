# Conversation Flows — ShopEase AI Customer Support Assistant

## Flow 1 — Happy path (order tracking with ID)

```mermaid
flowchart TD
A[Customer asks about order status] --> B{Order ID provided?}
B -- Yes --> C[AI acknowledges it cannot check live status]
C --> D[AI directs to order-tracking page / provides general guidance]
```

## Flow 2 — Missing information

```mermaid
flowchart TD
A[Customer asks: Where is my order?] --> B{Order ID provided?}
B -- No --> C[AI asks for order ID or identifying details]
C --> D[Customer provides ID]
D --> E[AI proceeds per Flow 1]
```

## Flow 3 — AI limitation (no database access)

```mermaid
flowchart TD
A[Customer expects a real-time status] --> B[AI has no live system access]
B --> C[AI explicitly states the limitation]
C --> D[AI redirects to tracking page or human support]
```

## Flow 4 — Ambiguous query

```mermaid
flowchart TD
A["Customer: My order is wrong"] --> B[AI asks clarifying question]
B --> C{What kind of issue?}
C --> D[Wrong item]
C --> E[Damaged item]
C --> F[Missing item]
C --> G[Quantity issue]
D & E & F & G --> H[AI collects order ID + details]
H --> I[AI provides next steps or escalates]
```

## Flow 5 — Escalation

```mermaid
flowchart TD
A[Customer raises complex/sensitive request] --> B{Within AI scope?}
B -- No --> C[AI states it cannot resolve this directly]
C --> D[AI explains reason for escalation]
D --> E[AI hands off to human support]
B -- Yes --> F[AI continues normal flow]
```
