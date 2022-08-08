# Operations

## Quick Reference

| Acronym | Backronym |
| - | - |
| BCM | Business Continuity Management |
| CI | Configuration Item |
| CSIM | Continual Service Improvement Management |
| IMT | Incident Management Team |
| IRT | IOncident Response Team |
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
=== Event
According to the ITIL framework, an event is defined as a change of state that has significance for the management of an IT service or other CI. This could be any unscheduled adverse impact to the operating environment.

Events are anything that occur in the IT framework. As a result, the term can also be used to mean an alert or notification created by an IT service, CI, or monitoring tool.

Events often require IT operations staff to take actions and lead to incidents being logged.

!!!
Not all events are incidents, but all incidents are events.
!!!

!!!
An event is distinguished form a disaster by the duration of impact. We consider events impact to last 3 days or less.
!!!
=== Incident
According to the ITIL framework, an incident is defined as an unplanned interruption to an IT service or a reduction in the quality of an IT service.

Essentially, incidents are unscheduled events.

!!!
Not all events are incidents, but all incidents are events.
!!!
===

## Operations Management

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

#### Overview

Configuration management *deals with the documentation of processes*.

Configuration management aims to maintain information about CIs required to deliver an IT service, including their relationships. Configuration management occurs when the configuration of an item, such as a network device, must be changed.

The process should include policies and procedures for each of the following:

- The development and implementation of new configurations that should apply to the hardware and software configurations of the cloud environment
- Quality evaluation of configuration changes and compliance with established security baselines
- Changing systems, including testing and deployment procedures, that should include adequate oversight of all configuration changes
- The *prevention* of any unauthorized changes in system configurations

#### Operational Relationships

=== Availability Management
- If an existing configuration were to have negative impacts on system availability, they would have to be identified, monitored, and remediated as per the existing SLAs for the services and systems affected.
=== Change Management
- Change management has to approve modifications to all production systems prior to them taking place. There should never be a change that is allowed to take place to a CI in a production system unless change management has approved the change first.
- Configuration management aims to **prevent** *unauthorized changes* whereas change management aims to **allow** *changes through a formal approval process*.
=== Release and Deployment Management
- Once the release is officially live in the production environment, the existing configurations for all systems and infrastructure affected by the release have to be updated to accurately reflect their new running configurations and status within the configuration management database (CMDB).
===

### Continual Service Improvement Management

Continual service improvement management *deals with identifying how the organization can perform more efficiently*.

Metrics on all services and processes should be collected and analyzed to find areas of improvement using a formal process. You can use various tools and standards to monitor performance. One example is the ITIL framework.

### Incident Management

#### Overview

Incident management *deals with minimizing the impact to the business*.

Incident management describes the activities of an organization to identify, analyze, and correct hazards to prevent a future reoccurrence. Incident management is typically involved in an initial attack and resolution of the attack. Identifying the root cause of the attack and deploying a fix to a known error is part of problem management.

Within a structured organization, an IRT or IMT typically addresses these types of incidents.

!!!
Incident management should be focused on the identification, classification, investigation, and resolution of an incident, with the ultimate goal of *returning the effected systems to normal as soon as possible*.
!!!

#### Purpose

- Restore normal service operation as quickly as possible
- Minimize the adverse impact on business operations
- Ensure service quality and availability are maintained

#### Objectives

- Ensure standardized methods and procedures are used for efficient and prompt response, analysis, documentation of ongoing management, and reporting of incidents
- Increase visibility and communication of incidents to business and IT support staff
- Enhance business perception of IT by using a professional approach in quickly resolving and communicating incidents when they occur
- Align incident management activities with those of the business
- Maintain user satisfaction

#### Plan

- Definitions of an incident by service type or offering
- Customer and provider roles and responsibilities for an incident
- Incident management process from detection to resolution
- Response requirements
- Media coordination
- Legal and regulatory requirements such as data breach notification

#### Incident Prioritization

Incident prioritization is made up of the following items (displayed in a matrix of 1-5 where 1 is highest and 5 is lowest).

##### Impact

Effect on the business

##### Urgency

Extent to which the resolution can be delayed

##### Priority

`Urgency * Impact`

#### Process

1. Incident Occurs
2. Incident is Reported
3. Incident is Classified
4. Investigate and Collect Data
5. Resolution
6. Approvals
7. Implement Changes
8. Review
9. Reports

### Information Security Management

#### Overview

Information security management deals with the CIA of data.

- Security management
- Security policy
- Information security organization
- Asset management
- Human resources security
- Physical and environmental security
- Communications and operations management
- Access control
- Information systems acquisition, development, and maintenance
- Provider and customer responsibilities

!!!
This section looks much like what you'd see as the foundation for ISO 27001 as part of the ISMS (Information Security Management System or Program).
!!!

### Problem Management



### Release and Deployment Management

### Service Level Management
