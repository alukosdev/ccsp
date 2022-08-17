# Data Dispersion

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| AONT-RS | All-or-Nothing-Transform with Reed-Solomon |
| SMSS | Secret Sharing Made Short |

## Overview

Data dispersion is a technique that is commonly used to improve data security, but without the use of encryption mechanisms.

- Bit splitting
- Erasure coding

If the data is static (doesn't change), creating and distributing the data is a one-time cost. If the data is dynamic (continually changing), the erasure codes have to be re-created and the resulting data blocks redistributed.

Data dispersion is much like traditional RAID technologies; spreading the data across different storage areas and potentially different cloud providers spread across geographic boundaries. However, this comes with inherent risk. If data is spread across multiple cloud providers, there is a possibility that an outage at one provider will make the dataset unavailable to users, regardless of location. This would be a threat to availability, depending on the implementation.

## Components

### Bit Splitting

Bit splitting is like adding encryption to RAID. The data is first encrypted, then separated into pieces, and the pieces are distributed across several storage areas.

Bit splitting carries the following disadvantages:

- Processing is CPU intensive
- Availability concerns; all parts of the data need to be available to decrypt and use the information
- Storage requirements and costs are higher than other storage systems

Bit splitting can use different encryption methods, a large percentage of which are based on two secret sharing cryptographic algorithms:

==- SMSS
SMSS uses a three-phase process:

- Encryption of information
- Use of information dispersal algorithm
- Splitting the encryption key using the secret sharing algorithm

The different fragments of data and encryption keys are then signed and distributed to different cloud storage services. This makes it impossible to decrypt without both arbitrarily chosen data and encryption key fragments.
==- AONT-RS
AONT-RS integrates the AONT and erasure coding. This method first encrypts and transforms the information and the encryption key into blocks in a way that the information cannot be recovered without using all the blocks, and then it uses the IDA to split the blocks into shares that are distributed to different cloud storage services (similar to SMSS).

An AONT is an encryption mode which allows the data to be understood only if all of it is known.

!!!
Depending on how the system is implemented, some or all of the data set is required to be available to unencrypt and read the data.
!!!
==-

### Erasure Coding

Erasure coding is like using parity bits for RAID striping; in RAID, parity bits help you recover missing data if one striped drive gets lost. Erasure coding helps you recover missing data if a cloud data are is unavailable/lost while your data is dispersed.

Erasure coding is a method of data protection in which data is broken into fragments that are expanded and encoded with a configurable number of redundant pieces of data and stored across different locations such as disks, storage nodes, or geographical locations. This allows for the failure of 2 or more elements of a storage array, thus offering more protection than RAID. This is commonly referred to as *chunking*. When encryption is used, this is referred to as *sharding*.

!!!
Erasure coding is good for latency tolerant, large capacity stores and is generally found in the context of object storage with very large volume-cloud operators.
!!!
