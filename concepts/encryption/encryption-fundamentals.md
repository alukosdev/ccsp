!!!danger
This page is currently queued for revision.
!!!

# Encryption Fundamentals*

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
DAR | Data at Rest
DIM | Data in Motion
DIT | Data in Transit
DIU | Data in Use
EFS | Encrypting File System
FDE | Full Disk Encryption
FPE | Format-Preserving Encryption
HSM | Hardware Security Module
IaaS | Infrastructure-as-a-Service
PaaS | Platform-as-a-Service
SaaS | Software-as-a-Service
TPM | Trusted Platform Module
WDE | Whole Disk Encryption

## Glossary

=== Diffie-Hellman
The Diffie-Hellman *key exchange process* is used for *asymmetric encryption* and is designed to allow two parties to create a shared secret (symmetric key) over an untrusted medium.

!!!
Diffie-Hellman is not a symmetric algorithm; it is an asymmetric algorithm used to establish a shared secret for a symmetric key algorithm.
!!!
=== Hardware Security Module (HSM)
A device that can safely *store* and *manage* encryption keys used in servers, data transmission, log files, and so forth.

!!!
The key difference between HSM and TPM is that an HSM manages keys for several devices, whereas a TPM is specific to a single device.
!!!
=== Homomorphic Encryption
Intended to allow for processing of encrypted material without decrypting it first. Since the data is never decrypted, the provider and anyone trying to intercept communication between the user and the cloud would never have the opportunity to view the data in plaintext form.
=== IPsec
IPsec is a framework for providing secure transmission of sensitive information over unsecured networks such as the Internet. IPSec works at the network layer, protecting and authenticating IP packets between participating IPsec endpoints.

IPsec can provide the following network security services:

- Confidentiality by encrypting packets before sending them across a network.
- Integrity by authenticating packets sent to ensure that the data has not been altered during transmission.
- Authentication of the source of the IPsec packets sent.
- Antireplay by detected and rejected replayed packets.

Downsides to IPsec:

- IPsec adds overhead to network traffic
- Not NAT friendly

!!!
IPsec does not always tunnel traffic. GRE is a technology leveraged by IPsec that performs tunneling. IKE is another aspect of IPsec that provides encryption.
!!!
=== Trusted Platform Module (TPM)
A physical chip on a host device which stores RSA encryption keys specific to that host for hardware authentication. The purpose is to provide WDE in the event that a hard drive is removed from its host.

!!!
The key difference between HSM and TPM is that an HSM manages keys for several devices, whereas a TPM is specific to a single device.
!!!
===

## Overview

Encryption will be used to protect data at rest, in transit, and in use. Encryption will be used on the remote user end to create the secure communication connection (VPN), on the cloud customer's enterprise to protect their own data, and within the datacenter by the cloud provider to ensure various cloud customers don't accidentally access each other's data.

Without encryption, it would be impossible to use the cloud in any secure fashion.

!!!
*Deidentification* is needed when you want to give a dataset to someone for statistical analysis or for testing new software but parts of the actual data (usually data that could be used to identify a person) must be hidden from them (often required by regulatory legislation).

*Encryption* is needed when you want to ensure that people who can access the files containing the data or backups can't read any of the data unless they are able to log in to the database and have database user permissions to see what they want to see. You may want to encrypt deidentified data for testing and performance measurement purposes, so that the testers can't see the identities but do find any problems arising out of the encryption as well as other problems - that's the case where both are needed.
!!!

Using encryption should always be directly related to business considerations, regulatory requirements, and any additional constraints that the organization may have to address.

There are three components of an encryption system:

- *The data*. This is the data object or objects that need to be encrypted.
- *The encryption engine*. Performs the mathematical process of encryption.
- *Key management*. All encryption is based on keys. Safe-guarding the keys is a crucial activity, necessary for ensuring the ongoing integrity of the encryption implementation and its algorithms.

## Encryption by Data Architecture

+++ DAR
- FDE/WDE (BitLocker) to encrypt the entire drive
- Database encryption (transparent encryption)
- Volume encryption to encrypt a specific volume
- File or directory encryption (EFS) to encrypt individual files, folders, or directories
- FPE
- DLP
+++ DIM/DIT
- VPN (IPsec) to provide confidentiality
- TLS/SSL/HTTPS to prevent eavesdropping or tampering
- VLANs help provide confidentiality and integrity
- DLP provides control between demarcation network zones by using activity monitoring and egress filtering
+++ DIU
- Digital signatures and encryption to protect APIs.
- IRM can be used as a means for data classification and control.
- DRM is an extension of normal data protection which is encapsulated within the concept of IRM. In DRM, advanced security controls such as extra ACLs and permission requirements are placed onto the data.
+++

### Data at Rest (DAR)

Data at rest is mostly associated with *storage*.

DAR is data that is stored on some type of media such as a hard disk drive or solid state drive. DAR deals with storage-based data.

Availability and integrity of DAR is controlled through the use of redundant storage.

!!!
DAR is *best* protected using encryption methods such as AES (which is used by most FDE/WDE encryptions, including BitLocker).
!!!

### Data in Motion/Data in Transit (DIM/DIT)

Data in motion/data in transit is mostly associated with *network traffic*.

DIM deals with moving data across network or communication links. Transferring data from one computer to another such as via SFTP, or by using an interactive user session such as submitting data via a browser.

DIM is typically associated with network traffic and is deployed near the gateway. For this reason, SSL interception would be necessary to inspect encrypted (HTTPS) traffic. The topology is a mixture of proxy, network tapping, or SMTP relays.

!!!
DIM/DIT is *best* protected by using encrypted transport methods such as TLS.
!!!

### Data in Use (DIU)

Data in use is mostly associated with *endpoints*.

DIU is data that is *actively being manipulated* by a specific user endpoint, such as if a file is opened and being worked on. This is drastically different than DIM; DIU is data that is being processed by the CPU in real-time.

DIU is mostly concerned with the actual endpoint. It requires leading edge technology and is not commonly protected. It offers insights into how users access/process data files. Client-based technology is typically more complex due to the large number of devices, users, and potential for multiple locations.

!!!
DIU is *best* protected through secure API calls and web services, which make use of technologies such as digital signatures.
!!!

## Encryption by Service Model

+++ IaaS
- Volume encryption
  - Instance-managed encryption
  - Externally-managed encryption
- Object and file storage
  - Client-side encryption
  - Server-side encryption
  - Proxy encryption
+++ PaaS
- Application layer encryption
- Database encryption
- Other
+++ SaaS
- Provider-managed encryption
- Proxy encryption
- [DLP]
- [Dedicated appliance/server]
- [Virtual appliance]
- [Endpoint agent]
- [Hypervisor agent]
- [DAM/FAM]
+++

### IaaS

#### Volume Storage Encryption

- *Instance-managed encryption*. The encryption engine runs within the instance, and the key is stored in the volume but protected by a passphrase or keypair.
- *Externally managed encryption*. The encryption engine runs in the instance, but the keys are managed externally and issued to the instance on request.

Protects from the following risks:

- Snapshot cloning/exposure
- Exploration by the cloud provider (and private cloud admins)
- Exposure by physical loss of drives

#### Object and File Storage Encryption

- *Client-side encryption*. When object storage is used as the back-end for an application, encrypt the data using an encryption engine embedded in the application or client.
- *Server-side encryption*. Data is encrypted on the server (cloud) side after being transferred in. The cloud provider has access to the key and runs the encryption engine.
- *Proxy encryption*. In this model, you connect the volume to a special instance or appliance/software, and then connect your instance to the encryption instance. The proxy handles all crypto operations and may keep keys either onboard or externally.

!!!
Object storage encryption is best able to protect against hardware theft. Since encryption occurs at the OS level, anyone with access to the OS already has access to that data.
!!!

### PaaS

*Application layer encryption*. Data is encrypted in the PaaS application or the client accessing the platform.
*Database encryption*. Data is encrypted in the database using encryption that's built in and is supported by a database platform like Transparent Database Encryption (TDE) or at the field level.
*Other*. These are provider-managed layers in the application, such as the messaging queue. There are also IaaS options when that is used for underlying storage.

### SaaS

SaaS providers may use any of the options previously discussed. It is recommended to use per-customer keys when possible, in order to better enforce multitenancy isolation.

*Provider-managed encryption*. Data is encrypted in the SaaS application and generally managed by the provider.
*Proxy encryption*. Data passes through an encryption proxy before being sent to the SaaS application.
