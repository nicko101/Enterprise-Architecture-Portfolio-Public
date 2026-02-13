# switching | pki and dur design logic

this document outlines the technical design for **downloadable user roles (dur)** and the supporting pki infrastructure on the aruba-cx fabric.

## overview: downloadable user roles (dur)
dur allows clearpass to dynamically push port-access policies (vlans, acl, and rate-limits) to the switch upon successful authentication. this eliminates the need for static local roles and ensures centralized policy management.

### dynamic handshake process
1. **auth:** client authenticates via 802.1x or mac-auth.
2. **request:** the switch receives a role name and initiates an https request to clearpass.
3. **trust:** the switch validates the clearpass ssl certificate using the local trust anchor.
4. **apply:** the policy payload is downloaded and applied to the hardware.

## trust anchor (ta) implementation
as verified in the [**raw cli evidence**](../configuration-exports/cli-out.txt), the switch is configured with a specific trust anchor to facilitate the secure https download.

### le-ta profile
- **root ca:** isrg root x1 (let's encrypt)
- **purpose:** provides the root of trust for cppm.duckdns.org.
- **configuration key:** the usage https-client command is applied to this profile to authorize api traffic.

---
## navigation
- [back to switching hub](../)
- [back to main lab architecture](../../../../../)
