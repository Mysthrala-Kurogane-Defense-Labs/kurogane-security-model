# Trust boundaries

## Record each crossing

For every actual data or control path, record sender, receiver, identity, fields, protocol, permissions, failure behavior, owner and supporting evidence.

| Proposed crossing | Question to resolve |
| --- | --- |
| Equipment to connector | Is observation approved and read-only? Can malformed input exhaust resources? |
| Connector to receiver | Who authenticates the sender? Which events, sizes and rates are accepted? |
| User to application | Which roles permit viewing, exporting or changing each object? |
| Administrator to infrastructure | Which approval, time limits, logs and revocation apply? |
| Local to external service | Which fields leave, who receives them and what happens during an outage? |
| One customer context to another | Where is separation enforced and how is denial tested? |

## Verification

In an agreed isolated environment, test denied operations as well as successful ones. Use synthetic identities and records. Keep the application, network and storage boundaries separate: a firewall does not prove object-level authorization.

## Public example boundary

The generator reads invented local model data. The validator and analyzer read local files. The SDK returns a local preview. Optional Node-RED runs an unauthenticated editor on host loopback. These examples do not implement or test a private Hub's user, customer or network boundaries.

Output: a reviewed flow register with every crossing marked verified, failed, unknown or not applicable. Do not publish a customer's topology or credentials with it.
