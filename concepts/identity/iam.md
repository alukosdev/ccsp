---
label: Identity and Access Management
---

# Identity and Access Management (IAM)

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
ABAC | Attribute-Based Access Control
IAM | Identity and Access Management
RBAC | Role-Based Access Control
SCIM | System for Cross-domain Identity Management
SPML | Service Provisioning Markup Language

## Glossary

=== Access Control
Access control is restricting access to resources.
=== Access Management
Access management is the process of managing access to resources.
=== Attributes
Attributes are facets of an identity. Attributes can be relatively static (like an organizational unit) or highly dynamic (IP address, device being used, if the user authenticated with MFA, location, etc.).
=== Authentication
Authentication is the process of confirming an identity. When you log in to a system you present a username (the identifier) and password (an attribute we refer to as an authentication factor).

!!!
Authentication is often referred to as AuthN.
!!!
=== Authoritative Source
An authoritative source is the root source of an identity, such as the directory server that manages employee identities.
=== Authorization
Authorization is the process of granting an identity access to something (.e.g. data or a function).

!!!
Authorization is often referred to as AuthZ.
!!!
=== Entitlement
An entitlement maps an identity (including roles, personas, and attributes) to an authorization. The entitlement is what they are allowed to do, and for documentation purposes we keep these in an entitlement matrix.
=== Entity
The person or "thing" that will have an identity. It could be an individual, a system, a device, or application code.
=== Federation
An association of organizations that come together to exchange information as appropriate about their users and resources to enable collaborations and transactions.
=== Identifier
The means by which an identity can be asserted. For digital identities this is often a cryptological token. In the real world it might be your passport.
=== Identity
The unique expression of an entity within a given namespace. An entity can have multiple digital identities, such as a single individual having a work identity (or even multiple identities, depending on the systems), a social media identity, and a personal identity. For example, if you are a single entry in a single directory server then that is your identity.
=== Persona
The expression of an identity with attributes that indicates context. For example, a developer who logs into work and then connects to a cloud environment as a developer on a particular project. The identity is still the individual, and the persona is the individual in the context of that project.
=== Policy Decision Point
?
=== Policy Enforcement Point
Access decisions can be enforced at various points with various technologies.
=== Policy Management
Establishes the security and access policies based on business needs and the degree of acceptable risk.
=== Role
Identities can have multiple roles which indicate context. "Role" is a confusing and abused term used in many different ways. For our purposes we will think of it as similar to a persona, or as a subset of a persona. For example, a given developer on a given project may have different roles, such as "super-admin" and "dev", which are then used to make access decisions.
==- System for Cross-domain Identity Management (SCIM)
SCIM is a standard for exchanging identity information between domains. It can be used for provisioning and deprovisioning accounts in external systems and for exchanging attribute information.

- Standardized
- Open standard for automating the exchange of user identity information between identity domains or IT systems
- Newer than SPML
=== Service Provisioning Markup Language (SPML)
A method for automating account creation.

- Standardized
- Seldom implemented due to inflexibility and lack of vendor support
- Older and uses XML, which is slow
===

## Overview

IAM is about the people, processes, and procedures used to create, manage, and destroy identities of all kinds. It is the security discipline that enables the right individuals to access the right resources at the right times for the right reasons.

Usually, *regulatory* compliance drives IAM efforts, not business requirements or needs.

!!!
IAM is always the responsibility of the *cloud customer*.
!!!

An IAM system includes the following components:

- Identity Management
- Access Management
- Identity Repository and Directory Services

An IAM system should carry out two functions:

1. Ensure the identity of an entity
2. Once authenticated, the entity should be given the correct level of access to the systems they are trying to access

IAM sets out to define what a subject (active entity) is allowed to do to an object (passive entity)?

!!!
*Accountability* is the end purpose of all IAM efforts. Identification, authentication, and authorization are the elements of IAM that support this effort.
!!!

Key phases include:

- Provisioning
- Centralized Directory
- Privileged User Management
- Authentication
- Access

## Components

### Identity Management

Identity management is the process whereby individuals are given access to system resources by associating user rights with a given identity. This includes registering, provisioning, and deprovisioning identities for all relevant entities and their attributes, while making that information available to the proper audit.

### Access Management

Access management is the process that deals with controlling access to resources once they have been granted. Access management tries to identify who a user is and what they are allowed to access.

This stage is where the real risk decisions are made. It is more important to control access rights than it is to control the number of identities.

### Identity Repositories and Directory Services

==- Identity Repository
An identity repository is the store of information or attributes of identities.
==- Directory Service
A directory services is how identities and attributes are managed. There are several directory services available today:

- X.500 and LDAP
- Microsoft Active Directory
- Novell eDirectory
- Metadata replication and synchronization
==-

## Provisioning and Deprovisioning

### Provisioning Process

Individual components of provisioning and deprovisioning process could be considered parts of identity and access management. In some cases, the process is referred to as "I triple A", starting at the identification phase and ending with accountability.

==- Proofing/registering.
Typically performed by HR.
==- Provisioning.
Traditionally performed by IT but strides are being made to automate this.
==- Identification.
The process of claiming an identity (asserting who you are). This should be unique for accountability (such as a user ID, account number, RFID, or IP/MAC).
==- Authentication.
The the process that establishes with adequate certainty the identity of an entity. Supports the identification claim by proving by some means (such as a username and password) that this is the user they say they are.; "Who are you?" and "How do I know I can trust you?"
==- Authorization.
The process of granting access to resources. Enforced at the policy enforcement point.; "What do you have access to?"
==- Accountability/auditing.
Based on identification information; the ability to match a subject's action to their identity.
==- Deprovisioning.
The process whereby a user account is disabled. This process should be standardized using SPLM or SCIM.
==-

### Provisioning Methods

Account provisioning or identity provisioning technology creates, modifies, disables, and deletes user accounts and their profiles across IT infrastructure and business applications.

==- Discretionary account provisioning
Administrators determine which applications and data a user should have access to.
==- Self-service account provisioning
Users participate in some aspects of the provisioning process, thus reducing administrative overhead. Often, users are allowed to request an account and manage their passwords.
==- Workflow-based account provisioning
Gathers the required approvals from the designated approves before granting a user access to an application or data. For example, the business rules in a finance application might require that every new account request be approved by the company's CFO.
==- Automated account provisioning
Requires every account to be added the same way through an interface in a centralized management application. This streamlines the process of adding and managing user credentials and provides administrators with the most accurate way to track who has access to specific applications and data sources.

Automated account provisioning is usually accomplished using one of the following two methods:

- SCIM
- SPML
==-

!!!
Cloud platforms tend to have greater support for the ABAC model for IAM, which offers greater flexibility and security than the RBAC model. RBAC is the traditional model for enforcing authorizations and relies on what is often a single attribute (a defined role). ABAC allows more granular and context aware decisions by incorporating multiple attributes, such as role, location, authentication method, and more. When available, ABAC is the preferred model for cloud-based access management.
!!!
