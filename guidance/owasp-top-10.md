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
| DTD | Document Type Definitions |
| OWASP | Open Web Application Security Project |
| SOAP | Simple Object Access Protocol |
| SSO | Single Sign-On |
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

==- :white_check_mark: Broken Access Control
Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits.

Notable Common Weakness Enumerations (CWEs) include:

- CWE-200: Exposure of Sensitive Information to an Unauthorized Actor
- CWE-201: Insertion of Sensitive Information Into Sent Data
- CWE-352: Cross-Site Request Forgery

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
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 1 |
| Top 10:2017 | :white_check_mark: | 5 |
==- :x: Broken Authentication
Application functions related to authentication and session management are often implemented incorrectly, allowing attackers to compromise passwords, keys, or session tokens, or to exploit other implementation flaws to assume other users’ identities temporarily or permanently.

Notable Common Weakness Enumerations (CWEs) include:

- CWE-256: Plaintext Storage of a Password
- CWE-308: Use of Single-factor Authentication
- CWE-523: Unprotected Transport of Credentials

+++ Vulnerabilities
+++ Prevention
+++ Attack Scenarios
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 2 |

!!!
This risk was renamed to [Identification and Authentication Failures](#identification-and-authentication-failures) in 2021.
!!!
==- :x: Cross-Site Scripting (XSS)
Notable Common Weakness Enumerations (CWEs) include:

- CWE-79: Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting')

+++ Vulnerabilities
+++ Prevention
+++ Attack Scenarios
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 7 |

!!!
This risk was merged with and renamed to [Injection](#injection) in 2021.
!!!
==- :white_check_mark: :zap: Cryptographic Failures
!!!danger
We need to add a summary here. I dislike the summary provided by OWASP.
!!!

Notable Common Weakness Enumerations (CWEs) include:

- CWE-259: Use of Hard-coded Password
- CWE-327: Broken or Risky Crypto Algorithm
- CWE-331: Insufficient Entropy

+++ Attack Scenarios
**Scenario #1**: An application encrypts credit card numbers in a database using automatic database encryption. However, this data is automatically decrypted when retrieved, allowing a SQL injection flaw to retrieve credit card numbers in clear text.

---

**Scenario #2**: A site doesn't use or enforce TLS for all pages or supports weak encryption. An attacker monitors network traffic (e.g., at an insecure wireless network), downgrades connections from HTTPS to HTTP, intercepts requests, and steals the user's session cookie. The attacker then replays this cookie and hijacks the user's (authenticated) session, accessing or modifying the user's private data. Instead of the above they could alter all transported data, e.g., the recipient of a money transfer.

---

**Scenario #3**: The password database uses unsalted or simple hashes to store everyone's passwords. A file upload flaw allows an attacker to retrieve the password database. All the unsalted hashes can be exposed with a rainbow table of pre-calculated hashes. Hashes generated by simple or fast hash functions may be cracked by GPUs, even if they were salted.
+++ Vulnerabilities
The first thing is to determine the protection needs of data in transit and at rest. For example, passwords, credit card numbers, health records, personal information, and business secrets require extra protection, mainly if that data falls under privacy laws, e.g., EU's General Data Protection Regulation (GDPR), or regulations, e.g., financial data protection such as PCI Data Security Standard (PCI DSS). For all such data:

- Is any data transmitted in clear text? This concerns protocols such as HTTP, SMTP, FTP also using TLS upgrades like STARTTLS. External internet traffic is hazardous. Verify all internal traffic, e.g., between load balancers, web servers, or back-end systems.
- Are any old or weak cryptographic algorithms or protocols used either by default or in older code?
- Are default crypto keys in use, weak crypto keys generated or re-used, or is proper key management or rotation missing? Are crypto keys checked into source code repositories?
- Is encryption not enforced, e.g., are any HTTP headers (browser) security directives or headers missing?
- Is the received server certificate and the trust chain properly validated?
- Are initialization vectors ignored, reused, or not generated sufficiently secure for the cryptographic mode of operation? Is an insecure mode of operation such as ECB in use? Is encryption used when authenticated encryption is more appropriate?
- Are passwords being used as cryptographic keys in absence of a password base key derivation function?
- Is randomness used for cryptographic purposes that was not designed to meet cryptographic requirements? Even if the correct function is chosen, does it need to be seeded by the developer, and if not, has the developer over-written the strong seeding functionality built into it with a seed that lacks sufficient entropy/unpredictability?
- Are deprecated hash functions such as MD5 or SHA1 in use, or are non-cryptographic hash functions used when cryptographic hash functions are needed?
- Are deprecated cryptographic padding methods such as PKCS number 1 v1.5 in use?
- Are cryptographic error messages or side channel information exploitable, for example in the form of padding oracle attacks?
+++ Prevention
- Classify data processed, stored, or transmitted by an application. Identify which data is sensitive according to privacy laws, regulatory requirements, or business needs.
- Don't store sensitive data unnecessarily. Discard it as soon as possible or use PCI DSS compliant tokenization or even truncation. Data that is not retained cannot be stolen.
- Make sure to encrypt all sensitive data at rest.
- Ensure up-to-date and strong standard algorithms, protocols, and keys are in place; use proper key management.
- Encrypt all data in transit with secure protocols such as TLS with forward secrecy (FS) ciphers, cipher prioritization by the server, and secure parameters. Enforce encryption using directives like HTTP Strict Transport Security (HSTS).
- Disable caching for response that contain sensitive data.
- Apply required security controls as per the data classification.
- Do not use legacy protocols such as FTP and SMTP for transporting sensitive data.
- Store passwords using strong adaptive and salted hashing functions with a work factor (delay factor), such as Argon2, scrypt, bcrypt or PBKDF2.
- Initialization vectors must be chosen appropriate for the mode of operation. For many modes, this means using a CSPRNG (cryptographically secure pseudo random number generator). For modes that require a nonce, then the initialization vector (IV) does not need a CSPRNG. In all cases, the IV should never be used twice for a fixed key.
- Always use authenticated encryption instead of just encryption.
- Keys should be generated cryptographically randomly and stored in memory as byte arrays. If a password is used, then it must be converted to a key via an appropriate password base key derivation function.
- Ensure that cryptographic randomness is used where appropriate, and that it has not been seeded in a predictable way or with low entropy. Most modern APIs do not require the developer to seed the CSPRNG to get security.
- Avoid deprecated cryptographic functions and padding schemes, such as MD5, SHA1, PKCS number 1 v1.5 .
- Verify independently the effectiveness of configuration and settings.
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 2 |
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Sensitive Data Exposure](#sensitive-data-exposure) in 2021.
!!!
==- :white_check_mark: Identification and Authentication Failures
Confirmation of the user's identity, authentication, and session management is critical to protect against authentication-related attacks.

Notable Common Weakness Enumerations (CWEs) include:

- CWE-297: Improper Validation of Certificate with Host Mismatch
- CWE-287: Improper Authentication
- CWE-384: Session Fixation

+++ Attack Scenarios
**Scenario #1**: Credential stuffing, the use of lists of known passwords, is a common attack. Suppose an application does not implement automated threat or credential stuffing protection. In that case, the application can be used as a password oracle to determine if the credentials are valid.

---

**Scenario #2**: Most authentication attacks occur due to the continued use of passwords as a sole factor. Once considered best practices, password rotation and complexity requirements encourage users to use and reuse weak passwords. Organizations are recommended to stop these practices per NIST 800-63 and use multi-factor authentication.

---

**Scenario #3**: Application session timeouts aren't set correctly. A user uses a public computer to access an application. Instead of selecting "logout," the user simply closes the browser tab and walks away. An attacker uses the same browser an hour later, and the user is still authenticated.
+++ Vulnerabilities
There may be authentication weaknesses if the application:

- Permits automated attacks such as credential stuffing, where the attacker has a list of valid usernames and passwords.
- Permits brute force or other automated attacks.
- Permits default, weak, or well-known passwords, such as "Password1" or "admin/admin".
- Uses weak or ineffective credential recovery and forgot-password processes, such as "knowledge-based answers," which cannot be made safe.
- Uses plain text, encrypted, or weakly hashed passwords data stores (see [A02:2021-Cryptographic Failures](#cryptographic-failures)).
- Has missing or ineffective multi-factor authentication.
- Exposes session identifier in the URL.
- Reuse session identifier after successful login.
- Does not correctly invalidate Session IDs. User sessions or authentication tokens (mainly single sign-on (SSO) tokens) aren't properly invalidated during logout or a period of inactivity.
+++ Prevention
- Where possible, implement multi-factor authentication to prevent automated credential stuffing, brute force, and stolen credential reuse attacks.
- Do not ship or deploy with any default credentials, particularly for admin users.
- Implement weak password checks, such as testing new or changed passwords against the top 10,000 worst passwords list.
- Align password length, complexity, and rotation policies with National Institute of Standards and Technology (NIST) 800-63b's guidelines in section 5.1.1 for Memorized Secrets or other modern, evidence-based password policies.
- Ensure registration, credential recovery, and API pathways are hardened against account enumeration attacks by using the same messages for all outcomes.
- Limit or increasingly delay failed login attempts, but be careful not to create a denial of service scenario. Log all failures and alert administrators when credential stuffing, brute force, or other attacks are detected.
- Use a server-side, secure, built-in session manager that generates a new random session ID with high entropy after login. Session identifier should not be in the URL, be securely stored, and invalidated after logout, idle, and absolute timeouts.
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 7 |
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Broken Authentication](#broken-authentication) in 2021.
!!!
==- :white_check_mark: Injection
Notable Common Weakness Enumerations (CWEs) include:

- CWE-79: Cross-site Scripting
- CWE-89: SQL Injection
- CWE-73: External Control of File Name or Path

+++ Attack Scenarios
**Scenario #1**: An application uses untrusted data in the construction of the following vulnerable SQL call:

```
String query = "SELECT \* FROM accounts WHERE custID='" + request.getParameter("id") + "'";
```

---

**Scenario #2**: Similarly, an application’s blind trust in frameworks may result in queries that are still vulnerable, (e.g., Hibernate Query Language (HQL)):

```
Query HQLQuery = session.createQuery("FROM accounts WHERE custID='" + request.getParameter("id") + "'");
```

In both cases, the attacker modifies the ‘id’ parameter value in their browser to send: ‘ or ‘1’=’1. For example:
```
http://example.com/app/accountView?id=' or '1'='1
```

This changes the meaning of both queries to return all the records from the accounts table. More dangerous attacks could modify or delete data or even invoke stored procedures.
+++ Vulnerabilities
An application is vulnerable to attack when:

- User-supplied data is not validated, filtered, or sanitized by the application.
- Dynamic queries or non-parameterized calls without context-aware escaping are used directly in the interpreter.
- Hostile data is used within object-relational mapping (ORM) search parameters to extract additional, sensitive records.
- Hostile data is directly used or concatenated. The SQL or command contains the structure and malicious data in dynamic queries, commands, or stored procedures.
+++ Prevention
Source code review is the best method of detecting if applications are vulnerable to injections. Automated testing of all parameters, headers, URL, cookies, JSON, SOAP, and XML data inputs is strongly encouraged. Organizations can include static (SAST), dynamic (DAST), and interactive (IAST) application security testing tools into the CI/CD pipeline to identify introduced injection flaws before production deployment.

Preventing injection requires keeping data separate from commands and queries:

- The preferred option is to use a safe API, which avoids using the interpreter entirely, provides a parameterized interface, or migrates to Object Relational Mapping Tools (ORMs).

!!!
Even when parameterized, stored procedures can still introduce SQL injection if PL/SQL or T-SQL concatenates queries and data or executes hostile data with EXECUTE IMMEDIATE or exec().
!!!
- Use positive server-side input validation. This is not a complete defense as many applications require special characters, such as text areas or APIs for mobile applications.
- For any residual dynamic queries, escape special characters using the specific escape syntax for that interpreter.

!!!
SQL structures such as table names, column names, and so on cannot be escaped, and thus user-supplied structure names are dangerous. This is a common issue in report-writing software.
!!!
- Use LIMIT and other SQL controls within queries to prevent mass disclosure of records in case of SQL injection.
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 3 |
| Top 10:2017 | :white_check_mark: | 1 |

!!!
This risk was merged with and renamed from [Cross-Site Scripting (XSS)](#cross-site-scripting-xss) in 2021.
!!!
==- :x: Insecure Deserialization
Notable Common Weakness Enumerations (CWEs) include:

- CWE-502: Deserialization of Untrusted Data

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |

!!!
This risk was merged with and renamed to [Software and Data Integrity Failures](#software-and-data-integrity-failures) in 2021.
!!!
==- :zap: Insecure Design
Notable Common Weakness Enumerations (CWEs) include:

- CWE-209: Generation of Error Message Containing Sensitive Information
- CWE-256: Unprotected Storage of Credentials
- CWE-501: Trust Boundary Violation
- CWE-522: Insufficiently Protected Credentials

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 4 |
| Top 10:2017 | :x: | |

==- :x: Insufficient Logging and Monitoring

Notable Common Weakness Enumerations (CWEs) include:

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 10 |

!!!
This risk was renamed to [Security Logging and Monitoring Failures](#security-logging-and-monitoring-failures) in 2021.
!!!
==- :zap: Security Logging and Monitoring Failures
Notable Common Weakness Enumerations (CWEs) include:

- CWE-117: Improper Output Neutralization for Logs
- CWE-223: Omission of Security-relevant Information
- CWE-532: Insertion of Sensitive Information into Log File

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 9 |
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Insufficient Logging and Monitoring](#insufficient-logging-and-monitoring) in 2021.
!!!
==- :zap: Security Misconfiguration
Notable Common Weakness Enumerations (CWEs) include:

- CWE-16: Configuration
- CWE-611: Improper Restriction of XML External Entity Reference

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 5 |
| Top 10:2017 | :white_check_mark: | 6 |

==- :x: Sensitive Data Exposure
Notable Common Weakness Enumerations (CWEs) include:

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 3 |

!!!
This risk was renamed to [Cryptographic Failures](#vulnerable-and-outdated-components) in 2021.
!!!
==- :zap: Server-Side Request Forgery (SSRF)
SSRF flaws occur whenever a web application is fetching a remote resource without validating the user-supplied URL. It allows an attacker to coerce the application to send a crafted request to an unexpected destination, even when protected by a firewall, VPN, or another type of network access control list (ACL).

As modern web applications provide end-users with convenient features, fetching a URL becomes a common scenario. As a result, the incidence of SSRF is increasing. Also, the severity of SSRF is becoming higher due to cloud services and the complexity of architectures.

Notable Common Weakness Enumerations (CWEs) include:

- The data shows a relatively low incidence rate with above average testing coverage and above-average Exploit and Impact potential ratings.

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 10 |
| Top 10:2017 | :x: | |

==- :zap: Software and Data Integrity Failures
Notable Common Weakness Enumerations (CWEs) include:

- CWE-829: Inclusion of Functionality from Untrusted Control Sphere
- CWE-494: Download of Code Without Integrity Check
- CWE-502: Deserialization of Untrusted Data

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 8 |

!!!
This risk was merged with and renamed from [Insecure Deserialization](#insecure-deserialization) in 2021.
!!!
==- :x: Using Components with Known Vulnerabilities
Notable Common Weakness Enumerations (CWEs) include:

- CWE does not cover the limitations of human processes and procedures that cannot be described in terms of a specific technical weakness as resident in the code, architecture, or configuration of the software. Since "known vulnerabilities" can arise from any kind of weakness, it is not possible to map this OWASP category to other CWE entries, since it would effectively require mapping this category to ALL weaknesses.[https://cwe.mitre.org/data/definitions/1035.html]

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :x: | |
| Top 10:2017 | :white_check_mark: | 9 |

!!!
This risk was renamed to [Vulnerable and Outdated Components](#vulnerable-and-outdated-components) in 2021.
!!!
==- :zap: Vulnerable and Outdated Components
Notable Common Weakness Enumerations (CWEs) include:

- CWE-1104: Use of Unmaintained Third-Party Components

+++ Attack Scenarios
+++ Vulnerabilities
+++ Prevention
+++

| Publication | Appearance | Ranking |
| - | - | - |
| Top 10:2021 | :white_check_mark: | 6 |
| Top 10:2017 | :x: | |

!!!
This risk was renamed from [Using Components with Known Vulnerabilities](#using-components-with-known-vulnerabilities) in 2021.
!!!
==- :white_check_mark: XML External Entities (XXE)
Notable Common Weakness Enumerations (CWEs) include:

- CWE-611: Improper Restriction of XML External Entity Reference

+++ Attack Scenarios
**Scenario #1**: The attacker attempts to extract data from the 
server:

```
<?xml version="1.0" encoding="ISO-8859-1"?>
<!DOCTYPE foo [
<!ELEMENT foo ANY >
<!ENTITY xxe SYSTEM "file:///etc/passwd" >]>
<foo>&xxe;</foo>
```
---

**Scenario #2**: An attacker probes the server's private network by 
changing the above `ENTITY` line to:

```
<!ENTITY xxe SYSTEM "https://192.168.1.1/private" >]>
```
---

**Scenario #3**: An attacker attempts a denial-of-service attack by 
including a potentially endless file:

```
<!ENTITY xxe SYSTEM "file:///dev/random" >]>
```
+++ Vulnerabilities
Applications and in particular XML-based web services or 
downstream integrations might be vulnerable to attack if:

- The application accepts XML directly or XML uploads, 
especially from untrusted sources, or inserts untrusted data into 
XML documents, which is then parsed by an XML processor.
- Any of the XML processors in the application or SOAP based 
web services has document type definitions (DTDs) enabled. 
As the exact mechanism for disabling DTD processing varies 
by processor, it is good practice to consult a reference such as 
the OWASP Cheat Sheet 'XXE Prevention’. 
- If your application uses SAML for identity processing within 
federated security or single sign on (SSO) purposes. SAML 
uses XML for identity assertions, and may be vulnerable.
- If the application uses SOAP prior to version 1.2, it is likely 
susceptible to XXE attacks if XML entities are being passed to 
the SOAP framework.
- Being vulnerable to XXE attacks likely means that the 
application is vulnerable to denial of service attacks including 
the Billion Laughs attack.
+++ Prevention
Developer training is essential to identify and mitigate XXE. 
Besides that, preventing XXE requires:

- Whenever possible, use less complex data formats such as 
JSON, and avoiding serialization of sensitive data.
- Patch or upgrade all XML processors and libraries in use by 
the application or on the underlying operating system. Use 
dependency checkers. Update SOAP to SOAP 1.2 or higher.
- Disable XML external entity and DTD processing in all XML 
parsers in the application, as per the OWASP Cheat Sheet 
'XXE Prevention'. 
- Implement positive ("whitelisting") server-side input validation, 
filtering, or sanitization to prevent hostile data within XML 
documents, headers, or nodes.
- Verify that XML or XSL file upload functionality validates 
incoming XML using XSD validation or similar.
- SAST tools can help detect XXE in source code, although 
manual code review is the best alternative in large, complex 
applications with many integrations.

If these controls are not possible, consider using virtual 
patching, API security gateways, or Web Application Firewalls 
(WAFs) to detect, monitor, and block XXE attacks.
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