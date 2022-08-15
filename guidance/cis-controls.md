---
categories: [Security Management and Controls]
tags: [cis]
---

!!!danger
This page is currently being updated for the 2022 version of the CCSP exam.
!!!

# CIS Controls

## Acronyms

| Acronym | Backronym |
| - | - |
| CIS | Center for Internet Security |
| CSC | Critical Security Controls (formerly) |

## Overview

The CIS Controls (formerly known as Critical Security Controls) are a recommended set of actions for cyber defense that provide specific and actionable ways to stop today's most pervasive and dangerous attacks.[¹]

## Controls

:::banner
The following CIS Controls are derived from the official CIS Critical Security Controls, Version 8, released **May 18, 2021**.
:::

| Control Number | Control Name |
| - | - |
| Control 01 | Inventory and Control of Enterprise Assets |
| Control 02 | Inventory and Control of Software Assets |
| Control 03 | Data Protection |
| Control 04 | Secure Configuration of Enterprise Assets and Software |
| Control 05 | Account Management |
| Control 06 | Access Control Management |
| Control 07 | Continuous Vulnerability Management |
| Control 08 | Audit Log Management |
| Control 09 | Email and Web Browser Protections |
| Control 10 | Malware Defenses |
| Control 11 | Data Recovery |
| Control 12 | Network Infrastructure Management |
| Control 13 | Network Monitoring and Defense |
| Control 14 | Security Awareness and Skills Training |
| Control 15 | Service Provider Management |
| Control 16 | Application Software Security |
| Control 17 | Incident Response Management |
| Control 18 | Penetration Testing |

!!!info
An underlying theme for these controls is support for large-scale, standards-based security automation for the management of cyber defenses.
!!!

### CIS CSC 2

#### Effectiveness Metrics

When testing the effectiveness of the automated implementation of this control, organizations should determine the following:

- The amount of time it takes to detect new software installed on the organization's systems
- The amount of time it takes the scanning functions to alert the organization's administrators when an unauthorized application has been discovered on a system
- The amount of time it takes for an alert to be generated when a new application has been discovered on a system
- Whether the scanning function identifies the department, location, and other critical details about the unauthorized software that has been detected

#### Automation Metrics

Organizations should gather the following information to automate the collection of relevant data from these systems:

- The total number of unauthorized applications located on the organization's business systems
- The average amount of time it takes to remove unauthorized applications from the organization's business systems
- The total number of the organization's business systems that are not running whitelisting software
- The total number of applications that have been recently blocked

## References

1. https://www.sans.org/blog/cis-controls-v8/