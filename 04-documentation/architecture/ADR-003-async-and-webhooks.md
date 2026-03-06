# ADR-003: Asynchronous Patterns and Webhooks

## Status
Proposed

## Context
Payment operations may need asynchronous processing for long-running transactions or external confirmations.

## Decision
We will implement:
- **Webhooks** for event notifications (payment.succeeded, payment.failed)
- **Callback URLs** provided by clients per request
- **Idempotency keys** for retry safety
- **Dead letter queues** for failed webhook deliveries

## Consequences
**Positive:**
- Better scalability for long operations
- Real-time event notifications
- Decoupled architecture

**Negative:**
- More complex error handling
- Need webhook retry mechanisms
- Clients must expose endpoints
