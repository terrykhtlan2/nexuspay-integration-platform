# ADR-002: API Versioning and Release Strategy

## Status
Proposed

## Context
The NexusPay API will evolve over time. We need a versioning strategy that allows backward compatibility while enabling innovation.

## Decision
We will use:
- **URI versioning** (e.g., /v1/payments) for major breaking changes
- **Semantic Versioning** for the API contract (major.minor.patch)
- **Release candidates** in test environments before production
- **GitHub Releases** tagged with version numbers

## Consequences
**Positive:**
- Clear version visibility in requests
- Multiple versions can coexist
- Clients control their upgrade timeline

**Negative:**
- Need to maintain multiple versions
- URI structure becomes less clean
