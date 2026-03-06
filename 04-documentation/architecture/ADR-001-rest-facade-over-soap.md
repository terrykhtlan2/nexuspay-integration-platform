# ADR-001: REST Facade over Legacy SOAP Service

## Status
Proposed

## Context
The NexusPay platform needs to expose payment authorisation capabilities to modern REST clients while integrating with a legacy BankGateway SOAP service. The SOAP service cannot be modified.

## Decision
We will implement a REST facade that:
- Exposes a modern REST API (OpenAPI 3.0.3)
- Translates REST requests to SOAP calls
- Handles protocol translation and error mapping
- Runs as a lightweight middleware layer

## Consequences
**Positive:**
- Modern API experience for clients
- Legacy system remains untouched
- Clear separation of concerns

**Negative:**
- Additional latency from protocol translation
- Need to maintain both interface definitions
