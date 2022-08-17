---
categories: [Application Risk Management Guidance]
tags: [owasp]
---

# OWASP Top Ten

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| OWASP | Open Web Application Security Project |

## Overview

To address these vulnerabilities, organizations must have an application risk-management program in place. Implementation of an application risk-management program addresses not only vulnerabilities but also all risks associated with applications.

## Risks from 2020

1. Injection
2. Broken Authentication
3. Sensitive Data Exposure
4. XML External Entities (XXE)
5. Broken Access Control
6. Security Misconfiguration
7. Cross-Site Scripting (XSS)
8. Insecure Deserialization
9. Using Components with Known Vulnerabilities
10. Insufficient Logging and Monitoring

### 1. Injection

An injection attack occurs when an attacker sends malicious statements to an application via data input fields. Another way to say this is that untrusted data is sent to an interpreter as part of a command or query. These could be SQL queries, LDAP queries, or other forms of injection.

#### Prevention

- Whitelisting input validation/bounds checking (preventing what types of data can be input)
- Using prepared statements
- Escaping all user supplied input

### 2. Broken Authentication

Occurs when authentication and session management application functions are not implemented correctly.

#### Impact

- Allows attackers to compromise passwords, keys, or session tokens
- Exploitation of other implementation flaws to assume other identities

#### Prevention

- Do not use custom authentication schemes.
- Rotate session IDs after a successful login.
- Do not allow simple passwords to be used.
- Ensure the connection is encrypted so credentials aren't exposed.

### 3. Sensitive Data Exposure

Commonly allowed when web applications do not properly protect sensitive data, such as credit cards, tax IDs, and authentication credentials. Attackers may steal or modify poorly protected data to initiate credit card fraud, identity theft, or other felonies. Even with proper encryption methods put in place, sensitive data is still at risk if the client's browser is insecure.

#### Impact

- Attackers may steal or modify weakly protected data to conduct fraud, theft, or other crimes.

#### Prevention

- Encryption (at rest or in transit)
- Perform checks against client browsers to ensure they meet security standards. If the browser doesn't meet the security standards, it can be prevented access to the web application.

### 4. XML External Entities (XXE)

XML external entities refer to references, such as the application directory structure or the configuration of the hosting system, that should be removed from the code, but are left in by accident. These items can provide information to an attacker that may allow them to circumvent authentication measures to gain access.

Attackers can exploit vulnerable XML processors if they can upload XML or include hostile content in an XML document, exploiting vulnerable code, dependencies, or integrations.

### 5. Broken Access Control

This risk is also known as *missing function-level access control*.

Web applications typically verify function level access rights before allowing that functionality from the UI. Best practice requires applications to perform access control checks on the server when each function is accessed. Broken access control occurs when requests are not verified.

#### Impact

- Attackers can forge requests allowing access to functionality without proper authorization.

#### Prevention

- Set the default to deny all access to functions, and require authentication/authorization for each access request. This ensures that no particular function may be run without explicitly ensuring that it was called by an authorized user.
- Run a process as both a user and privileged user, compare results, and determine similarity.

### 6. Security Misconfiguration

#### Prevention

- Secure settings should be defined, implemented, and maintained, as defaults are well known to attackers.
- Software should be patched regularly to keep it up to date.
- Software settings should be kept up to date.

### 7. Cross-Site Scripting (XSS)

Occurs when an application receives untrusted data and then sends it to a web browser without proper validation.

#### Impact

- Allows attackers to execute scripts in a victim's browser which can hijack user sessions, deface websites, or redirect the user to malicious websites.

#### Prevention

- Use an auto-escaping template system
- Put untrusted data in only allowed slots of HTML documents
- HTML escape when including untrusted data in any HTML elements
- Use the attribute escape when including untrusted data in attribute elements
- Sanitize HTML markup with a library designed for the purpose

This is not a threat to the back-end database, but a threat to the client.

### 8. Insecure Deserialization

Serialization is the process of turning some object into a data format that can be restored later. People often serialize objects in order to save them to storage, or to send as part of communications.

Deserialization is the reverse of serialization; taking data structured from some format and rebuilding it into an object. The features of these native deserialization mechanisms can be repurposed for malicious effect when operating on untrusted data. Attacks against deserializers have been found to allow DoS, access control, and remote code execution attacks.

Today the most popular data format for serializing data is JSON. Before that, it was XML.

### 9. Using Components with Known Vulnerabilities

Components, such as libraries, frameworks, and other software modules, almost always run with full privileges.

#### Impact

- This could allow an attack to undermine application defenses and launch unpredictable attacks.
- Data loss or server takeover.

#### Prevention

- Applications using components with known vulnerabilities should be quarantined or, at an absolute minimum, have special monitoring to prevent application attacks.

It's important to remember that these are known vulnerabilities, not unknown. Developers are willingly using these components knowing that they have vulnerabilities. This could be for a variety of reasons, including the fact that they may not actually be leveraging a "vulnerable" aspect of a particular component in their application.

### 10. Insufficient Logging and Monitoring

## Risks from 2013

1. Injection
2. Broken Authentication and Session Management
3. Cross-Site Scripting (XSS)
4. **Insecure Direct Object References**
5. Security Misconfiguration
6. Sensitive Data Exposure
7. Missing Function-Level Access Control
8. **Cross-Site Request Forgery (CSRF)**
9. Using Components with Known Vulnerabilities
10. **Invalidated Redirects and Forwards**

### 4. Insecure Direct Object References

When a developer allows a reference to an internal implementation object to be exposed. The exposure could be a file, directory, or database key. An example could be the following URL:

`www.sybex.com/authoraccounts/benmalisow`

The URL reveals location of specific data as well as the format for potential other data (such as other authors' pages/accounts).

#### Impact

- Attackers may be able to manipulate these references to access unauthorized data.

#### Prevention

- Refrain from including direct access information in URLs.
- Check access each time a direct object reference is called by an untrusted source.
- Run a process as both user and privileged user, compare results, and determine similarity; this will help you determine if there are functions that regular users should not have access to and thereby demonstrate that you are missing necessary controls.

### 8. Cross-Site Request Forgery (CSRF)

Occurs when a logged-on user's browser sends a forged HTTP request along with cookies and other authentication information, forcing the victim's browser to generate a request that the application thinks is a legitimate request from the user.

#### Impact

- The attacker could have the user log into one of the user's online accounts.
- The attacker could collect the user's online account login credentials to be used by the attacker later.
- The attacker could have the user perform an action in one of the user's online accounts.

#### Prevention

- Ensure that all HTTP resource requests include a unique, unpredictable token.
- Include a CAPTCHA code as part of the user resource request process.

### 10. Invalidated Redirects and Forwards

Redirection to unauthorized pages, often in conjunction with a social engineering/phishing aspect.

#### Prevention

- Don't use redirects/forwards in your applications.
- Train users to recognize invalidated links.
