\# 🚀 Azure NVA Transit Infrastructure



\## 🏛️ Architecture Overview

This section documents a high-availability \*\*Palo Alto NVA\*\* transit hub. The design utilizes a "Load Balancer Sandwich" to provide stateful inspection and deterministic routing for all hybrid cloud traffic.



---



\## 🗺️ Technical Components

\* \*\*Palo Alto NVA\*\*: Deployed via ARM templates with multi-interface support (Untrust/Trust) for zone-based security.

\* \*\*Dual Load Balancers\*\*: 

&nbsp;   \* \*\*External LB\*\*: Manages inbound Gateway traffic with \*\*Source-IP Persistence\*\* to ensure stable IPsec negotiation.

&nbsp;   \* \*\*Internal LB\*\*: Serves as the \*\*Next Hop\*\* for internal subnets, providing high availability for East-West traffic.

\* \*\*User Defined Routes (UDR)\*\*: Custom Route Tables force all traffic through the Internal LB's Virtual IP (VIP) for centralized inspection.



---



\## ✅ Operational Validation

\* \*\*Routing Logic\*\*: \[Verified Traffic Steering via Tunnel 200](https://github.com/nicko101/Enterprise-Architecture-Story/blob/main/Packet-Life-Forensics/slide-pbf.png).

\* \*\*Deployment Status\*\*: \[System Status: Verified](https://github.com/nicko101/Enterprise-Architecture-Story/blob/main/Packet-Life-Forensics/status.png).



> 🚀 \*\*Engineering Note\*\*: This transit model is fully automated via ARM templates, allowing for the rapid deployment of standardized security perimeters across multiple Azure regions.

