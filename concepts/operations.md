# Operations

## Quick Reference

| Acronym | Backronym |
| - | - |
| BCM | Business Continuity Management |
| CI | Configuration Item |
| CSIM | Continual Service Improvement Management |
| SLM | Service Level Management |

=== Configuration Item (CI)
Configuration items can be applied to anything designated for the application of the elements of configuration management and treated as a single entity in the configuration-management system. Examples of CI types include:

- Hardware/Devices
- Software/Applications
- Communications/Networks
- Location
- Database
- Service
- Documentation
- People (Staff and Contractors)
===

## Operations Management

### Availability Management

#### Overview

Availability management aims to define, analyze, plan, measure, and improve all aspects of the availability of IT services. It is also responsibility for ensuring that all IT infrastructure, processes, tools, roles, and so on, are appropriate for the agreed-upon availability targets.

!!!
Most virtualization platforms allow for the management of system availability and can act in the event of a system outage (such as vMotion).
!!!

#### Operational Relationships

=== Release and Deployment Management
If the release were not to go as planned, any negative impacts on system availability would have to be identified, monitored, and remediated as per the existing SLAs for the services and systems affected.
===

### Business Continuity Management

#### Overview

Business continuity management *deals with planning, redundancy, criticality analysis, and sustaining the long-term operations of the business*.

BCM is focused on the planning steps that businesses engage in to ensure that their mission-critical systems are able to be restored to service following a disaster or service interruption event.

To focus BCM activities correctly, a prioritized ranking or listing of systems and services must be created and maintained. This is accomplished through the BIA, which identifies and produces a prioritized listing of systems and services critical to the normal functioning of the business.

### Capacity Management

#### Overview

Capacity management *deals with scalability and elasticity*.

Capacity management is focused on ensuring that the business IT infrastructure is adequately provisioned to deliver the agreed service-level targets in a timely and cost-effective manner.

Capacity management considers all resources required to deliver IT services within the scope of the defined business requirements. System capacity must be monitored and thresholds must be set to prevent systems from reaching an over-capacity situation.

### Change Management

#### Overview

Change management *deals with ensuring you are following the appropriate processes*.

Change management manages all changes to CIs, including any devices. All changes must be tested and formally approved prior to deployment in the live environment. It also deals with modifications to the network, such as the acquisition and deployment of new systems and components and the disposal of those taken out of service.

Change management is an approach that allows organizations to manage and control the impact of change through a structured process. The primary goal of change management is to create and implement a series of processes that allow changes to the scope of a project to be formally introduced and approved.

#### Components

##### Baselines

###### Baselining

Baselining creates a general-purpose map of the network and systems, based on the required functionality as well as security (such as required security controls)

The baseline should be a reflection of the risk appetite of the organization and provide the optimum balance of security and operational functionality.

###### Deviations and Exceptions

Deviations and exceptions to the baseline should be documented.

###### Roles and Processes

The change management process should be formalized in the organization's governance:

- Composition of the change management board
- The process
- Documentation requirements
- Instructions for requesting exceptions
- Assignment of change management tasks (validation scanning, analysis, deviation notification)
- Procedures for addressing deviations upon detection
- Enforcement measures and responsibility

The process has two forms:

- One that will occur once
- One that will occur repetitiously

The initial process should look something like this:

- *Full asset inventory*. May be aided by information pulled from other sources such as the BIA.
- *Codification of the baseline*. Can use risk management framework, enterprise and security architecture, and so on.
- *Secure baseline build*.
- *Deployment of new assets*.

In the normal operations mode, the change management process is slightly different:

- *Change management board meeting*.
- *Change management testing*.
- *Deployment*.
- *Documentation*.

##### Objectives

- Respond to a customer's changing business requirements while maximizing value and reducing incidents, disruption, and rework.
- Respond to business and IT requests for change that aligns services with business needs.
- Ensure that changes are recorded and evaluated.
- Ensure that authorized changes are prioritized, planned, tested, implemented, documented, and reviewed in a controlled manner.
- Ensure that all changes to CIs are recorded in the configuration management system.
- Optimize overall business risk. It is often correct to minimize business risk, but sometimes it is appropriate to knowingly accept a risk because of the potential benefit.

##### Process

A change-management process focused on the cloud should include policies and procedures for each of the following:

- The development and acquisition of new infrastructure and software
- Quality evaluation of new software and compliance with established security baselines
- Changing systems, including testing and deployment procedures; they should include adequate oversight of all changes
- Preventing the unauthorized installation of software and hardware

#### Functions

##### Patch Management

Patch management is a function of change management. It is the process of identifying, acquiring, installing, and verifying patches for products and systems. Patches correct security and functionality problems in software and firmware.

An applicability assessment is performed by the customer organization to determine whether a particular patch or update applies to the customer's deployment.

#### Operational Relationships

=== Configuration Management
- Change management has to approve modifications to all production systems prior to them taking place. There should never be a change that is allowed to take place to a CI in a production system unless change management has approved the change first.
- Configuration management aims to **prevent** *unauthorized changes* whereas change management aims to **allow** *changes through a formal approval process*.
=== Problem Management
- Problem management works with change management to ensure fixes are properly tested and approved. Once the fix is approved, change management will deploy the fix, and the fix will be marked as completed in both the change management and problem management processes.
=== Release and Deployment Management
- Change management must approve any activities that release and deployment management will be engaging in prior to the release.
- Change management must approve requests to carry out the release, and then deployment management can schedule and execute the release.
=== Service Level Management
- Change management must approve changes to all SLAs as well as ensure that the legal function has a chance to review them and offer guidance and direction on the nature and language of the proposed changes prior to them taking place. There should never be a change that is allowed to take place to an SLA that governs a production system unless change management has approved the change first.
===

### Configuration Management

### Continual Service Improvement Management

### Incident Management

### Information Security Management

### Problem Management

### Release and Deployment Management

### Service Level Management
