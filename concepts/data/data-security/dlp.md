---
label: Data Loss Prevention
---

# Data Loss Prevention (DLP)

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
DAR | Data at Rest
DIM | Data in Motion
DIT | Data in Transit
DIU | Data in Use
DLP | Data Loss Prevention

## Glossary

=== Content Discovery
Includes the tools and processes to identify sensitive information in storage.
===

## Overview

DLP solutions are designed to protect your documents when they are *inside* your organization (unlike IRM/DRM which can protect an object anywhere it travels). It is a set of controls that is used to ensure that data is only accessible to those who should have access to it.

DLP describes the controls put in place by an organization to ensure that certain types of data (structured and unstructured) remain under organizational controls, in line with policies, standards, and procedures.

!!!
According to CSA, DLP is typically a way to monitor and protect data that your employees access via monitoring local systems, web, email, and other traffic. It is not typically used within datacenters, and thus is more applicable to SaaS than PaaS or IaaS, where it is typically not deployed.
!!!

## Components

DLP consists of three components:

==- 1. Discovery and Classification
The discovery process usually maps data in cloud storage services and databases and enables classification based on data categories (regulated data, credit card data, public data, and more).
==- 2. Monitoring
Monitors for violations.
==- 3. Enforcement
Many DLP tools provide the capability to interrogate data and compare its location, use, or transmission destination against a set of policies to prevent data loss. If a policy violation is detected, specified relevant enforcement actions can automatically be performed.

DLP policies are enforced and violations which were observed during the monitoring phase are addressed.

DLP provides the following benefits:

- Additional Security
- Policy Enforcement
- Enhanced Monitoring
- Regulatory Compliance
==-

## Types of DLP

### DAR

In order to protect DAR, DLP solutions must be deployed on each of the systems (typically as an agent) that house data, including any servers, workstations, and mobile devices.

Data at rest is mostly associated with storage.

- Storage based data
- Installed on the actual storage subsystems, file servers, or application servers

### DIM/DIT

Data in motion/data in transit is mostly associated with *network traffic*.

- Deployed near the gateway
  - Proxy, network tapping, SMTP relays
  - Requires SSL interception to inspect HTTPS traffic

### DIU

Data in use is mostly associated with *endpoints*.

- Offers insights into how users access/process data files
- More complex due to the large number of devices, users, and potential for multiple locations
