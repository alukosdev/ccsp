---
icon: quote
order: 1100
---

# Glossary

!!!danger
Should this page should be updated to contain both the word as well as the hyphenised acronym? Or should it just contain the acronym and then the definition can contain the word with the hypenised acronym?
!!!

## A

==- Agreed-Upon Procedures (AUP)
An agreed-upon procedure is a standard a company or client outlines when it hires an external party to perform an audit on a specific test or business process. The procedures, which are called audit standards, are designed and agreed upon by the entity conducting the audit, as well as any appropriate third parties.

The auditor does not provide an opinion; rather, the entities or third parties form their own conclusions based on the report.
==- Auditability
Auditability is collecting and making available necessary evidence related to the operation and use of the cloud.
==-

## B

#### Bastion Host

A bastion host is a method for remote access to a secure environment. The bastion host is an extremely hardened device that is typically focused on providing access to one application or for one particular usage. Having the device set up in this focused manner makes hardening it more effective. Bastion hosts are made publicly available on the Internet.

:::
The difference between a jump server and a bastion host is that a jump server is intended to breach the gap between two security zones and have a gateway to obtain access to something inside of the other security zone. A bastion host is outside of your security zone and will require additional security considerations.
:::

==- Business Continuity (BC)
Business continuity efforts are concerned with maintaining (or "continuing") critical operations during any interruption in service.

Business continuity is defined as the capability of the organization to "continue" delivery of products or services at acceptable predefined levels following a disruptive incident. It focuses primarily on the continuity of business processes (as opposed to technical processes).
==- Business Continuity Management (BCM)
Business continuity management is the process by which risks and threats are actively reviewed and managed at set intervals as part of the overall risk management process.

BCM is defined as a holistic management process that identifies potential threats to an organization and the impacts to business operations those threats, if realized, might cause.

It provides a framework for building organizational resilience with the capability of an effective response that safeguards the interests of its key stakeholders, reputation, brand, and value-creating activities.
==- Business Continuity Plan (BCP)
The business continuity plan allows a business to plan what it needs to do to ensure that its key products and services *continue to be delivered* in case of a disaster.

Business continuity plans typically outline how to maintain or "continue" business operations back to the point of permanent operations. It allows an enterprise to plan what is necessary to ensure that its key products and services will "continue" to be available in the event of a disaster, and that disruption to the business is minimized as much as possible.

!!!
The BCP is *not* critical to the continuation of services in the event of a business interruption. BC, however, *is*. The BCP is drafted to support BC.
!!!
==-

## C

#### Capability Maturity Model \(CMM\)

A way of determining a target's maturity in terms of **process** documentation and repeatability. Contains five levels. Is typically not associated with security, however.

#### Confidentiality

Protecting information from unauthorized access/dissemination.

#### Controls

Act as mechanisms designed to restrict a list of possible actions to allowed or permitted actions. If a control is breached, the next step of mitigating is a countermeasure. Proactive.

#### Cost Benefit Analysis

A cost-benefit analysis \(CBA\) is the process used to measure the benefits of a decision or taking action minus the costs associated with taking that action. It determines whether certain activities \(such as BC/DR\) are worth implementing. The CBA will compare the costs of a disaster and the impact of downtime against the cost of implementing the BCDR solution. Another example would be whether the movement to a cloud model would be lower than the cost of not moving to the cloud.

#### Countermeasure

Countermeasures are what is deployed once a control has been breached. Reactive.

#### Cross-Cutting Aspects

Cross-cutting aspects are behaviors or capabilities which need to be coordinated across roles and implemented consistently in a cloud computing system.

An example of a cross-cutting aspect is security.

## D

#### Data Remanence

Any data left over after sanitization and disposal methods have been attempted.

==- Data Replication
The process of copying data from one location to another. The system works to keep up-to-date copies of its data in the event of a disaster.
==-

#### Demand Management

Can we meet our demand requirements \(can we scale up and down\)? Elasticity in the cloud solves this.

#### Digital Signatures

Uses the senders private key *and* a hash to guarantee the integrity and the origin \(authenticity/non-repudiation\) of a message. This method requires a PKI.

==- Disaster Recovery (DR)
Disaster recovery efforts are focused on the resumption of operations after an interruption due to disaster.

Disaster recovery is a subset of business continuity. It is the process of saving data with the sole purpose of being able to recover it in the event of a disaster. Disaster recovery includes backing up systems and IT contingency plans for critical functions and applications.

Disaster recovery focuses on technology and data policies (as opposed to business processes).
==- Disaster Recovery Plan (DRP)
The disaster recovery plan allows a business to plan what needs to be done immediately after a disaster to *recover from the event*.

Disaster recovery planning is the process by which suitable plans and measures are taken to ensure that, in the event of a disaster, the business can respond appropriately with the view to recovering critical and essential operations to a state of partial or full level of service in as little time as possible.

DRP is usually part of the BCP and typically tends to be more technical in nature. Addresses what needs to be accomplished during a disaster to restore business processes in order to recover from the event.
==-

## E

#### Enterprise Application

Applications or software that a business would use to assist the organization in solving enterprise problems.

==- Enterprise Cloud Backup
Adds essential features such as archiving and disaster recovery to cloud backup solutions.
==-

#### European Economic Area \(EEA\)

The European Economic Area, abbreviated as EEA, consists of the Member States of the European Union \(EU\) and three countries of the European Free Trade Association \(EFTA\) \(Iceland, Liechtenstein and Norway; excluding Switzerland\). The Agreement on the EEA entered into force on 1 January 1994.

## F

#### Fault Tolerance

Fault tolerance involves the use of specialized hardware that can detect faults and automatically switch to redundant components or systems.

:::
Should be used when the goal is to **eliminate** system downtime as a threat to system availability altogether.
:::

#### Financial Management

Do we have the funds and can we allocate them appropriately? Are we receiving a good return on investment \(ROI\)? Are we good stewards of the money entrusted to us? Are we making a profit?

#### Fraggle Attack

A variation to the Smurf attack is the Fraggle attack. The attack is essentially the same as the Smurf attack but instead of sending an ICMP echo request to the direct broadcast address, it sends UDP packets.

==- Functionality Replication
Used to duplicate processing capability at a secondary location. The secondary location could be with the same CSP or it could be a different CSP. It occurs anytime a needed *function*, including DNS, database, or other functionality is replicated to a CSP's other facilities.
==-

## G

==- Gap Analysis
To create an accurate frame of reference, a gap analysis is conducted. This is like a lightweight audit in that there are generally findings of weaknesses or vulnerabilities, but the purpose is to identify those weaknesses so they can be remediated prior to any actual audit work. It also provides a starting point for those organizations in the early stages of an information system program development, providing them with a clear starting point.

Gap analysis benchmarks and identifies relevant gaps against specified frameworks or standards. This includes reviewing the organization's current position/performance as revealed by an audit against a given standard.

The value of such an assessment is often determined based on what you did not know or for an independent resource to communicate to relevant management or senior personnel such risks, as opposed to internal resources saying what you need or should be doing.

Typically, resources or personnel who are not engaged or functioning within the area of scope perform gap analysis. The use of independent or impartial resources is best served to ensure there are no conflicts or favoritism. Perspectives gained from people outside the audit target are invaluable because they may see possibilities and opportunities revealed by the audit, whereas the personnel in the target department may be constrained by habit and tradition.
==-

#### Generally Accepted Accounting Practices \(GAAP\)

GAAP is a combination of authoritative standards \(set by policy boards\) and the commonly accepted ways of recording and reporting accounting information. GAAP aims to improve the clarity, consistency, and comparability of the communication of financial information.

These are the industry standards, also recognized by the courts and regulators, that accountants and auditors must adhere to in professional practice. Many of these deal with elements of the CIA Triad, but they also include aspects such as conflict of interest, client privacy, and so forth.

A standard framework of guidelines for financial accounting.

#### Geofence

A geofence is a virtual perimeter for a real-world geographic area.

## H

#### Hashing

Able to detect corruption.

#### High Availability

High availability makes use of shared and pooled resources to maintain a high level of availability and minimize downtime. It typically includes the following capabilities:

- Live recovery
- Automatic migration

:::
Should be used when the goal is to **minimize** the impact of system downtime.
:::

## I

#### Inference

An attack technique that derives sensitive material from an aggregation of innocuous data.

#### Integrity

The process of ensuring that data is real, accurate, and protected from unauthorized modification.

#### IT Service Management \(ITSM\)

The activities that are performed by an organization to design, plan, deliver, operate and control IT services offered to customers.

ITSM makes it possible to:

- Ensure portfolio management, demand management, and financial management are all working together for efficient service delivery to customers and effective charging for services if appropriate
- Involve all the people and systems necessary to create alignment and ultimately success

## J

#### Jump Server

A jump server, jump host or jump box is a system on a network used to access and manage devices in a separate security zone. A jump server is a hardened and monitored device that spans two dissimilar security zones and provides a controlled means of access between them. The most common example is managing a host in a DMZ from trusted networks or computers.

:::
The difference between a jump server and a bastion host is that a jump server is intended to breach the gap between two security zones and have a gateway to obtain access to something inside of the other security zone. A bastion host is outside of your security zone and will require additional security considerations.
:::

## K

## L

## M

==- Maximum Allowable Downtime (MAD)/Maximum Tolerable Downtime (MTD)
A measure of how long it would take for an interruption in service to kill an organization. For example, if a company would fail because it had to halt operations for a week, then it's MAD is one week.

!!!
MAD is measured in *time*.
!!!
==-

#### Microsoft Best Practice Analyzers \(BPA\)

#### Microsoft Deployment Toolkit \(MDT\)

Microsoft Deployment Toolkit is a computer program that permits network deployment of Microsoft Windows and Microsoft Office.

#### Middleware

A term used to describe software that works between an operating system and another application or database of some sort. Typically operates above the transport layer and below the application layer.

## N

#### NERC CIP

The NERC \(North American Electric Reliability Corporation\) CIP \(Critical Infrastructure Plan\) is a set of requirements designed to secure the assets required for operating North America's bulk electric system.

#### Nonrepudiation

The assurance that a specific author actually did create and send a specific item to a specific recipient and that it was successfully received. The sender of the message cannot later credibly deny having sent the message, nor can the recipient credibly claim not to have received it.

## O

#### Outage Duration

Outage duration is the length of time of a documented outage and is expressed as an amount of time \(minutes, hours, days\).

## P

#### Portfolio Management

A portfolio consists of all endeavors undertaken by an organization. We are looking to show value for each individual endeavor but also the IT program as a whole. For example, are we receiving the value from cloud services that we're looking for?

## Q

#### Quantum Computing

A theoretical technology which allows superposition of physical states to increase both computing capacity and encryption keyspace.

## R

#### Record

A data structure or collection of information that is retained by an organization for legal, regulator, or business reasons.

==- Recovery Point Objective (RPO)
The RPO indicates the amount of acceptable data loss measured in terms of how much data can be lost before the business is too adversely affected.

The point in time at which you would like to restore to. For instance, if an organization performs daily full backups and the BCDR plan includes a goal of resuming critical operations using the last full backup, the RPO would be 24 hours.

*Data replication strategies will most affect this metric*, as the choice of strategy will determine how much recent data is available for recovery purposes.
!!!
RPO is measured in *time*.
!!!
==- Recovery Time Objective (RTO)
The RTO indicates the amount of system downtime defining the total time of the disaster until the business can resume operations.

This is the goal for recovery of operational capability after an interruption in service (i.e., the amount of time it takes to recover). For example, a company might have an MAD of one week, while the company's BCDR plan includes and supports an RTO of six days.

!!!
RTO is measured in *time*. The RTO must be lower than the MAD.
!!!
==- Recovery Service Level (RSL)
The recovery service level is a *percentage measurement (0-100%)* of how much computing power is necessary based on the percentage of the production system needed during a disaster.

For example, an RSL of 50% would specify that the DR system would need to operate at a minimum of 50% the performance level of the normal production system.

!!!
RSL is measured in *percentage*.
!!!
==-

#### Return on Investment

A term used to describe a profitability ratio.

Generally calculated by dividing net profit by net assets.

## S

#### Sandboxing

- Testing untested or untrusted code
- To better understand if an application is working the way it was intended to work

#### Separation of Duties

Dictates that one person/entity cannot complete an entire transaction alone.

In the case of encryption, a single entity should not be able to administer the issuing of keys, encrypt the data, and store the keys, because this could lead to a situation where that entity has the ability to access or take encrypted data.

==- Server Replication
Concerned more about the processing system rather than the data being replicated.
==-

#### Service Oriented Architecture \(SOA\)

Views software as a combination of interoperable services, the components of which can be substituted at will.

#### Severity Assessment

Performed by the customer organization to determine the importance of a particular patch or update.

#### Shadow IT

Money spent on technology to acquire services without the IT department's dollars or knowledge.

For example, on-demand self service promotes and allows the ability to provision computing resources without human interaction, The consumer can provision resources regardless of location and time. This can be a challenge to purchasing departments as the typical purchasing processes can be avoided.

#### Silos

The configuration when an enterprise deploys applications in dedicated infrastructure.

Having silos in an enterprise deployment could be a precursor to migrating the environments to the cloud.

#### Smurf Attack

The Smurf attack is a distributed denial-of-service attack in which large numbers of Internet Control Message Protocol \(ICMP\) packets with the intended victim’s spoofed source IP are broadcast to a computer network using an IP broadcast address. Most devices on a network will, by default, respond to this by sending a reply to the source IP address. If the number of machines on the network that receive and respond to these packets is very large, the victim’s computer will be flooded with traffic.

==- Storage Replication
Works with a local service to store or archive data to secondary storage using a SAN. This would typically be in the same location.
==-

## T

#### Trust Zones/Security Zones

A trust zone is a network segment within which data flows relatively freely, whereas data flowing in and out of the trust zone is subject to stronger restrictions. These could be physical, logical, or virtual boundaries around network resources, such as:

- DMZ \(semi-trusted\)
- Department-specific zones/site-specific zones
- Application-defined zones \(such as web application tiers\)

Before a cloud provider can implement trust zones, they must undergo threat and vulnerability assessments to determine where their weaknesses are within the environment. This will help to determine where trust zones would be most helpful.

When controls implemented by the virtualization components are deemed to be not strong enough, trust zones can be used to segregate the physical infrastructure.

To protect trust zones:

- Implement granular role-based controls on traffic, users, and assets
- Manage inter-zone communications including between sub-zones
- Enforce policy and regulations
- Protect, detect, and contain

![Trust Zones](/static/trust-zones.png)

## U

## V

## W

#### Wassenaar Arrangement

 The **Wassenaar** Arrangement, formally established in July 1996, is a voluntary export control regime whose 42 members exchange information on transfers of conventional weapons and dual-use goods and technologies. This includes import restrictions and data sharing.

#### Write Once, Read Many \(WORM\)

A type of long-term storage, meaning it is written to initially and only used for read purposes thereafter.

==- WRT
The time necessary to very restoration of systems once they have been returned to operation.
==-

## X

## Y

## Z
