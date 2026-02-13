# infrastructure | core architectural modules

this section documents the foundational compute, identity, and virtualisation layers of the hybrid cloud architecture. 

---

## architecture modules

* [**compute-and-servers**](./compute-and-servers/) - high-level architecture and implementation of server configurations.
* [**endpoint-and-device-management**](./endpoint-and-device-management/) - management of win10 hosts and lab endpoints.
* [**identity-and-trust**](./identity-and-trust/) - aruba cppm, active directory, and zero-trust admission.
* [**platform-and-virtualisation**](./platform-and-virtualisation/) - proxmox foundation and hypervisor-level configuration.
* [**storage-and-data-services**](./storage-and-data-services/) - centralised storage and data pathing.

---

## cloud networking & system integrity
validation evidence and configuration exports for this service are centralised in the module-level hub. the 'packet life' walk through these modules confirms end-to-end path validity.

* [**access validation-proof hub**](./compute-and-servers/validation-proof/)

---

## navigation
* [back to parent category](../)
* [back to main lab architecture](../../README.md)

---

> **methodology note**: architectural visuals and slide evidence were synthesised by processing raw technical logs and running-configurations through **notebooklm** to ensure direct alignment with actual lab logic.
