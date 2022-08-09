# Key Management

## Summary

The main considerations for key management are performance, accessibility, latency, and security. Can you get the right key to the right place at the right time while also meeting your security and compliance requirements?

### Challenges

- *Key storage*. Keys need to be stored in a secure manner. The optimal storage method is via a hardware solution such as an HSM.
- *Key replication*. Keys stored in the cloud via software will likely be backed up and replicated multiple times. This will require a good management system.
- *Key access*. Access to keys should be monitored and only permitted to authorized users.

### Considerations

- *Level of protection*. Encryption keys should *always* be secured at the same level or higher as the data they protect. The sensitivity of the data dictates this level of protection, according to the organization's **data security policies**. The strength of the cryptosystem is only valid if private keys are never disclosed.
- *Key recovery*. This usually entails a procedure that involves multiple people \(separation of duties/two-person integrity\), each with access to only a portion of the key.
- *Key distribution*. Keys should *never* be distributed in the clear. Often, passing keys out of band is a preferable, yet cumbersome and expensive, solution. 
- *Key revocation*. A process must exist for revoking keys.
- *Key escrow*. Keys are held by a trusted third party in a secure environment. This can aid in many management efforts.
- *Outsourcing*. It is preferable to have keys stored somewhere other than with the cloud provider or within the cloud provider's datacenter. Keys should *never* be stored with the data they're protecting.

## Key Management Methods

There are four potential options for handling key management:

- *HSM/appliance*. Use a traditional HSM or appliance-based key manager, which will typically need to be on-premises, and deliver the keys to the cloud over a dedicated connection.
- *Virtual appliance/software*. Deploy a virtual appliance or software-based key manager in the cloud.
- *Cloud provider service*. This is a key management service offered by the cloud provider. Before selecting this option, make sure you understand the security model and SLAs to understand if your key could be exposed.
- *Hybrid*. You can also use a combination, such as using a HSM as the root of trust for keys but then delivering application-specific keys to a virtual appliance that's located in the cloud and only manages keys for its particular context.

### Internally Managed

Keys are stored on the component that is also acting as the encryption engine.

- Storage-level encryption
- Internal database encryption
- Backup application encryption

Helpful for mitigating against the risks associated with lost media. However, this method alone is not ideal.

### Externally Managed

Keys are maintained separate from the encryption engine and data. They *can* be on the same cloud platform, internally within the organization, or on a different cloud.

!!!
Externally managed keys could also be referred to as "customer-managed" keys.
!!!

### Managed by a Third Party

Outsourcing key management to a third-party, such as a CASB.

Hosting the keys within the organization is expensive and complicated and attenuates some of the benefit we get from offloading our enterprise to the cloud. Another option is using a CASB. The cost of using a CASB should be lower than trying to maintain keys within the organization, and the CASB will have core competencies most cloud customer's wont.

## Key Management Systems

The following are ways to manage keys that allows the customer to generate, hold, and retain the keys. The foundational aspect is the customer must control the keys to retain maximum control of the data.

- Remote Key Management System
- Client-Side Key Management
