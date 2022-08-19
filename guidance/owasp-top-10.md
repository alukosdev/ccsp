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
| CSRF | Cross-Site Request Forgery |
| OWASP | Open Web Application Security Project |
| SSRF | Server Side Request Forgery |
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
10. [Server Side Request Forgery (SSRF)](#server-side-request-forgery-ssrf)
+++ Top 10:2017
- A1:2017 - [Injection](#injection)
- A2:2017 - [Broken Authentication](#broken-authentication)
- A3:2017 - [Sensitive Data Exposure](#sensitive-data-exposure)
- A4:2017 - [XML External Entities (XXE)](#xml-external-entities-xxe)
- A5:2017 - [Broken Access Control](#broken-access-control)
- A6:2017 - [Security Misconfiguration](#security-misconfiguration)
- A7:2017 - [Cross-Site Scripting (XSS)](#cross-site-scripting-xss)
- A8:2017 - [Insecure Deserialization](#insecure-deserialization)
- A9:2017 - [Using Components with Known Vulnerabilities](#using-components-with-known-vulnerabilities)
- A10:2017 - [Insufficient Logging and Monitoring](#insufficient-logging-and-monitoring)
+++ Top 10:2013
- A1:2013 - [Injection](#injection)
- A2:2013 - [Broken Authentication and Session Management](#broken-authentication)
- A3:2013 - [Cross-Site Scripting (XSS)](#cross-site-scripting-xss)
- A4:2013 - [Insecure Direct Object References](#insecure-direct-object-references)
- A5:2013 - [Security Misconfiguration](#security-misconfiguration)
- A6:2013 - [Sensitive Data Exposure](#sensitive-data-exposure)
- A7:2013 - [Missing Functional Level Access Control](#missing-functional-level-access-control)
- A8:2013 - [Cross-Site Request Forgery (CSRF)](#cross-site-request-forgery-csrf)
- A9:2013 - [Using Components with Known Vulnerabilities](#using-components-with-known-vulnerabilities)
- A10:2013 - [Unvalidated Redirects and Forwards](#unvalidated-redirects-and-forwards)
+++

## Web Application Security Risks

==- Broken Access Control
<span id="rev1"></span>Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits.[[¹]](#ref1)

+++ Attack Scenarios
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 1 |
| Top 10:2017 | :white_check_mark: | 5 |
| Top 10:2013 | :white_check_mark: | 7* |

> Text below this needs to be cited.

+++ Impact
- Attackers can forge requests allowing access to functionality without proper authorization.
+++ Prevention
- Set the default to deny all access to functions, and require authentication/authorization for each access request. This ensures that no particular function may be run without explicitly ensuring that it was called by an authorized user.
- Run a process as both a user and privileged user, compare results, and determine similarity.
+++

!!!
This risk was formerly known as *missing function-level access control*.
!!!
==- Cryptographic Failures

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 2 |
| Top 10:2017 | :white_check_mark: | 3* |
| Top 10:2013 | :white_check_mark: | 6* |

!!!
This risk was formerly known as *sensitive data exposure*.
!!!
==- Injection

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 3 |
| Top 10:2017 | :white_check_mark: | 1 |
| Top 10:2013 | :white_check_mark: | 1 |

> Text below this needs to be cited.

An injection attack occurs when an attacker sends malicious statements to an application via data input fields. Another way to say this is that untrusted data is sent to an interpreter as part of a command or query. These could be SQL queries, LDAP queries, or other forms of injection.

To prevent injection attacks:

- Whitelisting input validation/bounds checking (preventing what types of data can be input)
- Using prepared statements
- Escaping all user supplied input
==- Insecure Design

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 4 |
| Top 10:2017 | :white_check_mark: | 8? |
| Top 10:2013 | :white_check_mark: | 4? |

==- Security Misconfiguration

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 5 |
| Top 10:2017 | :white_check_mark: | 6 |
| Top 10:2013 | :white_check_mark: | 5 |

> Text below this needs to be cited.

+++ Prevention
- Secure settings should be defined, implemented, and maintained, as defaults are well known to attackers.
- Software should be patched regularly to keep it up to date.
- Software settings should be kept up to date.
+++
==- Vulnerable and Outdated Components

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 6 |
| Top 10:2017 | :white_check_mark: | 9? |
| Top 10:2013 | :white_check_mark: | 9? |

==- Identification and Authentication Failures

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 7 |
| Top 10:2017 | :white_check_mark: | 2? |
| Top 10:2013 | :white_check_mark: | 2? |

==- Software and Data Integrity Failures

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 8 |
| Top 10:2017 | :x: | |
| Top 10:2013 | :x: | |

==- Security Logging and Monitoring Failures

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 9 |
| Top 10:2017 | :x: | |
| Top 10:2013 | :x: | |

==- Server Side Request Forgery (SSRF)

> Are other vulnerabilities part of SSRF, such as CSRF, XSS, and XXE?

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 10 |
| Top 10:2017 | :x: | |
| Top 10:2013 | :x: | |

==- Broken Authentication

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 2 |
| Top 10:2013 | :white_check_mark: | 2? |

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
==- Sensitive Data Exposure

*See [Cryptographic Failures](#cryptographic-failures)

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 3 |
| Top 10:2013 | :white_check_mark: | 6 |

> Text below this needs to be cited.

Commonly allowed when web applications do not properly protect sensitive data, such as credit cards, tax IDs, and authentication credentials. Attackers may steal or modify poorly protected data to initiate credit card fraud, identity theft, or other felonies. Even with proper encryption methods put in place, sensitive data is still at risk if the client's browser is insecure.

+++ Impact
- Attackers may steal or modify weakly protected data to conduct fraud, theft, or other crimes.
+++ Prevention
- Encryption (at rest or in transit)
- Perform checks against client browsers to ensure they meet security standards. If the browser doesn't meet the security standards, it can be prevented access to the web application.
+++
==- XML External Entities (XXE)

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 4 |
| Top 10:2013 | :x: | |

> Text below this needs to be cited.

XML external entities refer to references, such as the application directory structure or the configuration of the hosting system, that should be removed from the code, but are left in by accident. These items can provide information to an attacker that may allow them to circumvent authentication measures to gain access.

Attackers can exploit vulnerable XML processors if they can upload XML or include hostile content in an XML document, exploiting vulnerable code, dependencies, or integrations.
==- Cross-Site Scripting (XSS)

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 7 |
| Top 10:2013 | :white_check_mark: | 3 |

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
==- Insecure Deserialization

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |
| Top 10:2013 | :x: | |

> Text below this needs to be cited.

Serialization is the process of turning some object into a data format that can be restored later. People often serialize objects in order to save them to storage, or to send as part of communications.

Deserialization is the reverse of serialization; taking data structured from some format and rebuilding it into an object. The features of these native deserialization mechanisms can be repurposed for malicious effect when operating on untrusted data. Attacks against deserializers have been found to allow DoS, access control, and remote code execution attacks.

!!!
Today the most popular data format for serializing data is JSON. Before that, it was XML.
!!!
==- Using Components with Known Vulnerabilities

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 9 |
| Top 10:2013 | :white_check_mark: | 9 |

Components, such as libraries, frameworks, and other software modules, almost always run with full privileges.

+++ Impact
- This could allow an attack to undermine application defenses and launch unpredictable attacks.
- Data loss or server takeover.
+++ Prevention
- Applications using components with known vulnerabilities should be quarantined or, at an absolute minimum, have special monitoring to prevent application attacks.
+++

It's important to remember that these are known vulnerabilities, not unknown. Developers are willingly using these components knowing that they have vulnerabilities. This could be for a variety of reasons, including the fact that they may not actually be leveraging a "vulnerable" aspect of a particular component in their application.
==- Insufficient Logging and Monitoring

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 10 |
| Top 10:2013 | :x: | |

==- Insecure Direct Object References

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :x: | |
| Top 10:2013 | :white_check_mark: | 4 |

> Text below this needs to be cited.

When a developer allows a reference to an internal implementation object to be exposed. The exposure could be a file, directory, or database key. An example could be the following URL:

`www.sybex.com/authoraccounts/benmalisow`

The URL reveals location of specific data as well as the format for potential other data (such as other authors' pages/accounts).

+++ Impact
- Attackers may be able to manipulate these references to access unauthorized data.
+++ Prevention
- Refrain from including direct access information in URLs.
- Check access each time a direct object reference is called by an untrusted source.
- Run a process as both user and privileged user, compare results, and determine similarity; this will help you determine if there are functions that regular users should not have access to and thereby demonstrate that you are missing necessary controls.
+++
==- Cross-Site Request Forgery (CSRF)

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :x: | |
| Top 10:2013 | :white_check_mark: | 8 |

> Text below this needs to be cited.

Occurs when a logged-on user's browser sends a forged HTTP request along with cookies and other authentication information, forcing the victim's browser to generate a request that the application thinks is a legitimate request from the user.

+++ Impact
- The attacker could have the user log into one of the user's online accounts.
- The attacker could collect the user's online account login credentials to be used by the attacker later.
- The attacker could have the user perform an action in one of the user's online accounts.
+++ Prevention
- Ensure that all HTTP resource requests include a unique, unpredictable token.
- Include a CAPTCHA code as part of the user resource request process.
+++
==- Unvalidated Redirects and Forwards

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :x: | |
| Top 10:2013 | :white_check_mark: | 10 |

> Text below this needs to be cited.

Redirection to unauthorized pages, often in conjunction with a social engineering/phishing aspect.

+++ Prevention
- Don't use redirects/forwards in your applications.
- Train users to recognize invalidated links.
+++
==- Missing Functional Level Access Control
*See [Broken Access Control](#broken-access-control)*.
==-

!!!
To address these vulnerabilities, organizations must have an application risk management program in place. Implementation of an application risk management program addresses not only vulnerabilities but also all risks associated with applications.
!!!

## References

1. <span id="ref1"></span>[⌃](#rev1) OWASP. (2021). *A01:2021 - Broken Access Control*. https://owasp.org/Top10/A01_2021-Broken_Access_Control/

## Sources

- OWASP. (2021). *OWASP Top 10*. https://owasp.org/www-project-top-ten
- OWASP. (2017). *OWASP Top 10*. https://owasp.org/www-pdf-archive/OWASP_Top_10-2017_%28en%29.pdf.pdf
- OWASP. (2013). *OWASP Top 10*. https://owasp.org/www-pdf-archive/OWASP_Top_10_-_2013.pdf