# Network assumptions to verify

## Input

Obtain an approved flow list with source, destination, direction, protocol, purpose, owner and expiry. Draw IT/OT and external-service boundaries without placing sensitive addresses in public material.

## Questions

Who can reach an engineering station, collector or editor? Are remote-support paths time-limited? Which DNS, time and identity services are required? Which outbound destinations are allowed? What changes when Internet or a gateway fails?

## Verification

Compare the proposed flow list with configuration evidence and permitted observations. Test intended denials in a separate environment under an agreed plan. Do not infer isolation merely from a VLAN label, or scan an operational network without owner and vendor approval.

## Public lab assumptions

Compose starts the generator without an exposed port. Node-RED is optional and publishes to `127.0.0.1`; its editor has no configured authentication. Keep it on a trusted development machine. Loopback is not user authorization, and container networking still needs an exposure review before shared use.

See [Docker port-publishing behavior](https://docs.docker.com/engine/network/port-publishing/) and [Node-RED security guidance](https://nodered.org/docs/user-guide/runtime/securing-node-red). These assumptions are not a firewall specification for a private Hub installation.

Output: approved flows, tested denials, outage behavior and explicitly unresolved dependencies.
