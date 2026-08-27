# Synthetic Test Data — ShopEase AI Customer Support Assistant

All data below is fictional and created only for this testing exercise. No real customers, orders, or transactions exist.

## Sample orders

| Order ID | Item | Status (internal, not given to AI unless test requires it) | Order Date |
|---|---|---|---|
| SE-10234 | Wireless Earbuds | Shipped | 2026-08-10 |
| SE-10298 | Running Shoes (Size 9) | Processing | 2026-08-18 |
| SE-10310 | Blender | Delivered | 2026-08-05 |
| SE-10355 | Phone Case | Cancelled | 2026-08-12 |

## Sample customers

| Customer | Email (fake) | Notes |
|---|---|---|
| Arjun R. | arjun.r@example-mail.com | Asking about order SE-10234 |
| Priya K. | priya.k@example-mail.com | Received wrong item (SE-10298) |
| Meera S. | meera.s@example-mail.com | Wants refund on SE-10310 |
| Dev N. | dev.n@example-mail.com | Payment charged twice for SE-10355 |

## Policy snippets (given to AI only where a test calls for provided context)

- **Cancellation:** Orders can be cancelled free of charge within 2 hours of placing the order, or before the order ships, whichever is earlier.
- **Refunds:** Approved refunds are processed within 5–7 business days after the returned item is received and inspected.
- **Damaged/wrong item:** Customer must provide order ID and a photo; replacement or refund is offered after review.
- **Payment issues:** Duplicate charges are investigated by the payments team within 3 business days; the AI cannot resolve these directly.

## Usage note

Some test cases intentionally give the AI **no context** (to test hallucination behavior), and some give it **partial or full context** (to test accuracy/instruction-following). This is indicated per test case in `test-cases.xlsx`.
