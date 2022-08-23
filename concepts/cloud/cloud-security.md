---
icon: stop
---

!!!danger
This page has not yet been revised for 2022.
!!!

# Cloud Security

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
API | Application Programming Interface
DAM | Database Activity Monitoring
FAM | File Activity Monitoring
WAF | Web Application Firewall

## Glossary

=== API Gateway
An API gateway translates requests from clients into multiple requests to many microservices and delivers the content as a whole via an API it assigns to that client/session.

API gateways can provide access control, rate limiting, logging, metrics, and security filtering services.
=== Database Activity Monitoring (DAM)
Captures and records, at a minimum, all SQL activity in real time or near real time, including database administrator activity, across multiple database platforms; and can generate alerts on policy violations.

A DAM operates at layer 7 of the OSI model.
=== File Activity Monitoring (FAM)
FAM monitors and records all activity within designated file repositories at the user level, and generate alerts on policy violations.
=== Honeynet
Grouping multiple honeypot systems to form a network that is used in the same manner as the honeypot, but with more scalability and functionality.
=== Honeypot
Honeypots are computer systems setup to look like production systems using the modern concept of deception. They contain an operating system and can mimic many common systems such as Apache or IIS web servers, Windows file shares, or Cisco routers. A honeypot could be deployed with a known vulnerability that an attacker would be enticed to exploit. While it appears vulnerable to attack, it is in fact protection the real systems from attack while gathering defensive information such as the attacker's identity, access, and compromise methods.

Used to detect, deflect, or in some manner counteract attempts at unauthorized use of information systems.

Enticement vs. entrapment. The real term to be used should be "distract".
=== Web Application Firewall (WAF)
A WAF is a type of firewall that filters HTTP traffic and can help prevent DoS attacks.

A WAF operates at layer 7 of the OSI model.
=== XML Gateway
XML gateways transform how services and sensitive data are exposed as APIs to developers, mobile users, and the cloud. They can be either hardware or software based and they can implement security controls such as DLP, antivirus, and antimalware. XML gateways can also act as a reverse proxy and perform content inspection on many traffic protocols, including SFTP.
===

### Associated Standards

In the absence of cloud-specific security standards that are universally accepted by providers and customers alike, you'll deal with a patchwork of security standards, frameworks, and controls that are being applied to cloud environments.

| Standard | Description |
| - | - |
| ISO/IEC 27001 | Information security management systems |
| ISO/IEC 27002 | Code of practice for information security controls |
| ISO/IEC 27017 | Code of practice for information security controls based on ISO/IEC 27002 for cloud services |
| NIST SP 800-53 | Security and Privacy Controls for Federal Information Systems and Organizations |

## Overview

Enterprise security architecture provides the conceptual design of network security infrastructure and related security mechanisms, policies, and procedures. It links components of the security infrastructure as a cohesive unit with the goal of protecting corporate information.

The following principles should be adhered to at all times:

- Define protections that enable trust in the cloud.
- Develop cross-platform capabilities and patterns for proprietary and open source providers.
- Facilitate trusted and efficient access, administration, and resiliency to the customer or consumer.
- Provide direction to secure information that is protected by regulations.
- Facilitate proper and efficient identification, authentication, authorization, administration, and auditability.
- Centralize security policy, maintenance operation, and oversight functions.
- Make access to information both secure and easy to obtain.
- Delegate or federate access control where appropriate.
- Ensure ease of adoption and consumption, supporting the design of security patterns.
- Make the architecture elastic, flexible, and resilient, supporting multitenant, multilandlord platforms.
- Ensure the architecture addresses and supports multiple levels of protection, including network, OS, and application security needs.

## Supplemental Security Devices

- Generic firewall
- Web application firewall (layer 7)
- Database activity monitoring (detect and stop malicious commands)
- A DAM can determine if malicious commands are being executed on your organization's SQL server and can prevent them from being executed.
- Deception technology
- API gateways (access control, rate limiting, logging, metrics, and security filtering)
- XML gateways (DLP, AV, antimalware)
- IPS/IDS (host-based, network-based; signature, anomaly, stateful)

## DNSSEC

DNSSEC is a suite of extensions that adds security to the DNS protocol by enabling DNS response validation using a process called zone signing.

Specifically, DNSSEC provides:

- Origin authority
- Data integrity
- Authenticated denial of existence

With DNSSEC, the DNS protocol is much less susceptible to certain types of attacks:

- Cache poisoning/spoofing
- Pharming
- MITM

DNSSEC uses digital signatures embedded in the data. The DNSSEC digital signature verifies you are communicating with the site you intended to visit (authenticity). DNSSEC puts additional records in DNS alongside existing records. The new record types, such as RRSIG and DNSKEY, can be accessed the same way as common records such as A, CNAME, and MX. A public and private key will exist for each zone. When a request is made, the request include information signed with a private key; the recipient then unlocks it with the public key.

!!!
It's important to note that while DNSSEC uses cryptopgraphy, it does not provide nor perform encryption.
!!!

DNSSEC does not protect against:

- Confidentiality
- DDoS

### Components

==- Zone Signing Key
Used to sign and validate the individual record sets within the zone.
==- Key Signing Key
Used to sign the DNSKEY records in the zone.
==-
