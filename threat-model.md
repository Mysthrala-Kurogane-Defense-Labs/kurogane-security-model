# Threat model for a scoped review

## Scope and assets

Start with a dated component and data-flow diagram. Identify operational availability, event integrity, credentials, sensitive inventory, evidence records and operator decisions. Include source equipment, connector, receiver, administrator, provider and external services where actually present.

| Threat hypothesis | Boundary / consequence | Evidence or test to request |
| --- | --- | --- |
| Forged or replayed event | Source to receiver; false operational picture | Source authentication and duplicate/replay policy tested with invented events |
| Missing or delayed data | Collection to operator; absence mistaken for normal operation | Freshness indicators, queue limits and outage observations |
| Stolen support account | Provider to customer; unauthorized changes | Scoped identity, approval, revocation and access-log review |
| Untrusted dependency or build | Source to release; modified artifact | Pinned inputs, review, artifact hash and component inventory |
| Cross-customer data access | Identity to storage; confidentiality loss | Tenant-boundary design and negative authorization tests where multitenancy exists |
| Lost host or backup | Operation to recovery; extended interruption | Independently observed restore against agreed recovery targets |

## Use and output

Assign owner, current evidence, uncertainty, action and acceptance criterion to each applicable hypothesis. Add threats specific to the actual environment; this table is not exhaustive. Consider safety consequences with the operational owner rather than deriving them from a software finding alone.

The SDK's schema checks input shape but not source identity, freshness or authenticity. The lab's telemetry gap demonstrates absent observations only. None of the proposed private-system controls is proven by this model.
