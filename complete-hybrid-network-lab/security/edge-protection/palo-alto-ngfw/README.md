# palo alto ngfw | edge protection implementation

this module covers the core security services implemented on the palo alto platform to provide perimeter and internal segmentation.

---

## configuration modules

### [app-id](./app-id/)
implementation of application-level visibility and control to reduce the attack surface. **validation evidence and configuration exports for this service are centralized in the module-level hub.**

### [network-segmentation](./network-segmentation/)
zone-based policy architecture and inter-vlan traffic control. validation evidence is centralized in the module-level hub.

### [threat-prevention](./threat-prevention/)
antivirus, anti-spyware, and vulnerability protection profiles. validation evidence is centralized in the module-level hub.

### [ssl-decryption](./ssl-decryption/)
visibility into encrypted traffic for inspection and policy enforcement. validation evidence is centralized in the module-level hub.

### [user-id-mapping](./user-id-mapping/)
integration of identity into security policies for user-based visibility. validation evidence is centralized in the module-level hub.

### [global-operations](./global-operations/)
general management, high-availability (ha) state, and system-wide configuration. validation evidence is centralized in the module-level hub.

---

## navigation
* [**back to edge protection**](../)
* [**back to main portfolio architecture**](../../../../)