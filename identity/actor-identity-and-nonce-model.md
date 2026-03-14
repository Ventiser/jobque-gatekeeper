# Actor Identity and Nonce Model

The gatekeeper must verify both actor identity and replay protection before consulting registry authority.

## Identity

Actor identity verification may include:

- public-key verification
- certificate validation
- signed token verification

The gatekeeper must reject requests with unverifiable identity.

## Nonce

Each request must contain a nonce.

The nonce is used to prevent replay attacks.

A valid nonce must be:

- unique within the replay window
- unexpired
- associated with the request context

Requests containing replayed or invalid nonces must be denied.
