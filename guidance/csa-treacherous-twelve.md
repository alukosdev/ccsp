---
categories: [Cloud Computing Risk Management Guidance]
tags: [csa]
---

!!!warning
This page is currently being updated for the 2022 version of the CCSP.
!!!

:::banner
The following INSERTHERE are derived from the official [INSERTHERE](https://linkme) released on **Month Day, Year**.
:::

# CSA Treacherous Twelve

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| CSA | Cloud Security Alliance |

## Overview

The CSA Treacherous Twelve is a report of threats related specifically to cloud computing.

## Components

1. *Data Breaches*: If a multitenant cloud service database is not properly designed, a flaw in one client's application can allow an attacker access not only to that client's data but to every other client's data as well.
2. *Insufficient Identity, Credential and Access Management*
3. *Insecure Interfaces and APIs*: Cloud computing providers expose a set of software interfaces or APIs that customers use to manage and interact with cloud services. Provisioning, management, orchestration, and monitoring are all performed using these interfaces. The security and availability of general cloud services is dependent on the security of these basic APIs. From authentication and access control to encryption and activity monitoring, these interfaces must be designed to protect against both accidental and malicious attempts to circumvent policy.
4. *System Vulnerabilities*
5. *Account Hijacking*: If attackers gain access to your credentials, they can eavesdrop on your activities and transactions, manipulate data, return falsified information, and redirect your clients to illegitimate sites. Your account or service instances may become a new base for the attacker.
6. *Malicious Insiders*: European Organization for Nuclear Research (CERN) defines an insider threat as "A current or former employee, contractor, or other business partner who has or had authorized access to an organization's network, system, or data and intentionally exceeded or misused that access in a manner that negatively affected the confidentiality, integrity, or availability of the organization's information or information systems."
7. *Advanced Persistent Threats*
8. *Data Loss*: Any accidental deletion by the CSP, or worse, a physical catastrophe such as a fire or earthquake, can lead to the permanent loss of customers' data unless the provider takes adequate measures to back it up. Furthermore, the burden of avoiding data loss does not fall solely on the provider's shoulders. If a customer encrypts their data before uploading it to the cloud but loses the encryption key, the data is still lost.
9. *Insufficient Due Diligence*: Too many enterprise jump into the cloud without understanding the full scope of the undertaking. Without a complete understanding of the CSP environment, applications, or services being pushed to the cloud, and operational responsibilities such as incident response, encryption, and security monitoring, organizations are taking on unknown levels of risk in ways they may not even comprehend but that are a far departure from their current risks.
10. *buse and Nefarious Use of Cloud Services*: It might take an attacker years to crack an encryption key using his own limited hardware, but using an array of cloud servers, he might be able to crack it in minutes. Alternatively, he might use that array of cloud servers to stage a DDoS attack, serve malware, or distribute pirated software.
11. *Denial of Service*: By forcing the victim cloud service to consume inordinate amounts of finite system resources such as process power, memory, disk space, and network bandwidth, the attacker causes an intolerable system slowdown.
12. *Shared Technology Issues*: Whether it's the underlying components that make up this infrastructure that were not designed to offer strong isolation properties for a multitenant architecture (IaaS), redeployable platforms (PaaS), or multicustomer applications (SaaS), the threat of shared vulnerabilities exists in all delivery models. A defense-in-depth strategy is recommended and should include compute, storage, network, application and user security enforcement, and monitoring, whether the service model is IaaS, PaaS, or SaaS. The key is that a single vulnerability or misconfiguration can lead to compromise across an entire provider's cloud.
