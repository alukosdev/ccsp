---
categories: [Threat Models]
---

# STRIDE

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
SDLC | Software Development Lifecycle
STRIDE | Spoofing, Tampering, Repudiation, Information Disclosure, Denial-of-Service, and Elevation of Privilege

## Overview

STRIDE is an acronym that describes six categories of threats to software.

!!!
STRIDE was developed by Microsoft.
!!!

## Categories

The STRIDE acronym stands for:

- **S**poofing
- **T**ampering
- **R**epudiation
- **I**nformation disclosure
- **D**enial-of-service
- **E**levation of privilege

==- [S]poofing

Spoofing is using someone else's credentials to gain access to otherwise inaccessible assets.

==- [T]ampering

Tampering is changing data to mount an attack.

==- [R]epudiation

Repudiation occurs when a user denies performing an action, but the target of the action has no way to prove otherwise.

==- [I]nformation disclosure

Information disclosure threats are the disclosure of information to a user who does not have permission to see it.

==- [D]enial-of-service

Denial-of-service attacks threaten the ability of valid users to access resources. The resources could be disk space, network connections, or a physical device. Attacks that slow performance to unacceptable levels are also considered denial-of-service attacks.

==- [E]levation of privilege

An elevation-of-privilege attack can occur if an unprivileged user gains privileged status.

==-

!!!
STRIDE is particularly useful as part of the software development lifecycle (SDLC) in attempting to identify vulnerabilities throughout the build process. These six concepts help in identifying and classifying threats or vulnerabilities and help form a common language used to describe them.
!!!

## Noteworthy

- [x] STRIDE contains *six* categories.
- [x] STRIDE stands for spoofing, tampering, repudiation, information disclosure, denial-of-service, and elevation of privilege.

## Sources

- https://docs.microsoft.com/en-us/windows-hardware/drivers/driversecurity/threat-modeling-for-drivers