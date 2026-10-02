# Development and delivery evidence

## Public practice and review criteria

The public SDK tests event construction and schema agreement. Labs tests reproducible scenarios and local analysis. Repository health checks validate syntax and Markdown. Those checks have a bounded scope; they are not a comprehensive security audit of a private system.

For a proposed release, request the following authored review record:

1. Scope, intended behavior, threat assumptions and affected trust boundaries.
2. Reviewed source changes with negative tests and a record of unresolved findings.
3. Identified build inputs, dependencies, runtime and artifact hash.
4. Local and CI results recorded separately, including warnings and advisory dispositions.
5. Release approval, recovery/rollback plan and compatibility notes.
6. Actual deployment version and post-deployment observations where deployment is in scope.

## Completion

An approved source change, passing CI and a deployed release are distinct gates. Do not mark a finding closed because a PR exists, or claim private-product controls from public fixture tests. Record unknowns and accepted exceptions explicitly.

[NIST SSDF 1.1](https://csrc.nist.gov/pubs/sp/800/218/final) provides a final secure-development reference. This page supplies questions and evidence fields; it does not certify conformance to SSDF or attest to an unpublished private lifecycle.
