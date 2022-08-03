# Terminology

## A-C

### B

#### Bastion Host

A bastion host is a method for remote access to a secure environment. The bastion host is an extremely hardened device that is typically focused on providing access to one application or for one particular usage. Having the device set up in this focused manner makes hardening it more effective. Bastion hosts are made publicly available on the Internet.

:::info
The difference between a jump server and a bastion host is that a jump server is intended to breach the gap between two security zones and have a gateway to obtain access to something inside of the other security zone. A bastion host is outside of your security zone and will require additional security considerations.
:::

### C

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

## D-F

### D

#### Data Remanence

Any data left over after sanitization and disposal methods have been attempted.

#### Demand Management

Can we meet our demand requirements \(can we scale up and down\)? Elasticity in the cloud solves this.

#### Digital Signatures

Uses the senders private key *and* a hash to guarantee the integrity and the origin \(authenticity/non-repudiation\) of a message. This method requires a PKI.

### E

#### Enterprise Application

Applications or software that a business would use to assist the organization in solving enterprise problems.

#### European Economic Area \(EEA\)

The European Economic Area, abbreviated as EEA, consists of the Member States of the European Union \(EU\) and three countries of the European Free Trade Association \(EFTA\) \(Iceland, Liechtenstein and Norway; excluding Switzerland\). The Agreement on the EEA entered into force on 1 January 1994.

### F

#### Fault Tolerance

Fault tolerance involves the use of specialized hardware that can detect faults and automatically switch to redundant components or systems.

:::info
Should be used when the goal is to **eliminate** system downtime as a threat to system availability altogether.
:::

#### Financial Management

Do we have the funds and can we allocate them appropriately? Are we receiving a good return on investment \(ROI\)? Are we good stewards of the money entrusted to us? Are we making a profit?

#### Fraggle Attack

A variation to the Smurf attack is the Fraggle attack. The attack is essentially the same as the Smurf attack but instead of sending an ICMP echo request to the direct broadcast address, it sends UDP packets.

## G-I

### G

#### Generally Accepted Accounting Practices \(GAAP\)

GAAP is a combination of authoritative standards \(set by policy boards\) and the commonly accepted ways of recording and reporting accounting information. GAAP aims to improve the clarity, consistency, and comparability of the communication of financial information.

These are the industry standards, also recognized by the courts and regulators, that accountants and auditors must adhere to in professional practice. Many of these deal with elements of the CIA Triad, but they also include aspects such as conflict of interest, client privacy, and so forth.

A standard framework of guidelines for financial accounting.

#### Geofence

A geofence is a virtual perimeter for a real-world geographic area.

### H

#### Hashing

Able to detect corruption.

#### High Availability

High availability makes use of shared and pooled resources to maintain a high level of availability and minimize downtime. It typically includes the following capabilities:

- Live recovery
- Automatic migration

:::info
Should be used when the goal is to **minimize** the impact of system downtime.
:::

### I

#### Inference

An attack technique that derives sensitive material from an aggregation of innocuous data.

#### Integrity

The process of ensuring that data is real, accurate, and protected from unauthorized modification.

#### IT Service Management \(ITSM\)

The activities that are performed by an organization to design, plan, deliver, operate and control IT services offered to customers.

ITSM makes it possible to:

- Ensure portfolio management, demand management, and financial management are all working together for efficient service delivery to customers and effective charging for services if appropriate
- Involve all the people and systems necessary to create alignment and ultimately success

## J-L

### J

#### Jump Server

A jump server, jump host or jump box is a system on a network used to access and manage devices in a separate security zone. A jump server is a hardened and monitored device that spans two dissimilar security zones and provides a controlled means of access between them. The most common example is managing a host in a DMZ from trusted networks or computers.

:::info
The difference between a jump server and a bastion host is that a jump server is intended to breach the gap between two security zones and have a gateway to obtain access to something inside of the other security zone. A bastion host is outside of your security zone and will require additional security considerations.
:::

## M-O

### M

#### Microsoft Best Practice Analyzers \(BPA\)

#### Microsoft Deployment Toolkit \(MDT\)

Microsoft Deployment Toolkit is a computer program that permits network deployment of Microsoft Windows and Microsoft Office.

#### Middleware

A term used to describe software that works between an operating system and another application or database of some sort. Typically operates above the transport layer and below the application layer.

### N

#### NERC CIP

The NERC \(North American Electric Reliability Corporation\) CIP \(Critical Infrastructure Plan\) is a set of requirements designed to secure the assets required for operating North America's bulk electric system.

#### Nonrepudiation

The assurance that a specific author actually did create and send a specific item to a specific recipient and that it was successfully received. The sender of the message cannot later credibly deny having sent the message, nor can the recipient credibly claim not to have received it.

### O

#### Outage Duration

Outage duration is the length of time of a documented outage and is expressed as an amount of time \(minutes, hours, days\).

## P-R

### P

#### Portfolio Management

A portfolio consists of all endeavors undertaken by an organization. We are looking to show value for each individual endeavor but also the IT program as a whole. For example, are we receiving the value from cloud services that we're looking for?

### Q

#### Quantum Computing

A theoretical technology which allows superposition of physical states to increase both computing capacity and encryption keyspace.

### R

#### Record

A data structure or collection of information that is retained by an organization for legal, regulator, or business reasons.

#### Return on Investment

A term used to describe a profitability ratio.

Generally calculated by dividing net profit by net assets.

## S-U

### S

#### Sandboxing

- Testing untested or untrusted code
- To better understand if an application is working the way it was intended to work

#### Separation of Duties

Dictates that one person/entity cannot complete an entire transaction alone.

In the case of encryption, a single entity should not be able to administer the issuing of keys, encrypt the data, and store the keys, because this could lead to a situation where that entity has the ability to access or take encrypted data.

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

### T

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

![Trust Zones](/img/trust-zones.png)

## V-Z

### W

#### Wassenaar Arrangement

 The **Wassenaar** Arrangement, formally established in July 1996, is a voluntary export control regime whose 42 members exchange information on transfers of conventional weapons and dual-use goods and technologies. This includes import restrictions and data sharing.

#### Write Once, Read Many \(WORM\)

A type of long-term storage, meaning it is written to initially and only used for read purposes thereafter.
