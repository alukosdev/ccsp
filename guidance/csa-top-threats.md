---
categories: [Cloud Computing Risk Management Guidance]
icon: zap
tags: [csa]
---

!!!danger
This page is currently under revision.
!!!

:::banner
The following contents reflect information collected from the official [Top Threats to Cloud Computing](https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven){ target="_blank" } released on **June 6, 2022**.
:::

# CSA Top Threats

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| API | Application Programming Interface |
| APT | Advanced Persistent Threat |
| CSA | Cloud Security Alliance |

## Overview

<span id="rev1"></span>Top Threats is a working group established by the CSA that aims to provide organizations with an up-to-date, expert-informed understanding of cloud security risks, threats and vulnerabilities in order to make educated risk-management decisions regarding cloud adoption strategies.[[¹]](#ref1)

## Publications

The *Top Threats* reports traditionally aim to raise awareness of threats, vulnerabilities, and risks in the cloud. The reports reflect the current consensus among 
security experts in CSA community about the most significant security issues in the cloud, ranked in order of significance.

| Name | Release Date |
| - | - |
| [Pandemic Eleven](#pandemic-eleven) | 2022/06/06 |
| Egregious Eleven | 2019/08/06 |
| Treacherous Twelve | 2016/02/29 |
| Notorious Nine | 2013/02/24 |

### Pandemic Eleven

1. [Insufficient Identity, Credentials, Access, and Key Management](#1-insufficient-identity-credentials-access-and-key-management)
2. [Insecure Interfaces and APIs](#2-insecure-interfaces-and-apis)
3. [Misconfiguration and Inadequate Change Control](#3-misconfiguration-and-inadequate-change-control)
4. [Lack of Cloud Security Architecture and Strategy](#4-lack-of-cloud-security-architecture-and-strategy)
5. [Insecure Software Development](#5-insecure-software-development)
6. [Unsecured Third-Party Resources](#6-unsecured-third-party-resources)
7. [System Vulnerabilities](#7-system-vulnerabilities)
8. [Accidental Cloud Data Disclosure](#8-accidental-cloud-data-disclosure)
9. [Misconfiguration and Exploitation of Serverless and Container Workloads](#9-misconfiguration-and-exploitation-of-serverless-and-container-workloads)
10. [Organized Crime/Hackers/APT](#10-organized-crime-hackers-apt)
11. [Cloud Storage Data Exfiltration](#11-cloud-storage-data-exfiltration)

==- 1. Insufficient Identity, Credentials, Access, and Key Management
> Text below this needs to be cited.

Identity, credential, access management systems include tools and policies that allow organizations to manage, monitor, and secure access to valuable resources. Examples may include electronic files, computer systems, and physical resources, such as server rooms or buildings.

- Negative business performance and productivity due to reactive and overly restrictive lockdowns
- Employee testing fatigue resulting in a lack of compliance and apathy to security
- Data replacement or corruption vs. exfiltration by unauthorized or malicious users
- Loss of trust and revenue in the market
- Financial expenses incurred due to incident response and forensics
- Ransomware and supply chain disruption

!!!
This threat aligns with the Disclosure category of the STRIDE threat model.
!!!

!!!danger
This was taken from account hijacking.
!!!

If attackers gain access to your credentials, they can eavesdrop on your activities and transactions, manipulate data, return falsified information, and redirect your clients to illegitimate sites. Your account or service instances may become a new base for the attacker.
==- 2. Insecure Interfaces and APIs
> Text below this needs to be cited.

API usage continues to grow in popularity; securing these interfaces has become paramount. APIs and microservices must be checked for vulnerabilities due to misconfiguration, poor coding practices, a lack of authentication and inappropriate authorization. These oversights can potentially leave the interfaces vulnerable to malicious activity. Common examples include 1. Unauthenticated endpoints; 2. Weak authentication; 3. Excessive permissions; 4. Standard security controls disabled; 5. Unpatched systems; 6. Logical design issues; and 7. 
Disabled logging or monitoring. Misconfiguration of APIs and other interfaces is a leading cause of incidents and data breaches. These could allow exfiltration, deletion or modification of resources, data adjustments, or service interruptions.

The risk of an insecure interface or API varies depending on the usage and data associated with the API, as well as how quickly the vulnerability is detected and mitigated.

The most commonly reported business impact is the unintended exposure of sensitive or private data left unsecured by the API.

!!!danger
The following definition was copied from previous notes. References need to be identified.
!!!

Cloud computing providers expose a set of software interfaces or APIs that customers use to manage and interact with cloud services. Provisioning, management, orchestration, and monitoring are all performed using these interfaces. The security and availability of general cloud services is dependent on the security of these basic APIs. From authentication and access control to encryption and activity monitoring, these interfaces must be designed to protect against both accidental and malicious attempts to circumvent policy.
==- 3. Misconfiguration and Inadequate Change Control
> Text below this needs to be cited.
==- 4. Lack of Cloud Security Architecture and Strategy
> Text below this needs to be cited.

!!!danger
Was this formerly shared technology issues? That's what I added below.
!!!

Whether it's the underlying components that make up this infrastructure that were not designed to offer strong isolation properties for a multitenant architecture (IaaS), redeployable platforms (PaaS), or multicustomer applications (SaaS), the threat of shared vulnerabilities exists in all delivery models. A defense-in-depth strategy is recommended and should include compute, storage, network, application and user security enforcement, and monitoring, whether the service model is IaaS, PaaS, or SaaS. The key is that a single vulnerability or misconfiguration can lead to compromise across an entire provider's cloud.
==- 5. Insecure Software Development
> Text below this needs to be cited.
==- 6. Unsecured Third-Party Resources
> Text below this needs to be cited.

!!!danger
This was taken from insufficient due diligence.
!!!

Too many enterprise jump into the cloud without understanding the full scope of the undertaking. Without a complete understanding of the CSP environment, applications, or services being pushed to the cloud, and operational responsibilities such as incident response, encryption, and security monitoring, organizations are taking on unknown levels of risk in ways they may not even comprehend but that are a far departure from their current risks.
==- 7. System Vulnerabilities
> Text below this needs to be cited.

!!!danger
This was taken from denial of service.
!!!

By forcing the victim cloud service to consume inordinate amounts of finite system resources such as process power, memory, disk space, and network bandwidth, the attacker causes an intolerable system slowdown.
==- 8. Accidental Cloud Data Disclosure
> Text below this needs to be cited.

!!!danger
This was just a piece of data breaches from the T12.
!!!

If a multitenant cloud service database is not properly designed, a flaw in one client's application can allow an attacker access not only to that client's data but to every other client's data as well.
==- 9. Misconfiguration and Exploitation of Serverless and Container Workloads
> Text below this needs to be cited.
==- 10. Organized Crime/Hackers/APT
> Text below this needs to be cited.

!!!danger
I believe this was formerly abuse and nefarious use of cloud services.
!!!

It might take an attacker years to crack an encryption key using his own limited hardware, but using an array of cloud servers, he might be able to crack it in minutes. Alternatively, he might use that array of cloud servers to stage a DDoS attack, serve malware, or distribute pirated software.
==- 11. Cloud Storage Data Exfiltration
> Text below this needs to be cited.
==-

## Noteworthy

- [x] The security issues contained within the CSA *Top Threats* reports are specifically related to *cloud computing*.
- [x] The most current version of the CSA *Top Threats* report is known as the *Pandemic Eleven*.

## References

1. <span id="ref1"></span>[⌃](#rev1) CSA. (n.d.). *Top Threats Working Group*. https://cloudsecurityalliance.org/research/working-groups/top-threats

## Sources

- CSA. (2022, June 6). *Top Threats to Cloud Computing*. https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven