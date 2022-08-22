---
categories: [Cloud Computing Risk Management Guidance]
---

:::banner
The following page reflects information collected from the official [CWE Top 25](https://cwe.mitre.org/top25/archive/2022/2022_cwe_top25.html){ target="_blank" } released in **2022**.
:::

# CWE Top 25

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| CISA | Cybersecurity and Infrastructure Security Agency |
| CSRF | Cross-Site Request Forgery |
| CVE | Common Vulnerabilities and Exposures |
| CVSS | Common Vulnerability Scoring System |
| CWE | Common Weakness Enumeration |
| KEV | Known Exploited Vulnerabilities |
| NIST | National Institute of Standards and Technology |
| NVD | National Vulnerability Database |
| OS | Operating System |
| SQL | Structured Query Language |
| SSRF | Server-Side Request Forgery |
| XML | Extensible Markup Language |

## Overview

This list demonstrates the currently most common and impactful software weaknesses. Often easy to find and exploit, these can lead to exploitable vulnerabilities that allow adversaries to completely take over a system, steal data, or prevent applications from working.

To create the list, the CWE Team leveraged Common Vulnerabilities and Exposures (CVE) data found within the National Institute of Standards and Technology (NIST) National Vulnerability Database (NVD) and the Common Vulnerability Scoring System (CVSS) scores associated with each CVE Record, including a focus on CVE Records from the Cybersecurity and Infrastructure Security Agency (CISA) Known Exploited Vulnerabilities (KEV) Catalog. A formula was applied to the data to score each weakness based on prevalence and severity.

## Publications

| Name | Release Date |
| - | - |
| [Top 25:2022](#top-252022) | 2022 |
| Top 25:2021 | 2021 |
| Top 25:2020 | 2020 |
| Top 25:2019 | 2019 |

### Top 25:2022

| Rank | ID | Name | { class="compact" }
| - | - | - |
| 1 | CWE-787 | Out-of-bounds Write |
| 2 | CWE-79 | 	Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting') |
| 3 | CWE-89 | Improper Neutralization of Special Elements used in an SQL Command ('SQL Injection') |
| 4 | CWE-20 | Improper Input Validation |
| 5 | CWE-125 | Out-of-bounds Read |
| 6 | CWE-78 | Improper Neutralization of Special Elements used in an OS Command ('OS Command Injection') |
| 7 | CWE-416 | Use After Free |
| 8 | CWE-22 | Improper Limitation of a Pathname to a Restricted Directory ('Path Traversal') |
| 9 | CWE-352 | Cross-Site Request Forgery (CSRF) |
| 10 | CWE-434 | Unrestricted Upload of File with Dangerous Type |
| 11 | CWE-476 | NULL Pointer Dereference |
| 12 | CWE-502 | Deserialization of Untrusted Data |
| 13 | CWE-190 | Integer Overflow or Wraparound |
| 14 | CWE-287 | Improper Authentication |
| 15 | CWE-798 | Use of Hard-coded Credentials |
| 16 | CWE-862 | Missing Authorization |
| 17 | CWE-77 | Improper Neutralization of Special Elements used in a Command ('Command Injection') |
| 18 | CWE-306 | Missing Authentication for Critical Function |
| 19 | CWE-119 | Improper Restriction of Operations within the Bounds of a Memory Buffer |
| 20 | CWE-276 | Incorrect Default Permissions |
| 21 | CWE-918 | Server-Side Request Forgery (SSRF) |
| 22 | CWE-362 | Concurrent Execution using Shared Resource with Improper Synchronization ('Race Condition') |
| 23 | CWE-400 | Uncontrolled Resource Consumption |
| 24 | CWE-611 | Improper Restriction of XML External Entity Reference |
| 25 | CWE-94 | Improper Control of Generation of Code ('Code Injection') |

## Noteworthy

- [x] The CWE Top 25 contains *software weaknesses*.

## Sources

- CWE. (2022). *2022 CWE Top 25 Most Dangerous Software Weaknesses*. https://cwe.mitre.org/top25/archive/2022/2022_cwe_top25.html