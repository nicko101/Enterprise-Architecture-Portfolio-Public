# clearpass policy suite

the policy engine for the enterprise architecture. manages radius/tacacs+ authentication and defines the "trust level" for every device connecting to the fabric.

---

## architecture modules
* [guest](./guest/) - captive portal and temporary access workflows.
* [onboard-(byod-&-pki)](./onboard-(byod-&-pki)/) - secure certificate enrollment and private pki integration.
* [onguard](./onguard/) - device posture assessment and health-based enforcement.
* [policy-manager](./policy-manager/) - core rbac and authorization logic.

---

## navigation
* [back to design authority](../../)
* [back to main lab architecture](../../../README.md)

---

## system integrity & verification
validation evidence and configuration exports for this service are centralized in the module-level hub.
