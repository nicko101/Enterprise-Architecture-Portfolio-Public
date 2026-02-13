# Modern Data Services

## Overview
This domain documents the transition from legacy, public-facing data services to secure, private, and cloud-native storage architectures. We focus on removing public exposure and modernizing file collaboration using the Azure Well-Architected Framework.

---

## Data Modernisation Playbooks

###  [Azure Storage: DFS to Files](./azure-storage-(dfs-to-files)/)
* **Pattern:** Migrating legacy Distributed File System (DFS) namespaces to Azure Files using Azure File Sync for hybrid access.
* **Security:** Transitioning from SMB over VPN to modern cloud-native storage endpoints.

###  [Azure Private Endpoints](./azure-private-endpoints/)
* **Pattern:** Implementing Azure Private Link to ensure that data services (Storage, SQL, Key Vault) are only accessible via private IP addresses within the VNet.
* **Security:** Eliminating public internet exposure for PaaS resources.

---
[Return to Implementation Playbooks](../README.md)
