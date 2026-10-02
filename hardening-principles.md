# Hardening and recovery review

## Scope

Review a specific version and proposed environment. These are acceptance questions, not a declaration that controls exist in Kurogane Hub.

| Area | Action to request | Completion evidence |
| --- | --- | --- |
| Exposed services | Minimize listeners and restrict management paths | Dated configuration and approved exposure observation |
| Privilege | Limit application and support identities | Role review and denied-operation test |
| Updates | Pin inputs and agree a compatible update/rollback path | Version inventory and isolated rollback result |
| Recovery | Protect backups and demonstrate restoration | Restore record, readable data and measured recovery interval |
| Logs | Retain useful events without secrets | Example redacted records and access/retention review |
| Capacity | Bound payloads, queues and storage | Limit tests and operator-visible failure behavior |

Changes on real OT assets require owner approval, vendor constraints, a maintenance plan and stop conditions. A generic hardening action can affect operational availability.

The public lab pins images and limits editor publishing; it does not establish production hardening, secure defaults for a private deployment, vulnerability-free images or HA. Use [NIST OT guidance](https://csrc.nist.gov/pubs/sp/800/82/r3/final) as context and retain evidence specific to the installation.
