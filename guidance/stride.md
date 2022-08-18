---
categories: [Threat Models]
---

# STRIDE

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| STRIDE | Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege |

## Overview

### Introduction

STRIDE is an acronym that describes six categories of threats to software.

## Categories

The STRIDE acronym stands for:

- **S**poofing
- **T**ampering
- **R**epudiation
- **I**nformation disclosure
- **D**enial of service
- **E**levation of privilege

## Attributes

### [S]poofing

Spoofing is using someone else’s credentials to gain access to otherwise inaccessible assets. A process mounts a spoofing attack by passing forged or stolen credentials.

### [T]ampering

Tampering is changing data to mount an attack. For example, a driver might be susceptible to tampering if the required driver files are not adequately protected by driver signing and access control lists (ACLs). In this situation, a malicious user could alter the files, thus breaching system security.

### [R]epudiation

Repudiation occurs when a user denies performing an action, but the target of the action has no way to prove otherwise. A driver might be susceptible to a repudiation threat if it does not log actions that could compromise security. For example, a driver for a video device could be susceptible to repudiation if it does not log requests to change characteristics of its device, such as focus, scanned area, frequency of image capture, target location of captured images, and so forth. The resulting images could be corrupted, but system administrators would have no way to determine which user caused the problem.

### [I]nformation Disclosure

Information disclosure threats are exactly as the name implies: the disclosure of information to a user who does not have permission to see it. Any driver that passes information to or from a user buffer is susceptible to information disclosure threats. To avoid information disclosure threats, drivers must validate the length of each user buffer and zero-initialize the buffers before writing data.

### [D]enial of Service

Denial-of-service attacks threaten the ability of valid users to access resources. The resources could be disk space, network connections, or a physical device. Attacks that slow performance to unacceptable levels are also considered denial-of-service attacks. A driver that allows a user process to monopolize a system resource unnecessarily could be susceptible to a denial-of-service attack if the resource consumption hinders the ability of other valid users to perform their tasks.

### [E]levation of Privilege

An elevation-of-privilege attack can occur if an unprivileged user gains privileged status.

!!!
STRIDE is particularly useful as part of the software development lifecycle in attempting to identify vulnerabilities throughout the build process. These six concepts help in identifying and classifying threats or vulnerabilities and help form a common language used to describe them.
!!!

## Sources

!!!danger
I need to add formatting for referencing websites here.
!!!

- [Threat modeling for drivers](https://docs.microsoft.com/en-us/windows-hardware/drivers/driversecurity/threat-modeling-for-drivers). *docs.microsoft.com*.