# poc and validation: engineering verification

this directory contains the testing methodologies and success criteria used to verify architectural assumptions before final deployment.

---

## architecture modules
the following sub-directories contain the technical evidence for each validation domain:

* [**cross-tenant-private-link**](./cross-tenant-private-link/) - testing azure private link service and endpoint consistency.
* [**ndes-scep-publishing-pattern**](./ndes-scep-publishing-pattern/) - infrastructure for automated certificate enrollment.
* [**vpngw-p2s-internal-pki**](./vpngw-p2s-internal-pki/) - verification of point-to-site connectivity using private pki.

---

## navigation
* [**back to design authority**](../README.md)
* [**back to main lab architecture**](../../README.md)

---

## system integrity & verification
validation evidence and configuration exports for this service are centralized in the module-level hub.
