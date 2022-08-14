---
label: Release and Deployment Management
---

# Release and Deployment Management (RDM)

## Quick Reference

| Acronym | Backronym |
| - | - |
| RDM | Release and Deployment Management |

## Overview

In one sentence, this section deals with procedures for testing, certification, accreditation, and moving to operations (including monitoring and upgrades).

Release and deployment management aims to plan, schedule, and control the movement of releases to test and live environment. The primary goal of release and deployment management is to ensure that the integrity of the live environment is protected and that the correct components are released.

Deployment management plans, schedules, and controls the movement of releases to test and live environments. Deployment management is used when a new software version needs to be released or a new system is being deployed.

## Objectives

- Define and agree upon deployment plans
- Create and test release packages
- Ensure the integrity of release packages
- Record and track all release packages in the Definitive Media Library (DML)
- Manage stakeholders
- Check delivery of utility and warranty (utility + warranty = value in the mind of the customer)
- Utility is the functionality offered by a product or service to meet a specific need; it's what the service does.
- Warranty is the assurance that a product or service will meet agreed-upon requirements (SLA); it's how the service is delivered.
- Manage risks
- Ensure knowledge transfer

### JML

=== Joiners
Are users and software licenses up to date?
=== Movers
Are software licenses being automatically re-harvested?
=== Leavers
How much are you overpaying for what you no longer need?
===

## Operational Relationships

=== Change Management
- Change management must approve any activities that release and deployment management will be engaging in prior to the release.
- Change management must approve requests to carry out the release, and then deployment management can schedule and execute the release.
=== Problem Management
If anything were to go wrong with the release, incident and problem management would need to be involved to fix whatever went wrong (if it happened once, this would be more of an incident; if it happened several times, this would be more of a problem).
=== Configuration Management
Once the release is officially live in the production environment, the existing configurations for all systems and infrastructure affected by the release have to be updated to accurately reflect their new running configurations and status within the configuration management database (CMDB).
=== Availability Management
=== If the release were not to go as planned, any negative impacts on system availability would have to be identified, monitored, and remediated as per the existing SLAs for the services and systems affected.
===
