# connectivity and routing

## overview
this module documents the layer 3 topology of the hybrid lab. it defines the traffic flow between on-premises segments and azure vnets, managed by the palo alto virtual routers.

## core routing architecture

### inter-vr routing (palo alto)
the lab utilizes multiple **virtual routers (vr)** to enforce strict architectural isolation:
* **untrust-vr**: handles external transit and edge peering.
* **trust-vr**: manages internal vlan segments and private workloads.
* **shared-services-vr**: isolates core infrastructure (ad ds, pki) from general traffic.
* **logic**: route leaking is strictly controlled via static routes between vr instances, ensuring the security policy engine inspects all cross-vr traffic.

### bgp and hybrid transit
* **bgp peering**: dynamic route propagation between the palo alto nva and azure route server.
* **transit gateway**: centralized hub-and-spoke logic for scalable vnet integration.

## evidence & audit
* [**access validation-proof hub**](./validation-proof/)

## navigation
- [back to networking](../)
- [back to main lab architecture](../../)
