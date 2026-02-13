## enterprise-hybrid-architecture-portfolio

this repository represents a **fully functional enterprise network environment (lab02)**. all architectural decisions were validated through live engineering trials and forensic analysis.

---

### ??? cloud networking

the architecture is hosted on a high-availability virtualization cluster, utilizing tiered storage to separate management traffic from bulk data assets.

* **infrastructure resilience:** storage architecture was recently optimized to utilize a 1.2tb high-capacity pool for templates and virtual disks, ensuring the host os remains insulated from capacity-driven deadlocks.
* **storage tiering:** implemented zfs reservations on the root partition to maintain cluster configuration availability during peak i/o events.

---

### ?? evidence & audit

validation evidence and configuration exports for this service are centralized in the module-level hub. this ensures a clear chain of custody for all architectural changes and security policy implementations.

---

### ??? engineering notes: forensic recovery

this repository includes documentation on the recovery of the pve management layer following a filesystem deadlock. key actions included:

* **capacity recovery:** manual purge of stale system journals and apt-cache to recover critical boot space.
* **asset migration:** migration of 50gb of iso templates to secondary storage via cli to bypass gui lockout and restore write-access to the cluster filesystem.
* **process restoration:** restoration of the **pve-cluster** service and cleanup of uninterruptible "zombie" kvm processes to normalize console access.

---

### ?? navigation

* **[access validation-proof hub]**
* **[back to parent category]**
* **[back to main lab architecture]**
