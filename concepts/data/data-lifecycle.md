# Data Lifecycle

## Quick Reference

| Acronym | Backronym |
| - | - |
| DLP | Data Loss Prevention |
| DRM | Digital Rights Management |
| IRM | Information Rights Management |

## Summary

Being able to destroy data, or render it inaccessible, in the cloud is critical to ensuring confidentiality and managing a secure lifecycle for data.

1. Map the different lifecycle phases.
2. Integrate the different data locations and access types.
3. Map these into functions, actors, and controls.

## Functions, Actors, and Controls

### Functions

=== Access/Read
View/read the data, including creating, copying, file transfers, dissemination, and other exchanges of information.
=== Process
Perform a transaction on the data; update it; use it in a business processing transaction, etc. This would *not* include viewing, since that is a component of accessing/reading.
=== Store
Hold the data (in a file, database, etc.).
===

![Information Lifecycle Phases](/static/information-lifecycle-phases.png)

### Controls

Controls act as a mechanism to restrict a list of possible actions to allowed or permitted actions. These controls can be of a preventative, detective (monitoring), or corrective nature.

To determine the necessary controls to be deployed, you must first understand the:

- Functions of the data
- Locations of the data
- Actors upon the data

![Mapping the Lifecycle](/static/mapping-the-lifecycle.png)

## Phases

==- Create/Update
The create phase is the initial phase of the data lifecycle. Data is created any time it is considered new. This encompasses data which is newly created, data that is being imported from elsewhere, and also data that already exists but has been modified into a new form. This phase could be considered "create/update".

- The *data owner* is defined.
- Data is *categorized*.
- Data is *classified*.
- Data is *labeled, tagged, and marked*.

The create phase is an ideal time to implement technologies such as SSL/TLS with the data that is inputted or imported. It should be done in the create phase so that the data is protected initially before any further phases.

For data created remotely:

- Data should be encrypted.
- Connections should be secured (such as by using a VPN).
- Secure key management practices should be practiced.

For data created within the cloud:

- Data should be encrypted.
- Secure key management practices should be practiced.
==- Store
Usually meant to refer to near-term storage (as opposed to long-term storage). Occurs almost concurrently with the Create phase.

As soon as data enters the store phase, it's important to immediately employ:

- The use of backup methods on top of security controls to prevent data loss.
- Additional encryption for data at rest.
- DLP and IRM technologies are used to ensure that data security is enforced during the Use and Share phases of the cloud data lifecycle. They may be implemented during the Store phase, but do not enforce data security because data is not accessed during this phase.

!!!
While security controls are implemented in the create phase in the form of SSL/TLS, *this only protects data in transit and not data at rest*. The store phase is the first phase in which security controls are implemented to protect data at rest.
!!!
==- Use
Data is vulnerable in this state since it must be unencrypted.

- Technologies such as DLP and IRM/DRM could be leveraged to assist with monitoring access.

For data being accessed from the user side:

- Connections should be secured (such as by using a VPN).
- The platforms with which users connect to the cloud should be secured.
- Permissions for modifying and processing should be implemented.
- Logging and auditing should be implemented.

For data being access from the provider side:

- Strong protections in the implementation of virtualization.
- Personnel and administrative controls should be implemented.

!!!
Due to the nature of data being actively used, viewed, and processed in the use phase, it is more likely to be leaked in this phase than in others.
!!!
==- Share
*IRM/DRM*. Can control who can share and what they can share.
*DLP*. Can identify and prevent unauthorized sharing.
*VPNs/encryption*. For confidentiality.
*Restrictions based on jurisdiction*. Export or import controls, such as ITAR, EAR, or Wassenaar.
==- Archive
- Data should be encrypted.
- Key management is of utmost importance.
- Physical security.
  - Location (environmental, jurisdictional, geographical)
  - Format (medium, portability, weaknesses, age)
  - Staff Procedure (recovery procedures, backups)
- Retention policies
  - Retention period
  - Applicable regulations
  - Retention formats
  - Data classification
  - Archiving and retrieval procedures
  - Monitoring, maintenance, and enforcement

Many cloud providers will offer archiving services as a feature of the basic cloud service; realistically, most providers are already performing this function to avoid inadvertent loss of customer data. Because the customer is ultimately responsible for the data, the customer may elect to use another, or an additional, archive method. The contract will stipulate specific terms, such as archive size, duration, and so on and will determine who is responsible for performing archiving activities in a managed cloud environment.
==- Destroy
- Cryptoshredding (cryptographic erasure)

!!!
It's very important to note that cryptoshredding requires two **cryptosystems**; one to encrypt the target data and one to encrypt the resulting encryption keys.
!!!
==-
