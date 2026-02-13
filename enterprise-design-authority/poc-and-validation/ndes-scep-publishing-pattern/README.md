# PoC: Securing NDES/SCEP via Azure App Proxy
**Engineering-led refactoring: Moving from Edge-Inbound to Zero Trust Proxy**

---

## The Catalyst (Tactical Pivot)
While performing a certificate rotation for a Palo Alto SSL Inspection certificate, I identified a significant security exposure: the NDES server was reachable via a Public IP with inbound firewall rules.

I initiated this PoC to prove that we could eliminate all inbound firewall requirements by utilizing Microsoft Entra Private Network Connector, transitioning from a legacy DMZ model to an outbound-only authenticated tunnel.

---

## Engineering Highlights
* **Zero Inbound Ports**: Removed Palo Alto inbound NAT rules and Load Balancer (LB) VIPs.
* **Identity-Driven Access**: Leveraged Entra Enterprise App for pre-authentication.
* **NAC Integration**: Mapped Intune SCEP Profiles to the Proxy URL for Aruba ClearPass Wi-Fi authentication.

---

## Technical Validation
To ensure the integrity of the enrollment process, validation was performed across three distinct layers. Detailed log analysis and success confirmations are available in the project evidence folder.

* **Endpoint Verification**: Confirmed successful CSR generation and certificate delivery on managed devices.
* **Network Verification**: Monitored internal service availability via IIS logs to ensure the Proxy-to-NDES handoff was seamless.
* **Proxy Verification**: Validated authenticated outbound sessions via the Entra Private Network Connector.

---

## Project Artifacts
* [Technical Design and Validation Guide](./documentation/validation-guide.md)
* [Verification Logs and Success Screenshots](./evidence/)
* [Configuration Templates](./templates/)

---
[Return to Solutions Architecture](../../) | [Return to Root](../../../)
