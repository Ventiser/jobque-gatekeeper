# Request Evaluation Flow

The JobQue Gatekeeper processes operational requests through a deterministic sequence.

## Runtime Flow

```text
Request Received
        ↓
Canonicalization
        ↓
Identity Verification
        ↓
Nonce Validation
        ↓
Registry Consultation
        ↓
Decision Generation
        ↓
Execution Allowed or Blocked
        ↓
Evidence Recorded
Outcome

The gatekeeper produces one of two outcomes:

PERMIT

DENY

If any required condition fails, the gatekeeper must deny execution.
