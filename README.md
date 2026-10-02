# Kurogane Security Model

Security questions and evidence requirements for companies, reviewers and developers evaluating the public Kurogane ecosystem. These pages describe **review criteria and recommended controls**, not an attestation that a private deployment implements them.

## Start with a concrete decision

| Decision | Guide | Evidence to request |
| --- | --- | --- |
| What could go wrong? | [Threat model](threat-model.md), [trust boundaries](trust-boundaries.md) | Scoped flow diagram and tested failure behavior |
| Who can connect? | [Credentials](credential-handling.md), [network assumptions](network-assumptions.md) | Access review and approved flow list |
| Can we recover? | [Hardening](hardening-principles.md) | Restart, restore and rollback records |
| What data leaves the site? | [Data/privacy review](data-privacy-model.md) | Field-level transfer and retention register |
| What is in a release? | [SBOM](sbom-strategy.md), [development lifecycle](secure-development-lifecycle.md) | Artifact hash, component inventory and review results |
| How do we inspect the private core? | [Controlled access](controlled-review-access.md) | Agreed scope, access conditions and evidence handling |

Use the [review checklist](security-review-checklist.md) to record **verified / failed / unknown / not applicable**, with owner, version, date and supporting evidence. Unknown is not a passing result.

## Verified public boundaries

The SDK constructs and validates synthetic events and previews publication; it has no HTTP transport. Labs generates finite local scenarios. Its optional Node-RED editor is unauthenticated and bound to loopback. Those facts concern the public examples; private Hub authentication, tenancy, deployment and recovery remain outside the evidence supplied here.

For a sensitive finding, follow the [private disclosure process](disclosure-policy.md). For service or review requests, contact [MKDL](https://mkdl.jp/).

## Sources and license

See [NIST OT guidance](https://csrc.nist.gov/pubs/sp/800/82/r3/final), [NIST SSDF 1.1](https://csrc.nist.gov/pubs/sp/800/218/final) and the topic-specific primary links. Checked 2 October 2026; draft revisions are not substituted for final guidance. These authored questions do not reproduce a standard or establish compliance. Documentation retains [CC BY-ND 4.0](LICENSE.md).
