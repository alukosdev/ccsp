# Encryption Types

## Storage Encryption

### Basic Storage-Level Encryption

- The encryption engine is located on the storage management level, with the keys usually held by the CSP.
- The engine encrypts data written to the storage and decrypts it when exiting the storage.
- Only protects from hardware theft or loss; does not protect from CSP administrator access or any unauthorized access from the layers above the storage.

### Volume Storage Encryption

- Typically accomplished through an encrypted container, which is mapped as a folder or volume.
- Only allows access through the volume OS and provides protection against physical loss or theft, external administrator access, snapshot and storage-level exfiltration.
- Does not protect against access made through the instance or an attack within the application running on the instance.
- Key is managed by customer in IaaS.

Volume storage can use the following types of encryption:

#### Instance-Based Encryption

The encryption engine is located on the instance. Keys can be guarded locally but should be managed external to the instance.

#### Proxy-Based Encryption

The encryption engine is running on a proxy instance or appliance. The proxy instance is a secure machine that handles all cryptographic actions, including key management and storage. Keys can be stored on the proxy or via the external key storage, with the proxy providing the key exchanges and required safeguarding of keys in memory.

### Object Storage Encryption

Object storage can use the following types of encryption:

- *File-level encryption*. This is typically in the form of IRM/DRM. The encryption engine is commonly implemented at the client side (in the form of an agent) and preserves the format of the original file.
- *Application-level encryption*. The encryption engine resides in the application that is using the object storage. This type of encryption can be used with:
  - Database encryption
  - Object storage encryption
  - Can leverage proxy encryption (although this is more commonly seen in volume storage)

!!!
Application encryption is associated with object storage.
!!!

## Database Encryption

### File-Level Encryption

Database servers typically reside on volume storage. For this deployment, you are encrypting the volume or folder of the database, with the encryption engine and keys residing on instances attached to the volume.

Provides **protection** from:

- Media theft
- Lost backups
- External attacks

Does not provide protection from:

- Attacks with direct access to the application, OS, or database

### Transparent Encryption

The encryption engine resides within the database, and it is transparent to the application. Keys usually reside within the instance, although processing and managing them may be offloaded to an external KMS.

Provides **protection** from:

- Media theft
- Backup system intrusions
- Certain database and application-level attacks

!!!
Oracle and Microsoft refer to this as Transparent Database Encryption (TDE). Sybase references this as Application Security Encryption (ASE).
!!!

### Application-Level Encryption

The encryption engine resides at the application that is utilizing the database.

Used with:

- Database encryption
- Object storage encryption
- Proxy encryption

Provides *protection* from:

- Application-level attacks
- Hardware loss
- Compromised database and administrative accounts

!!!
Application-level encryption involves encryption the data *before* it enters the fields of the database; it is much more difficult to search and review data that has been encrypted, so this reduces the functionality of the database.
!!!
