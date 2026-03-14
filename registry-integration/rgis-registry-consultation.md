# RGIS Registry Consultation

The JobQue Gatekeeper consults registry authority using the RGIS protocol.

The minimal interaction is:

```text
Canonical Request
        ↓
RGIS Decision Query
        ↓
Registry Response
        ↓
PERMIT / DENY Enforcement

The gatekeeper is responsible for:

sending protocol-valid requests

verifying registry responses

enforcing deterministic outcomes

denying execution when protocol validity fails

Detailed protocol behavior is defined in the RGIS repository.
