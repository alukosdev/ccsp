---
categories: [Cloud Computing Risk Management Guidance]
tags: [csa]
---

!!!warning
This page is currently under active revision.
!!!

:::banner
The following contents are derived from the official [Top Threats to Cloud Computing](https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven) released on **June 6, 2022**.
:::

# CSA Top Threats

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| API | Application Programming Interface |
| APT | Advanced Persistent Threat |
| CSA | Cloud Security Alliance |

## Overview

Top Threats is a working group established by the CSA that aims to provide organizations with an up-to-date, expert-informed understanding of cloud security risks, threats and vulnerabilities in order to make educated risk-management decisions regarding cloud adoption strategies.[[¹]](#ref1)

## Publications

The *Top Threats* reports traditionally aim to raise awareness of threats, vulnerabilities, and risks in the cloud.[[²]](#ref2)

!!!
The security issues contained within these reports are specifically related to *cloud computing*.
!!!

| Name | Release Date |
| - | - |
| Pandemic Eleven | 2022/06/06 |
| Egregious Eleven | 2019/08/06 |
| Treacherous Twelve | 2016/02/29 |
| Notorious Nine | 2013/02/24 |

### Pandemic Eleven

The latest report highlights the Pandemic Eleven (ranked in order of significance per a survey of over 700 industry experts on security issues in the cloud industry). Also shown are the 2019 survey rankings in parentheses:

1. [Insufficient Identity, Credentials, Access, and Key Management](#insufficient-identity-credentials-access-and-key-management) (4)
2. [Insecure Interfaces and APIs](#insecure-interfaces-and-apis) (7)
3. [Misconfiguration and Inadequate Change Control](#misconfiguration-and-inadequate-change-control) (2)
4. [Lack of Cloud Security Architecture and Strategy](#lack-of-cloud-security-architecture-and-strategy) (3)
5. [Insecure Software Development](#insecure-software-development)
6. [Unsecured Third-Party Resources](#unsecured-third-party-resources)
7. [System Vulnerabilities](#system-vulnerabilities) (8)
8. [Accidental Cloud Data Disclosure](#accidental-cloud-data-disclosure)
9. [Misconfiguration and Exploitation of Serverless and Container Workloads](#misconfiguration-and-exploitation-of-serverless-and-container-workloads)
10. [Organized Crime/Hackers/APT](#organized-crime-hackers-apt) (11)
11. [Cloud Storage Data Exfiltration](#cloud-storage-data-exfiltration)

==- Insufficient Identity, Credentials, Access, and Key Management
Identity, credential, access management systems include tools and policies that allow organizations to manage, monitor, and secure access to valuable resources. Examples may include electronic files, computer systems, and physical resources, such as server rooms or buildings.

- Negative business performance and productivity due to reactive and overly restrictive lockdowns
- Employee testing fatigue resulting in a lack of compliance and apathy to security
- Data replacement or corruption vs. exfiltration by unauthorized or malicious users
- Loss of trust and revenue in the market
- Financial expenses incurred due to incident response and forensics
- Ransomware and supply chain disruption

!!!danger
This was taken from account hijacking.
!!!

If attackers gain access to your credentials, they can eavesdrop on your activities and transactions, manipulate data, return falsified information, and redirect your clients to illegitimate sites. Your account or service instances may become a new base for the attacker.
==- Insecure Interfaces and APIs
API usage continues to grow in popularity; securing these interfaces has become paramount. APIs and microservices must be checked for vulnerabilities due to misconfiguration, poor coding practices, a lack of authentication and inappropriate authorization. These oversights can potentially leave the interfaces vulnerable to malicious activity. Common examples include 1. Unauthenticated endpoints; 2. Weak authentication; 3. Excessive permissions; 4. Standard security controls disabled; 5. Unpatched systems; 6. Logical design issues; and 7. 
Disabled logging or monitoring. Misconfiguration of APIs and other interfaces is a leading cause of incidents and data breaches. These could allow exfiltration, deletion or modification of resources, data adjustments, or service interruptions.

The risk of an insecure interface or API varies depending on the usage and data associated with the API, as well as how quickly the vulnerability is detected and mitigated.

The most commonly reported business impact is the unintended exposure of sensitive or private data left unsecured by the API.

!!!danger
The following definition was copied from previous notes. References need to be identified.
!!!

Cloud computing providers expose a set of software interfaces or APIs that customers use to manage and interact with cloud services. Provisioning, management, orchestration, and monitoring are all performed using these interfaces. The security and availability of general cloud services is dependent on the security of these basic APIs. From authentication and access control to encryption and activity monitoring, these interfaces must be designed to protect against both accidental and malicious attempts to circumvent policy.
==- Misconfiguration and Inadequate Change Control
3
==- Lack of Cloud Security Architecture and Strategy
!!!danger
Was this formerly shared technology issues? That's what I added below.
!!!

Whether it's the underlying components that make up this infrastructure that were not designed to offer strong isolation properties for a multitenant architecture (IaaS), redeployable platforms (PaaS), or multicustomer applications (SaaS), the threat of shared vulnerabilities exists in all delivery models. A defense-in-depth strategy is recommended and should include compute, storage, network, application and user security enforcement, and monitoring, whether the service model is IaaS, PaaS, or SaaS. The key is that a single vulnerability or misconfiguration can lead to compromise across an entire provider's cloud.
==- Insecure Software Development
5
==- Unsecured Third-Party Resources
!!!danger
This was taken from insufficient due diligence.
!!!

Too many enterprise jump into the cloud without understanding the full scope of the undertaking. Without a complete understanding of the CSP environment, applications, or services being pushed to the cloud, and operational responsibilities such as incident response, encryption, and security monitoring, organizations are taking on unknown levels of risk in ways they may not even comprehend but that are a far departure from their current risks.
==- System Vulnerabilities
!!!danger
This was taken from denial of service.
!!!

By forcing the victim cloud service to consume inordinate amounts of finite system resources such as process power, memory, disk space, and network bandwidth, the attacker causes an intolerable system slowdown.
==- Accidental Cloud Data Disclosure
!!!danger
This was just a piece of data breaches from the T12.
!!!

If a multitenant cloud service database is not properly designed, a flaw in one client's application can allow an attacker access not only to that client's data but to every other client's data as well.
==- Misconfiguration and Exploitation of Serverless and Container Workloads
9
==- Organized Crime/Hackers/APT
!!!danger
I believe this was formerly abuse and nefarious use of cloud services.
!!!

It might take an attacker years to crack an encryption key using his own limited hardware, but using an array of cloud servers, he might be able to crack it in minutes. Alternatively, he might use that array of cloud servers to stage a DDoS attack, serve malware, or distribute pirated software.
==- Cloud Storage Data Exfiltration
11
==-

==- Malicious Insiders
!!!danger
This was #6 on T12.
!!!

European Organization for Nuclear Research (CERN) defines an insider threat as "A current or former employee, contractor, or other business partner who has or had authorized access to an organization's network, system, or data and intentionally exceeded or misused that access in a manner that negatively affected the confidentiality, integrity, or availability of the organization's information or information systems."
==- Data Loss
!!!danger
This was #8 on T12.
!!!

Any accidental deletion by the CSP, or worse, a physical catastrophe such as a fire or earthquake, can lead to the permanent loss of customers' data unless the provider takes adequate measures to back it up. Furthermore, the burden of avoiding data loss does not fall solely on the provider's shoulders. If a customer encrypts their data before uploading it to the cloud but loses the encryption key, the data is still lost.
==-

## References

1. https://cloudsecurityalliance.org/research/working-groups/top-threats<span id="ref1"></span>
2. https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven<span id="ref2"></span>

## Sources

- Cloud Security Alliance. (2022, June 6). Top Threats to Cloud Computing [PDF file]. https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven