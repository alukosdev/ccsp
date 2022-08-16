---
categories: [Data Center Design Standards]
---

# Uptime Institute

## Overview

The Uptime Institute is an advisory organization for matters related to IT service. UI publishes a standard for datacenter design, and it also certifies datacenters for compliance with this standard.

## Components

The UI standard is split into four tiers, in ascending durability of the datacenter.

### Tier 1

Tier 1 is a simplistic datacenter, with little or no redundancy and is labeled `Basic Site Infrastructure`.

#### Minimum Requirements

- Dedicated space for IT systems
- An uninterruptable power supply (UPS) system for line conditioning and backup purposes
- Sufficient cooling systems to serve all critical equipment
- A power generator for extended electrical outages, with at least 12 hours of fuel to run the generator at sufficient load to power the IT systems

#### Features

- Scheduled maintenance will require systems (including critical systems) to be taken offline.
- Both planned and unplanned maintenance and response activity may take systems (including critical systems) offline.
- Untoward personnel activity (both inadvertent and malicious) will result in downtime.
- Annual maintenance is necessary to safely operate the datacenter and requires full shutdown (including critical systems). Without this maintenance, the datacenter is likely to suffer increased outages and disruptions.

### Tier 2

Tier 2 is slightly more robust than Tier 1 and is named `Redundant Site Infrastructure Capacity Components`. It features all the attributes of the Tier 1 design, with additional elements.

#### Additional Features

- Critical operations do not have to be interrupted for scheduled replacement and maintenance of any of the redundant components; however, there may be downtime for any disconnection of power distribution systems and lines.
- Contrary to Tier 1, where untoward personnel activity will cause downtime, in Tier 2 it may cause downtime.
- Unplanned failures of components or systems might result in downtime.

### Tier 3

The Tier 3 design is known as a `Concurrently Maintainable Site Infrastructure`. The facility features both the redundant capacity components of a Tier 2 build and the added benefit of multiple distribution paths.

#### Additional Features

- There are dual power supplies for all IT systems.
- Critical operations can continue even if any single component or power element is out of service for scheduled maintenance ore replacement.
- Unplanned loss of a component may cause downtime; the loss of a single system, on the other hand, will cause downtime.
- Planned maintenance will not necessarily result in downtime; however, the risk of downtime may be increased during this activity. This temporary elevated risk does not make the datacenter lose its Tier 3 rating for the duration.

### Tier 4

The Tier 4 design is known as a `Fault-Tolerant Site Infrastructure`. Each and every element and system of the facility has integral redundancy such that critical operations can survive both planned and unplanned downtime at the loss of any component or system.

#### Additional Features

- There is redundancy of both IT and electrical components, where the various multiple components are independent and physically separate from each other.
- Even after the loss of any facility infrastructure element, there will be sufficient power and cooling for critical operations.
- The loss of any single system, component, or distribution element will not affect critical operations.
- The facility will feature automatic response capabilities for infrastructure control systems such that the the critical operations will not be affected by astructure failures.
- Any single loss, even, or personnel activity will not cause downtime of critical operations.
- Scheduled maintenance can be performed without affecting critical operations. However, while one set of assets is in the maintenance state, the datacenter may be at increased risk of failure due to an event affecting the alternate assets. During this temporary maintenance state, the facility does not lose its Tier 4 rating.