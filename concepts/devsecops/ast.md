---
label: Application Security Testing
---

# Application Security Testing (AST)

## Acronyms

| Acronym | Backronym |
| - | - |
| AST | Application Security Testing |
| DAST | Dynamic Application Security Testing |
| RASP | Runtime Application Self-Protection |
| SAST | Static Application Security Testing |

## Glossary

==- Black-Box Testing
Testing the program as it functions, in runtime.
==- Event-Driven Security
Automates detection and remediation of security issues.
==- Functional Testing
Functional testing is performed to confirm the functional aspect of a product. It verifies that a product is performing as expected based on the initial requirements laid out.
==- OWASP Dependency-Check
Dependency-Check is a Software Composition Analysis (SCA) tool that attempts to detect publicly disclosed vulnerabilities contained within a project’s dependencies. It does this by determining if there is a Common Platform Enumeration (CPE) identifier for a given dependency. If found, it will generate a report linking to the associated CVE entries.

A utility that identifies project dependencies and checks whether there are any known, publicly disclosed, vulnerabilities.
==- Regression Testing
Re-running functional and non-functional tests to ensure that previously developed and tested software still performs after a change. If not, that would be called a regression.
==- Source Code Analysis
Performing an analysis of the source code, byte code, and binaries.
==- Software Assurance
Encompasses the development and implementation of methods and processes for ensuring that software functions as intended while mitigating the risks of vulnerabilities, malicious code, or defects that could bring harm to the end user.
==- Software-Defined Security
Automates security controls.
==- White-Box Testing
Reviewing the source code.
===

## Overview

Security of applications must be viewed as a holistic approach in a broad context that includes not just software development considerations but also the business and regulatory context and other external factors that can affect the overall security posture of the applications being consumed by an organization.

OWASP makes several recommendations for testing:

- Identity management testing
- Authentication testing
- Authorization testing
- Session management testing
- Input validation testing
- Testing for error handling
- Testing for weak cryptography
- Business logic testing
- Client-side testing

## Types of Testing

### SAST

Source code, byte code, and binaries are all tested without executing the application. This type of testing is often used in the early stages of application development as the full application is not testable in any other way at that time. SAST is a *white-box* test, meaning that the tester has knowledge of and access to the source code.

- Performs an analysis of the source code, byte code, and binaries; SCA.
- Performed in an offline manner; SAST does *not* execute the application.

#### Uses

- Used to determine coding errors and omissions that are indicative of security vulnerabilities (XSS, SQL injection, buffer overflows, unhandled error conditions, and potential backdoors).
- SAST is often used as a test method while the tool is under development (early in the development lifecycle).
- SAST is excellent for DevOps or CI/CD (continuous integration/continuous development) environments. It is becoming the most popular option due to the growing needs of the new development era.
- SAST can help identify the following flaws:
  - Null pointer reference
  - Threading issues
  - Code quality issues
  - Issues in dead code
  - Insecure crypto functions
  - Issues in back-end application code
  - Complex injection issues
  - Issues in non-web app code

#### Advantages

- Because SAST is a white-box test, it usually delivers more results and more accuracy than DAST.

#### Goals

- Attempt to catch flaws prior to going into production.

#### Thoroughness

- SAST uses *code coverage* as a measure of how thorough testing was. For example, "SAST covered 90% of the source code."

### DAST

DAST is considered a black-box test since the code is not revealed and the test must look for problems and vulnerabilities while the application is running. The tester is not given any special information about the systems they are testing. DAST is performed on live systems.

- Must discover individual execution paths in the application.
- Used to analyze code in it's running state.

#### Uses

- DAST is most effective when testing exposed interfaces of web applications:
  - HTTP, HTML
- DAST is well-suited for waterfall environments.
- DAST can help identify the following flaws:
  - Environment configuration issues
  - Patch level issues
  - Runtime privileges issues
  - Authentication issues
  - Protocol parser issues
  - Session management issues
  - Issues in 3rd party web components
  - Malware analysis

#### Thoroughness

DAST uses *path coverage* as a measure of how thorough testing was. The objective is to test a significant sample of the possible logical paths from data input to output.

!!!
Web vulnerability testing and fuzzing are considered DAST tests.
!!!

### RASP

RASP is generally considered to focus on applications that possess self-protection capabilities built into their runtime environments, which have full insight into application logic, configuration, and data and event flows.

RASP prevents attacks by self-protecting or reconfiguring automatically without human intervention in response to certain conditions (threats, faults, and so on).

Unlike firewalls which rely solely on network data, RASP leverages the applications intrinsic knowledge of itself to accurately differentiate attacks from legitimate traffic.

### Vulnerability Assessments

Vulnerability scanning is a test that is run on systems to ensure that systems are properly hardened and there are not any *known* vulnerabilities on the system.

Most often, vulnerability assessments are performed as *white-box* tests, where the assessor knows the application and the environment the application runs in.

!!!
Any vulnerabilities not currently *known* and included in the scanning tool will remain in place and can later become zero-day exploits.
!!!

### Penetration Testing

Penetration testing is a type of test in which the tester attempts to break into systems using the same tools that an attacker would to discover vulnerabilities. These tests usually begin with a vulnerability scan to identify system weaknesses and then move on to the penetration phase.

This is a process used to collect information related to system vulnerabilities and exposures, with the view to actively exploit the vulnerabilities in the system.

Penetration testing is often a *black-box* test, in which the tester carries out the test as an attacker, has no knowledge of the application, and must discover any security issues within the application or system being tested.

!!!
To assist with targeting and focusing the scope of testing, independent parties also often perform *gray-box* testing, with only *some level of information provided*.
!!!

### Secure Code Reviews

### Open Source Review

Can detect flaws that a structured testing method might not.

### Fuzzing

Fuzzing is an automated software testing technique that involves providing invalid, unexpected, or random data as inputs to a computer program. The program is then monitored for exceptions such as crashes, or failing built-in code assertions, or for finding potential memory leaks.

Fuzzing is a type of *black-box* test.

## Threat Modeling

Threat modeling is the practice of viewing the application from the perspective of a potential attacker. In this way, threat modeling can be seen as an *application-specific* form of penetration. The idea is to identify specific points of vulnerability and then implement controls or countermeasures to protect or thwart those points from successful exploitation.

There are many ways to perform threat modeling. For instance, a vulnerability scan could be perceived as a low-level sort of threat model since attackers will be looking for the same (known) vulnerabilities that a vulnerability scan looks for.

Threat modeling also makes use of use/misuse cases. There are typically charts that display actions or functions that a user will take as well as an attacker. You then define the controls required to mitigate them.
===
