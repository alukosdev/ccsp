---
categories: [Application Risk Management Guidance]
icon: zap
tags: [owasp]
---

!!!danger
This page is currently under revision.
!!!

:::banner
The following contents reflect information collected from the official [OWASP Top 10](https://owasp.org/www-project-top-ten){ target="_blank" } released in **2021**.
:::

# OWASP Top 10

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| ACL | Access Control List |
| CSRF | Cross-Site Request Forgery |
| CWE | Common Weakness Enumeration |
| OWASP | Open Web Application Security Project |
| SSRF | Server-Side Request Forgery |
| XML | Extensible Markup Language |
| XSS | Cross-Site Scripting |
| XXE | XML External Entities |

## Overview

The OWASP Top 10 is a standard awareness document for developers and web application security. It represents a broad consensus about the most critical security risks to web applications.

## Publications

+++ Top 10:2021
1. [Broken Access Control](#broken-access-control)
2. [Cryptographic Failures](#cryptographic-failures)
3. [Injection](#injection)
4. [Insecure Design](#insecure-design)
5. [Security Misconfiguration](#security-misconfiguration)
6. [Vulnerable and Outdated Components](#vulnerable-and-outdated-components)
7. [Identification and Authentication Failures](#identification-and-authentication-failures)
8. [Software and Data Integrity Failures](#software-and-data-integrity-failures)
9. [Security Logging and Monitoring Failures](#security-logging-and-monitoring-failures)
10. [Server-Side Request Forgery (SSRF)](#server-side-request-forgery-ssrf)
+++ Top 10:2017
1. [Injection](#injection)
2. [Broken Authentication](#broken-authentication)
3. [Sensitive Data Exposure](#sensitive-data-exposure)
4. [XML External Entities (XXE)](#xml-external-entities-xxe)
5. [Broken Access Control](#broken-access-control)
6. [Security Misconfiguration](#security-misconfiguration)
7. [Cross-Site Scripting (XSS)](#cross-site-scripting-xss)
8. [Insecure Deserialization](#insecure-deserialization)
9. [Using Components with Known Vulnerabilities](#using-components-with-known-vulnerabilities)
10. [Insufficient Logging and Monitoring](#insufficient-logging-and-monitoring)

## Web Application Security Risks

!!!
To address these risks, organizations must have an application risk management program in place. Implementation of an application risk management program addresses not only vulnerabilities but also all risks associated with applications.
!!!

==- Broken Access Control
<span id="rev1"></span>Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits.[[¹]](#ref1)

+++ Notable CWEs
- CWE-200: Exposure of Sensitive Information to an Unauthorized Actor
- CWE-201: Insertion of Sensitive Information Into Sent Data
- CWE-352: Cross-Site Request Forgery
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 1 |
| Top 10:2017 | :white_check_mark: | 5 |

!!!
This risk was merged in 2017 from *Insecure Direct Object References* and *Missing Function Level Access Control*.
!!!
==- Broken Authentication
!!!
In 2021, this risk was renamed to [Identification and Authentication Failures](#identification-and-authentication-failures).
!!!

+++ Notable CWEs
- CWE-256: Plaintext Storage of a Password
- CWE-308: Use of Single-factor Authentication
- CWE-523: Unprotected Transport of Credentials
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 2 |

> Text below this needs to be cited.

Occurs when authentication and session management application functions are not implemented correctly.

+++ Impact
- Allows attackers to compromise passwords, keys, or session tokens
- Exploitation of other implementation flaws to assume other identities
+++ Prevention
- Do not use custom authentication schemes.
- Rotate session IDs after a successful login.
- Do not allow simple passwords to be used.
- Ensure the connection is encrypted so credentials aren't exposed.
+++
==- Cross-Site Scripting (XSS)
!!!
In 2021, this risk was merged with and renamed to [Injection](#injection).
!!!

+++ Notable CWEs
- CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 7 |

> Text below this needs to be cited.

Occurs when an application receives untrusted data and then sends it to a web browser without proper validation.

+++ Impact
- Allows attackers to execute scripts in a victim's browser which can hijack user sessions, deface websites, or redirect the user to malicious websites.
+++ Prevention
- Use an auto-escaping template system
- Put untrusted data in only allowed slots of HTML documents
- HTML escape when including untrusted data in any HTML elements
- Use the attribute escape when including untrusted data in attribute elements
- Sanitize HTML markup with a library designed for the purpose
+++

This is not a threat to the back-end database, but a threat to the client.
==- Cryptographic Failures

+++ Notable CWEs
- CWE-259: Use of Hard-coded Password
- CWE-327: Broken or Risky Crypto Algorithm
- CWE-331: Insufficient Entropy
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 2 |
| Top 10:2017 | :white_check_mark: | 3* |

!!!
In 2021, *Sensitive Data Exposure*.
!!!
==- Identification and Authentication Failures

+++ Notable CWEs
- CWE-297: Improper Validation of Certificate with Host Mismatch
- CWE-287: Improper Authentication
- CWE-384: Session Fixation
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 7 |
| Top 10:2017 | :white_check_mark: | 2? |

==- Injection

+++ Notable CWEs
- CWE-79: Cross-site Scripting
- CWE-89: SQL Injection
- CWE-73: External Control of File Name or Path
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 3 |
| Top 10:2017 | :white_check_mark: | 1 |

> Text below this needs to be cited.

An injection attack occurs when an attacker sends malicious statements to an application via data input fields. Another way to say this is that untrusted data is sent to an interpreter as part of a command or query. These could be SQL queries, LDAP queries, or other forms of injection.

To prevent injection attacks:

- Whitelisting input validation/bounds checking (preventing what types of data can be input)
- Using prepared statements
- Escaping all user supplied input
==- Insecure Deserialization
!!!
In 2021, this risk was merged with and renamed to [Software and Data Integrity Failures](#software-and-data-integrity-failures).
!!!

+++ Notable CWEs
- CWE-502: Deserialization of Untrusted Data
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |

> Text below this needs to be cited.

Serialization is the process of turning some object into a data format that can be restored later. People often serialize objects in order to save them to storage, or to send as part of communications.

Deserialization is the reverse of serialization; taking data structured from some format and rebuilding it into an object. The features of these native deserialization mechanisms can be repurposed for malicious effect when operating on untrusted data. Attacks against deserializers have been found to allow DoS, access control, and remote code execution attacks.

!!!
Today the most popular data format for serializing data is JSON. Before that, it was XML.
!!!
==- Insecure Design

+++ Notable CWEs
- CWE-209: Generation of Error Message Containing Sensitive Information
- CWE-256: Unprotected Storage of Credentials
- CWE-501: Trust Boundary Violation
- CWE-522: Insufficiently Protected Credentials
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 4 |
| Top 10:2017 | :white_check_mark: | 8? |

==- Insecure Direct Object References
!!!
This risk was merged into [Broken Access Control](#broken-access-control) in 2017.
!!!
==- Insufficient Logging and Monitoring
!!!
In 2021, this risk was renamed to [Security Logging and Monitoring Failures](#security-logging-and-monitoring-failures).
!!!
==- Security Logging and Monitoring Failures

+++ Notable CWEs
- CWE-117: Improper Output Neutralization for Logs
- CWE-223: Omission of Security-relevant Information
- CWE-532: Insertion of Sensitive Information into Log File
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 9 |
| Top 10:2017 | :white_check_mark: | 10* |

!!!
This risk was formerly known as *Insufficient Logging and Monitoring*.
!!!
==- Missing Function Level Access Control
This was merged into [Broken Access Control](#broken-access-control) in 2017.
==- Security Misconfiguration

+++ Notable CWEs
- CWE-16: Configuration
- CWE-611: Improper Restriction of XML External Entity Reference
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 5 |
| Top 10:2017 | :white_check_mark: | 6 |

> Text below this needs to be cited.

+++ Prevention
- Secure settings should be defined, implemented, and maintained, as defaults are well known to attackers.
- Software should be patched regularly to keep it up to date.
- Software settings should be kept up to date.
+++
==- Sensitive Data Exposure
!!!
In 2021, this was renamed to [Cryptographic Failures](#vulnerable-and-outdated-components).
!!!
==- Server-Side Request Forgery (SSRF)

<span id="rev1"></span>SSRF flaws occur whenever a web application is fetching a remote resource without validating the user-supplied URL. It allows an attacker to coerce the application to send a crafted request to an unexpected destination, even when protected by a firewall, VPN, or another type of network access control list (ACL).

As modern web applications provide end-users with convenient features, fetching a URL becomes a common scenario. As a result, the incidence of SSRF is increasing. Also, the severity of SSRF is becoming higher due to cloud services and the complexity of architectures.[[¹⁰]](#ref10)

+++ Notable CWEs
The data shows a relatively low incidence rate with above average testing coverage and above-average Exploit and Impact potential ratings.
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 10 |
| Top 10:2017 | :x: | |

==- Software and Data Integrity Failures

+++ Notable CWEs
- CWE-829: Inclusion of Functionality from Untrusted Control Sphere
- CWE-494: Download of Code Without Integrity Check
- CWE-502: Deserialization of Untrusted Data
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 8 |
| Top 10:2017 | :x: | |

==- Using Components with Known Vulnerabilities
!!!
In 2021, this was renamed to [Vulnerable and Outdated Components](#vulnerable-and-outdated-components).
!!!

+++ Notable CWEs
CWE does not cover the limitations of human processes and procedures that cannot be described in terms of a specific technical weakness as resident in the code, architecture, or configuration of the software. Since "known vulnerabilities" can arise from any kind of weakness, it is not possible to map this OWASP category to other CWE entries, since it would effectively require mapping this category to ALL weaknesses.[https://cwe.mitre.org/data/definitions/1035.html]
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 9 |

Components, such as libraries, frameworks, and other software modules, almost always run with full privileges.

+++ Impact
- This could allow an attack to undermine application defenses and launch unpredictable attacks.
- Data loss or server takeover.
+++ Prevention
- Applications using components with known vulnerabilities should be quarantined or, at an absolute minimum, have special monitoring to prevent application attacks.
+++

It's important to remember that these are known vulnerabilities, not unknown. Developers are willingly using these components knowing that they have vulnerabilities. This could be for a variety of reasons, including the fact that they may not actually be leveraging a "vulnerable" aspect of a particular component in their application.
==- Vulnerable and Outdated Components

+++ Notable CWEs
- CWE-1104: Use of Unmaintained Third-Party Components
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 6 |
| Top 10:2017 | :white_check_mark: | 9* |

!!!
In 2017, this was known as *Using Components with Known Vulnerabilities*.
!!!
==- XML External Entities (XXE)
!!!
In 2021, this risk was merged with and renamed to [Security Minconfiguration](#security-misconfiguration).
!!!

+++ Notable CWEs
- CWE-611: Improper Restriction of XML External Entity Reference
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 4 |

> Text below this needs to be cited.

XML external entities refer to references, such as the application directory structure or the configuration of the hosting system, that should be removed from the code, but are left in by accident. These items can provide information to an attacker that may allow them to circumvent authentication measures to gain access.

Attackers can exploit vulnerable XML processors if they can upload XML or include hostile content in an XML document, exploiting vulnerable code, dependencies, or integrations.
==-

## References

1. <span id="ref1"></span>[⌃](#rev1) OWASP. (2021). *A01:2021 - Broken Access Control*. https://owasp.org/Top10/A01_2021-Broken_Access_Control
10. <span id="ref10"></span>[⌃](#rev10) OWASP. (2021). *A10:2021 - Server-Side Request Forgery (SSRF)*. https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29/

## Sources

- MITRE. (n.d.). *CWE*. https://cwe.mitre.org/
- OWASP. (2021). *OWASP Top 10*. https://owasp.org/www-project-top-ten
- OWASP. (2017). *OWASP Top 10*. https://owasp.org/www-pdf-archive/OWASP_Top_10-2017_%28en%29.pdf.pdf