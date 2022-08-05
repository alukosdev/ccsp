# BCDR

## Quick Reference

| Acronym | Backronym |
| - | - |
| BC | Business Continuity |
| BCM | Business Continuity Management |
| BCP | Business Continuity Plan |
| BIA	| Business Impact Analysis |
| DR | Disaster Recovery |
| DRP	| Disaster Recovery Plan |
| MAD	| Maximum Allowable Downtime |
| MTD	| Maximum Tolerable Downtime |
| RPO	| Recovery Point Objective |
| RSL	| Recovery Service Level |
| RTO	| Recovery Time Objective |
| WRT	| Work Recovery Time |

=== Business Continuity
Business continuity efforts are concerned with maintaining (or "continuing") critical operations during any interruption in service.

Business continuity is defined as the capability of the organization to "continue" delivery of products or services at acceptable predefined levels following a disruptive incident. It focuses primarily on the continuity of business processes (as opposed to technical processes).
=== Business Continuity Management
Business continuity management is the process by which risks and threats are actively reviewed and managed at set intervals as part of the overall risk management process.

BCM is defined as a holistic management process that identifies potential threats to an organization and the impacts to business operations those threats, if realized, might cause.

It provides a framework for building organizational resilience with the capability of an effective response that safeguards the interests of its key stakeholders, reputation, brand, and value-creating activities.
=== Business Continuity Plan
The business continuity plan allows a business to plan what it needs to do to ensure that its key products and services *continue to be delivered* in case of a disaster.

Business continuity plans typically outline how to maintain or "continue" business operations back to the point of permanent operations. It allows an enterprise to plan what is necessary to ensure that its key products and services will "continue" to be available in the event of a disaster, and that disruption to the business is minimized as much as possible.

!!!
The BCP is *not* critical to the continuation of services in the event of a business interruption. BC, however, *is*. The BCP is drafted to support BC.
!!!
=== Data Replication
The process of copying data from one location to another. The system works to keep up-to-date copies of its data in the event of a disaster.
=== Disaster Recovery
Disaster recovery efforts are focused on the resumption of operations after an interruption due to disaster.

Disaster recovery is a subset of business continuity. It is the process of saving data with the sole purpose of being able to recover it in the event of a disaster. Disaster recovery includes backing up systems and IT contingency plans for critical functions and applications.

Disaster recovery focuses on *technology and data policies* (as opposed to business processes).
=== Disaster Recovery Plan
The disaster recovery plan allows a business to plan what needs to be done immediately after a disaster to *recover from the event*.

Disaster recovery planning is the process by which suitable plans and measures are taken to ensure that, in the event of a disaster, the business can respond appropriately with the view to recovering critical and essential operations to a state of partial or full level of service in as little time as possible.

DRP is usually part of the BCP and typically tends to be more technical in nature. Addresses what needs to be accomplished during a disaster to restore business processes in order to recover from the event.
=== Enterprise Cloud Backup
Adds essential features such as archiving and disaster recovery to cloud backup solutions.
=== Functionality Replication
Used to duplicate processing capability at a secondary location. The secondary location could be with the same CSP or it could be a different CSP. It occurs anytime a needed *function*, including DNS, database, or other functionality is replicated to a CSP's other facilities.
=== MAD/MTD
A measure of how long it would take for an interruption in service to kill an organization. For example, if a company would fail because it had to halt operations for a week, then it's MAD is one week.

!!!
MAD is measured in *time*.
!!!
=== RTO
The RTO indicates the amount of system downtime defining the total time of the disaster until the business can resume operations.

This is the goal for recovery of operational capability after an interruption in service (i.e., the amount of time it takes to recover). For example, a company might have an MAD of one week, while the company's BCDR plan includes and supports an RTO of six days.

!!!
RTO is measured in *time*. The RTO must be lower than the MAD.
!!!
=== RPO
The RPO indicates the amount of acceptable data loss measured in terms of how much data can be lost before the business is too adversely affected.

The point in time at which you would like to restore to. For instance, if an organization performs daily full backups and the BCDR plan includes a goal of resuming critical operations using the last full backup, the RPO would be 24 hours.

*Data replication strategies will most affect this metric*, as the choice of strategy will determine how much recent data is available for recovery purposes.

!!!
RPO is measured in *time*.
!!!
=== RSL
The recovery service level is a *percentage measurement (0-100%)* of how much computing power is necessary based on the percentage of the production system needed during a disaster.

For example, an RSL of 50% would specify that the DR system would need to operate at a minimum of 50% the performance level of the normal production system.

!!!
RSL is measured in *percentage*.
!!!
=== Server Replication
Concerned more about the processing system rather than the data being replicated.
=== Storage Replication
Works with a local service to store or archive data to secondary storage using a SAN. This would typically be in the same location.
=== WRT
The time necessary to very restoration of systems once they have been returned to operation.
===

## Overview

BC/DR protects against the risk of data not being available and the risk that the business processes that it supports are not functional, leading to adverse consequences for the organization. The analysis of this risk leads to the business requirements for BC/DR.

BC/DR starts at risk management since all security decisions are based on risk/risk management. We look at the assets and what they're worth, threats/vulnerabilities, potential for loss versus the cost of the countermeasures. This also helps us identify our critical assets to protect and prioritize. The BIA helps us define our critical assets.

Any BC/DR plan should include the following:

- Required capability and capacity of backup systems
- Trigger events to implement the plan
- Clearly defined roles and responsibilities by name and title
- Clearly defined continuity and recovery procedures
- Notification requirements

!!!
In DR terms, `RTO + WRT < MTD`.
!!!

## Comsiderations

=== Notification
### Forms

- Telephone call tree rosters
- Website postings
- SMS blasts

### Inclusions

- Personnel
- Public
- Regulatory and response agencies

### Processes

- Getting the People Out
- Getting the People Out Safely
- Designing for Protection
=== Continuity
We have to determine what the organization's critical operations are. In a cloud datacenter, that will usually be dictated by the customer contracts and SLAs. The BIA is extremely useful in this portion of the effort, since it informs us which assets would cause the greatest adverse impact if lost or interrupted.
=== Plan
The authors are big fans of checklists.

- A list of the Items from the Asset Inventory Deemed Critical
- The Circumstances Under Which an Event or Disaster is Declared
- Who is Authorized to Make the Declaration
- Essential Points of Contact
- Detailed Actions, Tasks, and Activities

The plan should be reviewed at least once per year, or as risk dictates.
=== Kit
There should be a container that holds all the necessary documentation and tools to conduct a proper BC/DR response action.

- A current copy of the plan
- Emergency and backup communication equipment
- Copies of all appropriate network and infrastructure diagrams and architecture
- Copies of all software for creating a clean build and media containing appropriate patches for current versioning
- Emergency contact information
- Documentation tools and equipment
- Emergency essentials (flashlight, water, rations, batteries)
=== Relocation
- HR and finance should be involved since travel arrangements and payments will be required
- Families should be considered
- Distance needs to be out of impact zone but close enough to not make expenses too high
- Joint operating agreements in the instance that the disaster only affects your organization's campus
=== Power
- UPS (near-term)
- Generators (short-term)
  - Minimum 12 hours of fuel
  - Should anticipate at least 72 hours
=== Strategy
- Location
- Data Replication
- Functionality Replication
- Planning, Preparing, and Provisioning
- Failover Capability
- Returning to Normal
- Testing and Acceptance to Production
=== Risks
- Changes in location
- Maintaining redundancy
- Having proper failover mechanisms
- Having the ability to bring services online quickly
- Having functionality with external services

!!!
Budget is *not* a risk since it should be something that is already factored in and accounted for.
!!!
===

## Planning

### 1. Define Scope

### 2. Gather Requirements

### 3. Analyze

### 4. Assess

### 5. Design

### 6. Implement

### 7. Test

### 8. Report

### 9. Revise

## Cloud vs. Traditional

## Backup Methodologies

## Shared Responsibilities

## Similarities to Traditional BC/DR
