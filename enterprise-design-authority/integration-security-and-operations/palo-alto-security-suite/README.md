# palo alto security suite

## overview
this design module defines the core security capabilities of the palo alto ngfw ecosystem within the enterprise architecture. it focuses on moving beyond traditional port-based filtering toward a zero-trust, identity-aware security posture.

## security pillars

### [inter-vr-routing](./inter-vr-routing/)
the segmentation backbone. isolation of traffic zones (untrust, trust, dmz) into independent virtual routers to prevent unauthorized lateral movement.

### [ssl-decryption](./ssl-decryption/)
the visibility foundation. defines the inspection of encrypted traffic to prevent threats from bypassing security controls via tls.

### [user-id](./user-id/)
identity-based policy enforcement. mapping of network sessions to active directory identities for granular rbac.

### [app-id](./app-id/)
application-layer control. reducing the attack surface by enforcing policies based on application characteristics rather than legacy ports.

### [global-protect-mfa](./global-protect-mfa/)
secure remote access. hardening the network edge with encrypted vpn tunnels and multi-factor authentication.

## navigation
- [back to parent category](../)
