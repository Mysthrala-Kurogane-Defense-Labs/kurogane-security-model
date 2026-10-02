# Data and privacy review

## Input

Classify operational inventory, telemetry, alarms, identities, audit logs and support evidence. Industrial data may reveal production patterns; logs and user records can contain personal information. Synthetic fixtures are not a substitute for reviewing real data flows.

## Review steps

1. Map each field to a stated purpose and required recipient. Remove unnecessary collection before choosing retention.
2. Record storage, backups, administrative access, external transfers and deletion limits.
3. Ask the actual controller and reviewer to determine legal basis, notices, processors and applicable transfer requirements. Do not infer these from hosting location.
4. Exercise export and deletion with invented records in an agreed test environment. Record copies that remain and why.

## Output

A private data register with purpose, sensitivity, owner, recipients, retention, access and supporting evidence. Unknown processor, location or deletion behavior remains a review gap.

## Limits

The public examples contain invented identifiers and fixed values. An extension field can still leak a secret or a person's name; schema validation does not detect that. No private deployment's privacy compliance, retention mechanism, encryption or legal basis is established by this document. See the [data-control guide](https://github.com/Mysthrala-Kurogane-Defense-Labs/kurogane-docs/blob/main/docs/data-sovereignty.md).
