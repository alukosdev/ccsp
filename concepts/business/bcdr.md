---
label: Business Continuity and Disaster Recovery
---

# Business Continuity and Disaster Recovery (BCDR)

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
BC | Business Continuity
BCM | Business Continuity Management
BCP | Business Continuity Plan
BIA	| Business Impact Analysis
DR | Disaster Recovery
DRP	| Disaster Recovery Plan
MAD	| Maximum Allowable Downtime
MTD	| Maximum Tolerable Downtime
RPO	| Recovery Point Objective
RSL	| Recovery Service Level
RTO	| Recovery Time Objective
WRT	| Work Recovery Time

## Glossary

=== Business Continuity (BC)
Business continuity efforts are concerned with maintaining (or "continuing") critical operations during any interruption in service.

Business continuity is defined as the capability of the organization to "continue" delivery of products or services at acceptable predefined levels following a disruptive incident. It focuses primarily on the continuity of business processes (as opposed to technical processes).
=== Business Continuity Management (BCM)
Business continuity management is the process by which risks and threats are actively reviewed and managed at set intervals as part of the overall risk management process.

BCM is defined as a holistic management process that identifies potential threats to an organization and the impacts to business operations those threats, if realized, might cause.

It provides a framework for building organizational resilience with the capability of an effective response that safeguards the interests of its key stakeholders, reputation, brand, and value-creating activities.
=== Business Continuity Plan (BCP)
The business continuity plan allows a business to plan what it needs to do to ensure that its key products and services *continue to be delivered* in case of a disaster.

Business continuity plans typically outline how to maintain or "continue" business operations back to the point of permanent operations. It allows an enterprise to plan what is necessary to ensure that its key products and services will "continue" to be available in the event of a disaster, and that disruption to the business is minimized as much as possible.

!!!
The BCP is *not* critical to the continuation of services in the event of a business interruption. BC, however, *is*. The BCP is drafted to support BC.
!!!
=== Data Replication
The process of copying data from one location to another. The system works to keep up-to-date copies of its data in the event of a disaster.
=== Disaster Recovery (DR)
Disaster recovery efforts are focused on the resumption of operations after an interruption due to disaster.

Disaster recovery is a subset of business continuity. It is the process of saving data with the sole purpose of being able to recover it in the event of a disaster. Disaster recovery includes backing up systems and IT contingency plans for critical functions and applications.

Disaster recovery focuses on *technology and data policies* (as opposed to business processes).
=== Disaster Recovery Plan (DRP)
The disaster recovery plan allows a business to plan what needs to be done immediately after a disaster to *recover from the event*.

Disaster recovery planning is the process by which suitable plans and measures are taken to ensure that, in the event of a disaster, the business can respond appropriately with the view to recovering critical and essential operations to a state of partial or full level of service in as little time as possible.

DRP is usually part of the BCP and typically tends to be more technical in nature. Addresses what needs to be accomplished during a disaster to restore business processes in order to recover from the event.
=== Enterprise Cloud Backup
Adds essential features such as archiving and disaster recovery to cloud backup solutions.
=== Functionality Replication
Used to duplicate processing capability at a secondary location. The secondary location could be with the same CSP or it could be a different CSP. It occurs anytime a needed *function*, including DNS, database, or other functionality is replicated to a CSP's other facilities.
=== Maximum Allowable Downtime (MAD)
A measure of how long it would take for an interruption in service to kill an organization. For example, if a company would fail because it had to halt operations for a week, then it's MAD is one week.

!!!
MAD is measured in *time*.
!!!
=== Maximum Tolerable Downtime (MTD)
*See [Maximum Allowable Downtime (MAD)](/concepts/business/bcdr/#maximum-allowable-downtime-mad)
=== Recovery Point Objective (RPO)
The RPO indicates the amount of acceptable data loss measured in terms of how much data can be lost before the business is too adversely affected.

The point in time at which you would like to restore to. For instance, if an organization performs daily full backups and the BCDR plan includes a goal of resuming critical operations using the last full backup, the RPO would be 24 hours.

*Data replication strategies will most affect this metric*, as the choice of strategy will determine how much recent data is available for recovery purposes.

!!!
RPO is measured in *time*.
!!!
=== Recovery Service Level (RSL)
The recovery service level is a *percentage measurement (0-100%)* of how much computing power is necessary based on the percentage of the production system needed during a disaster.

For example, an RSL of 50% would specify that the DR system would need to operate at a minimum of 50% the performance level of the normal production system.

!!!
RSL is measured in *percentage*.
!!!
=== Recovery Time Objective (RTO)
The RTO indicates the amount of system downtime defining the total time of the disaster until the business can resume operations.

This is the goal for recovery of operational capability after an interruption in service (i.e., the amount of time it takes to recover). For example, a company might have an MAD of one week, while the company's BCDR plan includes and supports an RTO of six days.

!!!
RTO is measured in *time*. The RTO must be lower than the MAD.
!!!
=== Server Replication
Concerned more about the processing system rather than the data being replicated.
=== Storage Replication
Works with a local service to store or archive data to secondary storage using a SAN. This would typically be in the same location.
=== Work Recovery Time (WRT)
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

## Considerations

=== Notification
Forms:

- Telephone call tree rosters
- Website postings
- SMS blasts

Inclusions:

- Personnel
- Public
- Regulatory and response agencies

Processes:

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

In migrating to a cloud service architecture, your organization will want to review its existing BIA and consider a new BIA, or at least a partial assessment, for cloud-specific concerns and the new risks and opportunities offered by the cloud.

BIA (link me)

Potential emergent BIA concerns include, but are not limited to, the following:

- New Dependencies
- Regulatory Failure
- Data Breach/Inadvertent Disclosure
- Vendor Lock-In/Lock-Out

### 3. Analyze

Will our plan meet the metrics specified in the previous step?

### 4. Assess

Assessing Risk (link me)

### 5. Design

Should address technical alternatives, procedures, workflow, staff, other business necessities.

### 6. Implement

Implement plan, exercising, assessing, and maintaining the plan.

### 7. Test

Any BCDR plan should be tested at *regular intervals*.

- Tabletop Exercise
- Walk-Through Drill
- Functional Drill
- Full-Interruption

There are two reasons to conduct a test of the organization's recovery from backup in an environment other than the primary production environment:

- You want to approximate contingency conditions, which includes not operating in the primary location. Assuming your facility is not available during contingency operations allows you to better simulate an emergency situation, which adds realism to the test.
- The risk of negative impact to both production and backup is too high. A recovery from backup into the production environment carries the risk of failure of both data sets (the production and the backup set).

#### Tabletop Exercise

Essential participants work together at a scheduled time to describe how they would perform their tasks in a given BCDR scenario.

!!!
This has the *least impact* on production of the testing alternatives, but is also the *least thorough*.
!!!

#### Walk-Through Drill

Simulates a disaster scenario but only includes operational and support personnel. It is more complicated than a tabletop exercise. Attendees practice certain functional steps to ensure that they have the knowledge and skills needed to complete them. Acting out the critical steps, recognizing difficulties, and resolving problems is critical for this type of test.

Moves beyond the involvement of a tabletop exercise. Chooses a specific event scenario and applies the BCP to it.

Specific characteristics include:

- Practice and validation of specific functional response capabilities
- Demonstration of knowledge as well as team interaction
- Role playing with simulated response at alternate locations
- Mobilization of the crisis management and response team
- Actual resource mobilization to reinforce the content of the plan

#### Functional Drill

Involves moving personnel to the recovery site(s) to attempt to establish communications and perform real recovery processing. The drill will help the organization determine whether following the BCP will successfully recover critical systems at an alternate processing site. Because a functional drive fully tests the BCP, all employees are involved. It demonstrates emergency management capabilities and tests procedures for evacuation, medical response, and warnings.

This test is also sometimes considered a "parallel" test. Parallel tests indicate that both the DR site and the production site are processing transactions, which results in heightened risk.

#### Full-Interruption Test

The entire organization takes part in an unscheduled, unannounced practice scenario, performing their full BCDR activities.

Provides the highest level of simulation, including notification and resource mobilization. A real-life emergency is simulated as closely as possible. It is important to properly plan this type of test to ensure that business operations are not negatively affected. This usually includes processing data and transactions using backup media at the recovery site. All employees must participate in this type of test, and all response teams must be involved.

!!!
As this could include system failover and facility evacuation, this test is the most useful for detecting shortcomings in the plan, but it has the greatest impact on productivity.
!!!

### 8. Report

### 9. Revise

## Cloud vs. Traditional

Cloud backup provides many advantages over tape-based backup:

- *Convenience*. As long as you have an Internet connection, data can be backed up as it is saved to disk. Data can be synced across multiple computers so that the data is not only backed up, but it is also instantly shared with other users.
- *Safety*. Local disasters such as fire or flood are no longer concerns.
- *Ease of Recovery*. Online backup systems can be configured to maintain multiple versions of a file. While this may be available with local backup, the ease with which different versions of a file can be restored are superior in the cloud.
- *Ease of Access*. Data can be accessed from anywhere there is an Internet connection.
Affordability. Capital expenditure is reduced as tape drives, libraries, servers, or other hardware is no longer necessary to perform the backup.

Advantages to using a cloud BC/DR include:

- Rapid elasticity
- Broad network connectivity
- On-demand self-service
- Experienced and capable staff
- Measured service

## Backup Methodologies

### Private Architecture with CSP as BC/DR

The organization maintains its own on-premise IT infrastructure and uses a CSP for BC/DR purposes.

### Cloud Operations with Primary CSP as BC/DR

The organization's infrastructure is already hosted in the cloud and they choose to use that same CSP for BC/DR purposes.

In some cases, cloud providers may offer a backup solution as a feature of their service and would ideally be located at another datacenter owned by the provider in case of a local disaster-level event.

### Cloud Operations with Third-Party CSP as BC/DR

Regular operations are hosted by the cloud provider, but contingency operations require failover to another cloud provider.

## Shared Responsibilities

### Declaration

The cloud customer and provider must decide, prior to the contingency, who specifically will be authorized to make decisions for disaster declaration and the explicit process for communicating when it has been made.

### Testing

BC/DR testing will have to be coordinated with the cloud provider. This should be planned well in advance of the scheduled testing.

## Similarities to Traditional BC/DR

### Traditional Hot Site

This would equate to an *ctive-passive* cloud model.

- In an active-passive deployment, resources are held in a secondary datacenter in standby mode. This would be similar to a hot site in the traditional DR methodology.
