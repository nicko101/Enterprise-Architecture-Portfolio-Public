# cloud-networking

## hybrid-cloud connectivity
this module documents the secure extension of the on-premise infrastructure into the microsoft azure environment.

### azure site-to-site vpn
* **gateway architecture**: connection between the palo alto ngfw (on-prem) and the azure virtual network gateway (vnet-gw).
* **tunneling protocol**: ipsec vpn using ikev2 for secure, encrypted transit.
* **routing**: static or dynamic (bgp) routing ensuring internal subnets can reach azure workloads seamlessly.

## evidence & audit
validation evidence and configuration exports for the vpn gateway and ipsec tunnels are centralized here:
* [**access validation-proof hub**](./validation-proof/)

## navigation
- [back to parent category](../)
- [back to main lab architecture](../../../)
