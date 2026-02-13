# enterprise architecture portfolio
## hybrid cloud infrastructure and security governance

this repository documents a comprehensive engineering lifecycle, spanning from high-level design authority to the execution of a fully validated hybrid-cloud environment. it serves as the centralized source of truth for technical designs, configurations, and operational evidence.

---

## portfolio directory

### 1. [enterprise design authority](./enterprise-design-authority/)
**the architectural blueprint** houses master governance and technical standards. it contains the high-level logic for l3 transit, virtual router (vr) segmentation, and security policy frameworks.

### 2. [complete hybrid network lab](./complete-hybrid-network-lab/)
**the engineering execution** the technical implementation of the enterprise on-premise to azure migration.
* **networking**: bgp fabric, s2s vpn tunnels, and transit gateway logic.
* **security**: palo alto ngfw policies (app-id/user-id), ssl decryption, and identity governance.

---

## engineering pillars
every technical deployment adheres to a standardized validation framework to ensure production-readiness:
* **design docs**: architectural requirements and ip addressing schemas.
* **configuration**: native exports (xml, json, cli) of applied security and network logic.
* **validation proof**: operational evidence including logs, session tables, and connectivity status.
