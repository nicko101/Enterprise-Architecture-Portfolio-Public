# packet life: forensic timeline and validation

this repository serves as the forensic flight recorder for the hybrid cloud architecture. it documents the packet life walk—the binary proof of identity-based access, deterministic routing, and cloud-ingress integrity.

---

## the validated packet journey

### 1. identity admission and edge security
* **statement of proof**: [digital identity card](./Packet-Life-Forensics/slide-cppm.png)
* **validation**: implementation of teap (eap-tls, eap-mschapv2) via aruba clearpass.
* **outcome**: verified session for lab02\nick on device win10, authorizing network access.

### 2. l3 mapping and deterministic provisioning
* **statement of proof**: [dhcp assignment](./Packet-Life-Forensics/slide-dhcp.png)
* **validation**: the pa-vm dhcp server binds the authenticated identity to a specific ip.
* **outcome**: host win10 committed to ipv4 address 10.0.11.17 from the 10.0.11.0/24 pool.

### 3. tunnel steering and policy enforcement
* **statement of proof**: [pbf routing logic](./Packet-Life-Forensics/slide-pbf.png)
* **validation**: policy-based forwarding (pbf) explicitly routes traffic through 'tunnel.200' for egress.
* **outcome**: traffic steered via pbf rule 'simulate-default-route'.

### 4. cloud ingress and forensic analysis
* **statement of proof**: [packet capture analysis](./Packet-Life-Forensics/slide-pcap.png)
* **artifact**: [raw capture (save.pcap)](./Packet-Life-Forensics/save.pcap)
* **diagnostic insight**: pcap analysis confirms bidirectional dns flow and active tcp management, proving end-to-end path validity.

---

## technical diagnostics
* **azure lb**: regional 'standard' sku (nf-elb) deployed in west europe.
* **health probes**: port 443 monitored every 5 seconds for backend availability.
* **traffic rules**: supports tcp (80, 443, 22) and udp (500, 4500) with sourceip load distribution.

---

## cognitive synthesis & notebooklm
the narrative components of this forensic timeline were synthesized using **notebooklm**. by feeding raw pcap analysis, clearpass session logs, and architectural configurations into the engine, i have ensured that the "packet life story" is grounded strictly in the primary source data of this lab. this represents an ai-augmented approach to complex architectural auditing.

---

## architectural validation status
**status: complete**
end-to-end architectural integrity is confirmed through the cross-correlation of identity logs, pbf enforcement, and packet-level captures.
