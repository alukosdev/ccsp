---
categories: [Standards, Auditing and Assurance Standards]
tags: [nist]
---

# NIST FIPS 140-3

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
CST | Cryptographic and Security Testing
CMVP | Cryptographic Module Validation Program
FIPS | Federal Information Processing Standard
NIST | National Institute of Standards and Technology
NVLAP |	National Voluntary Laboratory Accreditation Program
SBU | Sensitive But Unclassified

## Overview

A federal standard for accrediting and distinguishing secure and well-architected cryptographic modules produced by private sector vendors who seek to or are in the process of having their solutions and services certified for use in U.S. government departments and regulated industries (this includes financial services and healthcare) that collect, store, transfer, or share data that is deemed to be "sensitive" but not classified (i.e., Secret/Top Secret).

FIPS 140 Publication Series was issued by NIST to coordinate the requirements and standards for cryptography modules covering both hardware and software components for cloud and traditional computing environments.

The primary goal for the FIPS 140-3 standard is to accredit and distinguish secure and well-architected cryptographic modules produced by private sector vendors who seek to or are in the process of having their solutions and services certified for us in U.S. government departments and regulated industries that collect, store, transfer, or share data that is deemed to be sensitive but not classified.

!!!
FIPS 140-3 is *only* for sensitive but unclassified (SBU) data.
!!!

FIPS 140-3 is essentially just a list of approved cryptosystems.

## Components

The FIPS 140-3 standard provides four distinct levels of qualitative security intended to cover a range of potential applications and environments with emphasis on secure design and implementation of a cryptographic module.

Includes **11 sections:**

- Cryptographic module specification
- Cryptographic module interfaces
- Roles, services, and authentication
- Software/firmware security
- Operating environment
- Physical security
- Non-invasive security
- Sensitive security parameter management
- Self-tests
- Life-cycle assurance
- Mitigation of other attacks

The CMVP validates cryptographic modules to FIPS 140-3 and other cryptography-based standards. The goal of the CMVP is to promote the use of validated cryptographic modules and provide federal agencies with a security metric to use in procuring equipment containing validated cryptographic modules. In the CMVP, vendors of cryptographic modules use independent, accredited CST laboratories to have their modules tested. NVLAP accredited laboratories perform cryptographic module compliance/conformance testing.

:::
Some important sections that were included in FIPS 140-2 but are no longer explicitly referenced in FIPS 140-3 include:

- Finite state model
- Cryptographic key management
- Electromagnetic interference/electromagnetic compatibility (EMI/EMC)
:::

### Security Level 1

Requires production-grade equipment and externally tested algorithms.

!!!
This is the lowest level of security.
!!!

### Security Level 2

Adds requirements for physical tamper-evidence and role-based authentication. Software implementations must run on an Operating System approved to Common Criteria at EAL2.

- Detection and tampering.

### Security Level 3

Adds requirements for physical tamper-resistance and identity-based authentication. There must also be physical or logical separation between the interfaces by which "critical security parameters" enter and leave the module. Private keys can only enter or leave in encrypted form.

- Prevention and Detection

### Security Level 4

This level makes the physical security requirements more stringent, requiring the ability to be tamper-active, erasing the contents of the device if it detects various forms of environmental attack.

!!!
This is the highest level of security.
!!!
