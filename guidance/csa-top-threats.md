---
categories: [Cloud Computing Risk Management Guidance]
tags: [csa]
---

:::banner
The following page reflects information collected from the official [Top Threats to Cloud Computing](https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven){ target="_blank" } released on **June 6, 2022**.
:::

# CSA Top Threats

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
API | Application Programming Interface
APT | Advanced Persistent Threat
CSA | Cloud Security Alliance
CSP | Cloud Service Provider
IaC | Infrastructure as Cloud
IAM | Identity and Access Management
IP | Intellectual Property
PHI | Personal Health Information
PII | Personally Identifiable Information
SaaS | Software-as-a-Service
TTP | Tactics, Techniques, and Procedures

## Overview

<span id="rev1"></span>Top Threats is a working group established by the CSA that aims to provide organizations with an up-to-date, expert-informed understanding of cloud security risks, threats and vulnerabilities in order to make educated risk-management decisions regarding cloud adoption strategies.[[1]](#ref1)

## Publications

The *Top Threats* reports traditionally aim to raise awareness of threats, vulnerabilities, and risks in the cloud. The reports reflect the current consensus among 
security experts in CSA community about the most significant security issues in the cloud, ranked in order of significance.

Name | Release Date
:--- | :---
[Pandemic Eleven](#pandemic-eleven) | 2022/06/06
Egregious Eleven | 2019/08/06
Treacherous Twelve | 2016/02/29
Notorious Nine | 2013/02/24

### Pandemic Eleven

- Security Issue 1: [Insufficient Identity, Credentials, Access, and Key Management](#1-insufficient-identity-credentials-access-and-key-management)
- Security Issue 2: [Insecure Interfaces and APIs](#2-insecure-interfaces-and-apis)
- Security Issue 3: [Misconfiguration and Inadequate Change Control](#3-misconfiguration-and-inadequate-change-control)
- Security Issue 4: [Lack of Cloud Security Architecture and Strategy](#4-lack-of-cloud-security-architecture-and-strategy)
- Security Issue 5: [Insecure Software Development](#5-insecure-software-development)
- Security Issue 6: [Unsecured Third-Party Resources](#6-unsecured-third-party-resources)
- Security Issue 7: [System Vulnerabilities](#7-system-vulnerabilities)
- Security Issue 8: [Accidental Cloud Data Disclosure](#8-accidental-cloud-data-disclosure)
- Security Issue 9: [Misconfiguration and Exploitation of Serverless and Container Workloads](#9-misconfiguration-and-exploitation-of-serverless-and-container-workloads)
- Security Issue 10: [Organized Crime/Hackers/APT](#10-organized-crime-hackers-apt)
- Security Issue 11: [Cloud Storage Data Exfiltration](#11-cloud-storage-data-exfiltration)


1. Security Issue 1: [Insufficient Identity, Credentials, Access, and Key Management](#1-insufficient-identity-credentials-access-and-key-management)
2. Security Issue 2: [Insecure Interfaces and APIs](#2-insecure-interfaces-and-apis)
3. Security Issue 3: [Misconfiguration and Inadequate Change Control](#3-misconfiguration-and-inadequate-change-control)
4. Security Issue 4: [Lack of Cloud Security Architecture and Strategy](#4-lack-of-cloud-security-architecture-and-strategy)
5. Security Issue 5: [Insecure Software Development](#5-insecure-software-development)
6. Security Issue 6: [Unsecured Third-Party Resources](#6-unsecured-third-party-resources)
7. Security Issue 7: [System Vulnerabilities](#7-system-vulnerabilities)
8. Security Issue 8: [Accidental Cloud Data Disclosure](#8-accidental-cloud-data-disclosure)
9. Security Issue 9: [Misconfiguration and Exploitation of Serverless and Container Workloads](#9-misconfiguration-and-exploitation-of-serverless-and-container-workloads)
10. Security Issue 10: [Organized Crime/Hackers/APT](#10-organized-crime-hackers-apt)
11. Security Issue 11: [Cloud Storage Data Exfiltration](#11-cloud-storage-data-exfiltration)

==- 1. Insufficient Identity, Credentials, Access, and Key Management

Identity, credential, access management systems include tools and policies that allow organizations to manage, monitor, and secure access to valuable resources. Examples may include electronic files, computer systems, and physical resources, such as server rooms or buildings.

Proper maintenance and ongoing vigilance are important. The use of risk-scoring in Identity and Access Management (IAM) enhances security posture. Using a clear risk assignment model, diligent monitoring, and proper isolation of its behavior can help cross-check IAM systems. Tracking target access and frequency for risk scoring are also critical to understanding risk context.

Privileged accounts must be deprovisioned in a precise and immediate manner in order to avoid personnel access after offboarding or role change. This reduces the data exfiltration or the likelihood of compromise. Outside of deprovisioning privileged accounts, it is imperative that roles and responsibilities match the level of "need to know". Multiple over-privileged personnel create a higher likelihood of data mismanagement or account takeover.

==- 2. Insecure Interfaces and APIs

API usage continues to grow in popularity; securing these interfaces has become paramount. APIs and microservices must be checked for vulnerabilities due to misconfiguration, poor coding practices, a lack of authentication and inappropriate authorization. These oversights can potentially leave the interfaces vulnerable to malicious activity. Common examples include:

1. Unauthenticated endpoints
2. Weak authentication
3. Excessive permissions
4. Standard security controls disabled
5. Unpatched systems
6. Logical design issues
7. Disabled logging or monitoring.

Misconfiguration of APIs and other interfaces is a leading cause of incidents and data breaches. These could allow exfiltration, deletion or modification of resources, data 
adjustments, or service interruptions.

==- 3. Misconfiguration and Inadequate Change Control

Misconfigurations are the incorrect or sub-optimal setup of computing assets that may leave them vulnerable to unintended damage or external/internal malicious activity. Lack of system knowledge or understanding of security settings and nefarious intentions can result in misconfigurations. Some common misconfigurations are:

1. Unsecured data storage elements or containers
2. Excessive permissions
3. Default credentials and configuration settings are left unchanged
4. Standard security controls disabled
5. Unpatched systems
6. Logging or monitoring disabled
7. Unrestricted access to ports and services
8. Unsecured Secrets Management
9. Poorly configured or lack of configuration validation.

Misconfiguration of cloud resources is a leading cause of data breaches and could allow deletion or modification of resources and service interruptions.

==- 4. Lack of Cloud Security Architecture and Strategy

Cloud security strategy and security architecture encompasses the consideration and selection of cloud deployment models, cloud service models, cloud service providers (CSPs), service region availability zone, specific cloud services, general principles, and pre-determinations. Furthermore, a forward-looking design of IAM, networking and security controls across different cloud accounts, vendors, services, and environments are in scope. Consideration of strategy should precede and dictate design, but it is common that cloud 
challenges demand an incremental and agile approach to planning.

==- 5. Insecure Software Development

Software is complex, with cloud technologies tending to add to the complexity. In that complexity, unintended functionality emerges which could allow for the creation of exploits and likely misconfigurations. Thanks to the accessibility of the cloud, threat actors can leverage these "features" more easily than ever before.

==- 6. Unsecured Third-Party Resources

In a world where cloud computing adoption is increasing rapidly, a third-party resource could mean different things: from open source code, through SaaS products and API risks (Security Issue 2), and all the way to a managed service provided by a cloud vendor. Risks stemming from third-party resources are also considered supply chain vulnerabilities since they are a part of the process of delivering your products or services. These risks exist in every product and service consumed. Still, due to the increasing reliance on third-party services and software-based products in recent years, more exploits of these vulnerabilities and hackable configurations occur.

==- 7. System Vulnerabilities

System vulnerabilities are flaws in cloud service platforms. They may be exploited in an attempt to compromise confidentiality, integrity, and availability of data, potentially disrupting service operations. All components can contain vulnerabilities that may leave cloud services open to attack. Implementing security hardening practices that align 
with the below vulnerability categories is essential to mitigating their security risks.

There are four main categories of system vulnerabilities:

1. Zero-day vulnerabilities
2. Missing security patches
3. Configuration-based vulnerabilities
4. Weak or default credentials

==- 8. Accidental Cloud Data Disclosure

Cloud services enable companies to build, innovate, and scale at a pace never seen before. However, the complexity of the cloud and a shift to cloud-service ownership, with diverse teams and business units, often leads to a lack of security governance and control. Increasing numbers of configurations for cloud resources in different CSPs make misconfigurations more common, and the lack of transparency into cloud inventory and adequate network exposure can lead to unintentional data leaks.

==- 9. Misconfiguration and Exploitation of Serverless and Container Workloads

The migration to cloud infrastructure and adoption of DevOps practices enable IT teams to deliver value to the business faster than ever. Managing and scaling the infrastructure and security controls to run applications is still a significant burden on development teams. Legacy infrastructure teams used to managing on-prem environments must learn new skills like Infrastructure as Code (IaC) and cloud security. The same teams must take on more responsibility for the network and security controls supporting their applications. Serverless and cloud-native containerized workloads can seem like a silver bullet for this problem, offloading that responsibility to the cloud service provider (CSP). Still, it requires a higher level of cloud and application security maturity than migrating virtual machines to the cloud.

==- 10. Organized Crime/Hackers/APT

Advanced persistent threats (APTs) is a broad term used to describe an attack campaign in which an intruder, or team of intruders, establishes an illicit, long-term presence on a network to mine highly sensitive data. These teams may include nationstates as well as organized criminal gangs. The term Organized Crime is meant as a means to describe the manner in which the level of organization a group would have when creating planned and rational acts that reflect the efforts of group individuals. APTs have established sophisticated tactics, techniques, and protocols (TTPs) to infiltrate their targets. It is not uncommon for APT groups to spend months undetected in a target network. This extended time allows them to move laterally towards highly sensitive business data or assets. Some APT groups have historically also favored particular industries or organizations. For example, APT33 has been attributed to threat actors based out of Iran. They have historically targeted the energy and aviation sector. APT groups have various motivations to carry out malicious activities, such as political or economic.

==- 11. Cloud Storage Data Exfiltration

Cloud storage data exfiltration is an incident involving sensitive, protected, or confidential information. These data may be released, viewed, stolen, or used by an individual outside of the organization's operating environment. Data exfiltration may be the primary objective of a targeted attack and may result from an exploited vulnerability or 
misconfiguration, application vulnerabilities, or poor security practice. Exfiltration may involve any kind of information that was not intended for public release, for example, personal health information (PHI), financial information, personally identifiable information (PII), trade secrets, and intellectual property (IP).

==-

## Noteworthy

- [x] The security issues contained within the CSA *Top Threats* reports are specifically related to *cloud computing*.
- [x] The most current version of the CSA *Top Threats* report is known as the *Pandemic Eleven*.

## References

1. <span id="ref1"></span>[⌃](#rev1) CSA. (n.d.). *Top Threats Working Group*. https://cloudsecurityalliance.org/research/working-groups/top-threats

## Sources

- CSA. (2022, June 6). *Top Threats to Cloud Computing Pandemic Eleven*. https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven