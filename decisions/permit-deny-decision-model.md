# Permit and Deny Decision Model

The gatekeeper produces deterministic enforcement outcomes.

## Decision Space

- `PERMIT`
- `DENY`

## Decision Rule

A request may be permitted only when:

- request structure is valid
- actor identity is valid
- nonce validation succeeds
- registry authority confirms admissibility

Otherwise the request must be denied.

## Fail-Closed Requirement

If the gatekeeper cannot verify governance readiness, it must deny execution.
