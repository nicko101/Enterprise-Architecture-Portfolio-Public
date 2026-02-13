# automated trust: ndes & scep architecture

## overview
this module documents the deployment of the **network device enrollment service (ndes)** and the **simple certificate enrollment protocol (scep)**. this infrastructure acts as the trust bridge between the on-premises certificate authority (ca) and cloud-managed endpoints via **microsoft intune**.

## architecture flow
![ndes scep architecture](./ndes-scep.png)


### core components
* **root ca**: lab02rootca - the offline root of trust.
* **intermediate ca**: lab02-interca-ca - issues the ndes service certificates.
* **ndes server**: 
des01.duckdns.org - delegates scep challenges and pushes certificates to the intune service.
* **intune policy**: lab02-scep-machine - orchestrates the certificate delivery to authorized endpoints.

## engineering policies
the intune admin center is configured with specific engineering callouts for:
- **trusted certificates**: establishing the chain of trust for the lab02-interca-ca.
- **scep certificates**: machine-level enrollment policies (lab02-scep-machine).
- **user certificates**: identity-based enrollment for authorized lab users.

## navigation
- [view validation proof](./validation-proof/)
- [back to infrastructure root](../../)
