# Scoped security review checklist

For each row record **verified / failed / unknown / not applicable**, owner, component/version, checked date, evidence reference and next action. Do not put completed customer records into public GitHub issues. A check mark without evidence is not a verified result.

| Check | Evidence / acceptance question |
| --- | --- |
| Scope and permission | Named owner, reviewed systems, allowed methods and stop conditions |
| Asset/dependency inventory | Dated register with unknowns and operational owners |
| Trust boundaries | Actual flows and negative authorization tests |
| Source/event integrity | Authentication, duplicate and replay policy; timestamp handling |
| Freshness and outages | Operator distinguishes missing data from normal operation |
| Credentials/support | Approval, least privilege, expiry and demonstrated revocation |
| Network exposure | Approved listeners/flows and permitted denial observations |
| Recovery | Restore and rollback evidence against agreed targets |
| Data/privacy | Field-level purpose, access, recipients, retention and deletion limits |
| Software inventory | Artifact-bound SBOM, advisory date and finding dispositions |
| Delivery | Reviewed patch; separate local, CI, approval and deployment records |
| Residual findings | Exact count, owner and acceptance or remediation plan |

The SDK and labs can support contract and synthetic-behavior checks only. They cannot complete the private-product or customer-environment rows. Use the [topic guides](README.md) to define the required evidence.
