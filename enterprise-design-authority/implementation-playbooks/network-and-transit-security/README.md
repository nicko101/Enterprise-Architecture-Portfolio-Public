# Network & Transit Security

## Overview
This domain documents the foundational transport layer of the hybrid environment. It focuses on high-availability routing, centralized security enforcement, and secure remote connectivity patterns.

---

## Networking Playbooks

### Hybrid Connectivity & DNS
* **[Hybrid S2S VPN Integration](./hybrid-s2s-vpn-integration/)**: BGP-enabled Site-to-Site connectivity patterns.
* **[Hybrid DNS Private Resolver](./hybrid-dns-private-resolver/)**: Resolving names across On-Prem and Azure VNets.
* **[Secure Remote Access (P2S)](./secure-remote-access-p2s/)**: Certificate-based OpenVPN gateway for remote access.

### Security & Governance
* **[Hub-and-Spoke Firewall Governance](./hub-and-spoke-firewall-governance/)**: Azure Firewall inspection for East-West and North-South traffic.
* **[Palo Alto NGFW Core Deployment](./palo-alto-ngfw-core-deployment/)**: Integrating NVA for advanced security enforcement.
* **[Azure NVA Transit Infrastructure](./azure-nva-transit-infrastructure/)**: Centralized transit VNet architecture.

### Traffic Steering & Ingress
* **[Application Gateway L7 Routing](./application-gateway-l7-routing/)**: Secure web ingress with TLS termination.
* **[Load Balancing & Traffic Steering](./load-balancing-and-traffic-steering/)**: High-availability workload distribution.

---
[Return to Implementation Playbooks](../README.md) | [Return to Repository Root](../../../README.md)
