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
+++

## Web Application Security Risks

!!!
To address these risks, organizations must have an application risk management program in place. Implementation of an application risk management program addresses not only vulnerabilities but also all risks associated with applications.
!!!

==- Broken Access Control
Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits.

Notable Common Weakness Enumerations (CWEs) include:

- CWE-200: Exposure of Sensitive Information to an Unauthorized Actor
- CWE-201: Insertion of Sensitive Information Into Sent Data
- CWE-352: Cross-Site Request Forgery

+++ Vulnerabilities
Common access control vulnerabilities include:

- Violation of the principle of least privilege or deny by default, where access should only be granted for particular capabilities, roles, or users, but is available to anyone.
- Bypassing access control checks by modifying the URL (parameter tampering or force browsing), internal application state, or the HTML page, or by using an attack tool modifying API requests.
- Permitting viewing or editing someone else's account, by providing its unique identifier (insecure direct object references)
- Accessing API with missing access controls for POST, PUT and DELETE.
- Elevation of privilege. Acting as a user without being logged in or acting as an admin when logged in as a user.
- Metadata manipulation, such as replaying or tampering with a JSON Web Token (JWT) access control token, or a cookie or hidden field manipulated to elevate privileges or abusing JWT invalidation.
- CORS misconfiguration allows API access from unauthorized/untrusted origins.
- Force browsing to authenticated pages as an unauthenticated user or to privileged pages as a standard user.
+++ Prevention
Access control is only effective in trusted server-side code or server-less API, where the attacker cannot modify the access control check or metadata.

- Except for public resources, deny by default.
- Implement access control mechanisms once and re-use them throughout the application, including minimizing Cross-Origin Resource Sharing (CORS) usage.
- Model access controls should enforce record ownership rather than accepting that the user can create, read, update, or delete any record.
- Unique application business limit requirements should be enforced by domain models.
- Disable web server directory listing and ensure file metadata (e.g., .git) and backup files are not present within web roots.
- Log access control failures, alert admins when appropriate (e.g., repeated failures).
- Rate limit API and controller access to minimize the harm from automated attack tooling.
- Stateful session identifiers should be invalidated on the server after logout. Stateless JWT tokens should rather be short-lived so that the window of opportunity for an attacker is minimized. For longer lived JWTs it's highly recommended to follow the OAuth standards to revoke access.

Developers and QA staff should include functional access control unit and integration tests.
+++ Attack Scenarios
**Scenario #1**: The application uses unverified data in a SQL call that is accessing account information:

```
pstmt.setString(1, request.getParameter("acct"));
ResultSet results = pstmt.executeQuery( );
```

An attacker simply modifies the browser's 'acct' parameter to send whatever account number they want. If not correctly verified, the attacker can access any user's account.

```
https://example.com/app/accountInfo?acct=notmyacct
```

---

**Scenario #2**: An attacker simply forces browses to target URLs. Admin rights are required for access to the admin page.

```
https://example.com/app/getappInfo
https://example.com/app/admin_getappInfo
```

If an unauthenticated user can access either page, it's a flaw. If a non-admin can access the admin page, this is a flaw.
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 1 |
| Top 10:2017 | :white_check_mark: | 5 |
==- Broken Authentication
Application functions related to authentication and session management are often implemented incorrectly, allowing attackers to compromise passwords, keys, or session tokens, or to exploit other implementation flaws to assume other users’ identities temporarily or permanently.

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

!!!
This risk was renamed to [Identification and Authentication Failures](#identification-and-authentication-failures) in 2021.
!!!
==- Cross-Site Scripting (XSS)
+++ Notable CWEs
- CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 7 |

!!!
This risk was merged with and renamed to [Injection](#injection) in 2021.
!!!
==- Cryptographic Failures

!!!danger
We need to add a summary here. I dislike the summary provided by OWASP.
!!!

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
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Sensitive Data Exposure](#sensitive-data-exposure) in 2021.
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
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Broken Authentication](#broken-authentication) in 2021.
!!!
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

!!!
This risk was merged with and renamed from [Cross-Site Scripting (XSS)](#cross-site-scripting-xss) in 2021.
!!!
==- Insecure Deserialization
+++ Notable CWEs
- CWE-502: Deserialization of Untrusted Data
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |

!!!
This risk was merged with and renamed to [Software and Data Integrity Failures](#software-and-data-integrity-failures) in 2021.
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
| Top 10:2017 | :x: | |

==- Insufficient Logging and Monitoring
+++ Notable CWEs
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 10 |

!!!
This risk was renamed to [Security Logging and Monitoring Failures](#security-logging-and-monitoring-failures) in 2021.
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
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Insufficient Logging and Monitoring](#insufficient-logging-and-monitoring) in 2021.
!!!
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

==- Sensitive Data Exposure
+++ Notable CWEs
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 3 |

!!!
This risk was renamed to [Cryptographic Failures](#vulnerable-and-outdated-components) in 2021.
!!!
==- Server-Side Request Forgery (SSRF)
SSRF flaws occur whenever a web application is fetching a remote resource without validating the user-supplied URL. It allows an attacker to coerce the application to send a crafted request to an unexpected destination, even when protected by a firewall, VPN, or another type of network access control list (ACL).

As modern web applications provide end-users with convenient features, fetching a URL becomes a common scenario. As a result, the incidence of SSRF is increasing. Also, the severity of SSRF is becoming higher due to cloud services and the complexity of architectures.

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
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |

!!!
This risk was merged with and renamed from [Insecure Deserialization](#insecure-deserialization) in 2021.
!!!
==- Using Components with Known Vulnerabilities
+++ Notable CWEs
CWE does not cover the limitations of human processes and procedures that cannot be described in terms of a specific technical weakness as resident in the code, architecture, or configuration of the software. Since "known vulnerabilities" can arise from any kind of weakness, it is not possible to map this OWASP category to other CWE entries, since it would effectively require mapping this category to ALL weaknesses.[https://cwe.mitre.org/data/definitions/1035.html]
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 9 |

!!!
This risk was renamed to [Vulnerable and Outdated Components](#vulnerable-and-outdated-components) in 2021.
!!!
==- Vulnerable and Outdated Components
+++ Notable CWEs
- CWE-1104: Use of Unmaintained Third-Party Components
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 6 |
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Using Components with Known Vulnerabilities](#using-components-with-known-vulnerabilities) in 2021.
!!!
==- XML External Entities (XXE)
+++ Notable CWEs
- CWE-611: Improper Restriction of XML External Entity Reference
+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 4 |

!!!
This risk was merged with [Security Misconfiguration](#security-misconfiguration) in 2021.
!!!
==-

## Sources

- https://owasp.org/www-project-top-ten/2017/Top_10.html
- https://owasp.org/www-project-top-ten/2017/A2_2017-Broken_Authentication

- MITRE. (n.d.). *CWE*. https://cwe.mitre.org/
- OWASP. (2021). *A01:2021 - Broken Access Control*. https://owasp.org/Top10/A01_2021-Broken_Access_Control
- OWASP. (2021). *OWASP Top 10*. https://owasp.org/www-project-top-ten
- OWASP. (2021). *A10:2021 - Server-Side Request Forgery (SSRF)*. https://owasp.org/Top10/A10_2021-Server-Side_Request_Forgery_%28SSRF%29
- OWASP. (2017). *OWASP Top 10*. https://owasp.org/www-pdf-archive/OWASP_Top_10-2017_%28en%29.pdf.pdf