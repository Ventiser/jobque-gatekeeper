# JobQue Gatekeeper
Reference Runtime Enforcement Implementation

![JobQue Gatekeeper Version](https://img.shields.io/badge/JobQue--Gatekeeper-v1.0--draft-blue)

JobQue Gatekeeper is the reference **runtime enforcement implementation** for the **GRC-P** governance architecture and the **RGIS** runtime protocol.

It evaluates operational requests against authoritative governance state before execution occurs.

The gatekeeper does not define governance.  
It enforces permit/deny decisions using registry authority state.

---

## Role in the Stack

```text
GRC-P             → Governance architecture
RGIS              → Runtime interoperability protocol
GovenAI Registry  → Registry authority implementation
JobQue Gatekeeper → Gatekeeper enforcement implementation

GRC-P defines the governance architecture.

RGIS defines the runtime protocol between registry and gatekeeper.

GovenAI Registry provides governance authority state.

JobQue Gatekeeper enforces runtime decisions before execution.

Responsibilities

The gatekeeper is responsible for:

intercepting operational requests

canonicalizing request structure

verifying identity and signatures

validating replay protection

consulting registry authority via RGIS

issuing deterministic PERMIT / DENY decisions

recording tamper-evident enforcement evidence

Relationship to GRC-P and RGIS

JobQue Gatekeeper implements the runtime enforcement role defined by GRC-P.

It consumes authority state from registry implementations via RGIS.

Repositories:

GRC-P: https://github.com/Ventiser/grc-p

RGIS: https://github.com/Ventiser/rgis

GovenAI Registry: https://github.com/Ventiser/govenai-registry

Repository Structure
architecture/         gatekeeper enforcement model
runtime/              runtime request evaluation flow
identity/             actor identity and nonce handling
decisions/            permit/deny decision model
evidence/             enforcement evidence ledger
registry-integration/ RGIS registry consultation notes
conformance/          gatekeeper implementation notes
Status

Draft publication of the JobQue Gatekeeper v1.0 reference implementation model.

## Related Repositories

GRC-P — Governance architecture  
https://github.com/Ventiser/grc-p

RGIS — Registry–Gatekeeper protocol  
https://github.com/Ventiser/rgis

GovenAI Registry — reference registry authority implementation  
https://github.com/Ventiser/govenai-registry

JobQue Gatekeeper — reference runtime enforcement implementation  
https://github.com/Ventiser/jobque-gatekeeper

## Stewardship

Maintained by **Ventiser**.
