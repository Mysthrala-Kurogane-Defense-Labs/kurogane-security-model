# Credential handling review

## Inputs

List accounts and service identities by purpose, owner, scope, storage location, expiry, rotation and revocation path. Keep actual secrets out of the register and public issues.

## Recommended checks

- Separate individual, administrator and service identities; avoid anonymous shared support access.
- Require explicit approval and bounded access for a provider session.
- Keep credentials outside source, images, fixtures, URLs and logs. Use a suitable secret store for the actual deployment.
- Define rotation and revocation after personnel, provider or incident changes.
- Determine how collectors behave after expiry or lost access; prevent unbounded retries or silent data loss.

## Evidence exercise

In an agreed test environment, revoke an invented service identity, confirm new access fails, and verify that the operator can distinguish lost access from normal telemetry. Check logs for secret leakage without publishing the logs themselves.

## Public boundary

The public SDK implements no transport credentials or authentication. Its URL preview rejects embedded user information but cannot identify a secret placed in a query or event extension. No private-system credential store, MFA policy or rotation mechanism is attested here.

Output: dated access review, demonstrated revocation and unresolved lifecycle decisions, with owners.
