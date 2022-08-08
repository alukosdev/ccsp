---
label: Operations > Change Management
---

# Change Management

## Summary

Change management *deals with ensuring you are following the appropriate processes*.

Change management manages all changes to CIs, including any devices. All changes must be tested and formally approved prior to deployment in the live environment. It also deals with modifications to the network, such as the acquisition and deployment of new systems and components and the disposal of those taken out of service.

Change management is an approach that allows organizations to manage and control the impact of change through a structured process. The primary goal of change management is to create and implement a series of processes that allow changes to the scope of a project to be formally introduced and approved.

## Components

### Baselines

#### Baselining

Baselining creates a general-purpose map of the network and systems, based on the required functionality as well as security (such as required security controls)

The baseline should be a reflection of the risk appetite of the organization and provide the optimum balance of security and operational functionality.

#### Deviations and Exceptions

Deviations and exceptions to the baseline should be documented.

#### Roles and Processes

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

### Objectives

- Respond to a customer's changing business requirements while maximizing value and reducing incidents, disruption, and rework.
- Respond to business and IT requests for change that aligns services with business needs.
- Ensure that changes are recorded and evaluated.
- Ensure that authorized changes are prioritized, planned, tested, implemented, documented, and reviewed in a controlled manner.
- Ensure that all changes to CIs are recorded in the configuration management system.
- Optimize overall business risk. It is often correct to minimize business risk, but sometimes it is appropriate to knowingly accept a risk because of the potential benefit.

### Process

A change-management process focused on the cloud should include policies and procedures for each of the following:

- The development and acquisition of new infrastructure and software
- Quality evaluation of new software and compliance with established security baselines
- Changing systems, including testing and deployment procedures; they should include adequate oversight of all changes
- Preventing the unauthorized installation of software and hardware

## Functions

### Patch Management

Patch management is a function of change management. It is the process of identifying, acquiring, installing, and verifying patches for products and systems. Patches correct security and functionality problems in software and firmware.

An applicability assessment is performed by the customer organization to determine whether a particular patch or update applies to the customer's deployment.

## Operational Relationships

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
