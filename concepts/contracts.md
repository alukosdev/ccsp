---
order: 1700
---

# Contracts

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
LOI | Letter of Intent
MOA | Memorandum of Agreement
MOU | Memorandum of Understanding
OLA | Operational-Level Agreement
PLA | Privacy-Level Agreement
SLA | Service-Level Agreement

## Glossary

=== Memorandum of Agreement (MOA)
*See [Memorandum of Understanding (MOU)](/concepts/contracts/#memorandum-of-understanding-mou)
=== Memorandum of Understanding (MOU)
A *nonbinding* agreement between two or more parties outlining the terms and details of an understanding, including each parties' requirements and responsibilities.
=== Letter of Intent (LOI)
A LOI outlines the general plans of an agreement between two or more parties before a legal agreement is finalized.
=== Service Levels
Service levels indicate the minimum expected performance.
===

## Overview

The contract will spell out all the terms of the agreement: what each party is responsible for, what form the services will take, how issues will be resolved, and so on. The contract will also state what the penalties are (usually financial) when the cloud provider fails to meet the SLA for a given period.

> The provider will ensure the customer has constant, uninterrupted access to the Customer's data storage resources. Customer's monthly fee will be waived for any period following a calendar month in which any service level has not been attained by the Provider.

The contract defines all the terms of an agreement with a cloud provider, including what each party is responsible for, what form the services will take, how issues will be resolved, and so on.

!!!
Contract management is all about third-party governance.
!!!

From a contractual, regulated, and PII perspective, the following should be reviewed and fully understood with regard to any hosting contracts (along with other overarching components within an SLA):

=== Scope of processing
Clear understanding of the permissible types of data processing should be provided. The specifications should also list the purpose for which the data can be processed or utilized.
=== Use of subcontractors
Understanding where any processing, transmission, storage, or use of information will occur.
=== Deletion of data
Where the business operations no longer require information to be retained for a specific purpose, the deletion of information should occur in line with the organizations data retention policies and standards.
=== Appropriate or required data security controls
Where processing, transmission, or storage of data and resources is outsourced, the same level of security controls should be required for any entry's contracting or subcontracting services.
Locations of data. Where information is being stored, processed, and transmitted in the event of daily actions or failover.
=== Return or restitution of data
For both contractors and subcontractors where a contract is terminated, the timely and orderly return of data has to be required both contractually and within the SLA.
=== Right to audit subcontractors
Right to audit clauses should allow for the organization owning the data (not possessing) to audit or engage the services of an independent party to ensure that contractual and regulatory requirements are being satisfied by either the contractor or the subcontractor.
===

At a minimum, you should ensure that your cloud service contract states that you must be notified in the event of a subpoena or other similar actions to ensure that you do not lose access to your data as a result of lawsuits.

Immediate notification from a CSP to a customer should be required for all security related events. This is especially true for security breaches. This should be explicitly addressed in the service contract between the client and the CSP and should be non-negotiable.

## Types of Contracts

### Operational-Level Agreements (OLAs)

#### Overview

OLAs are SLAs negotiated between internal business units within the enterprise. OLAs are a contract that defines how various IT groups within a company plan to deliver a server or set of services.

For example, an IT department may guarantee system uptime to a separate group within the same organization.

### Privacy-Level Agreements (PLAs)

#### Overview

PLAs are an agreement whereby the cloud provider states the level and types of personal data protection(s) in place. A PLA would require the cloud provider to document expectations for the cloud customer's data security, which could be an explicit admission of liability for CSPs, which is why this typically isn't common.

The CSA allows for four items in a PLA:

- A PLA requires the CSP to clearly describe the level of privacy and data protection that is undertaken to maintain with respect to the relevant data processing.
- The CSP must adopt a common structure or outline of the PLAs in which it can promote a powerful global industry standard.
- A PLA should offer a clear and effective way to communicate the level of data protection offered by a CSP.
- The eventual goal for a PLA is to provide customers with a tool to baseline personal data protection legal requirements across an environment and to evaluate the data protection offered by different CSPs.

#### Characteristics

- Provides a clear and effective way to communicate the level of personal data protection offered by a service provider
- Works as a tool to assess the level of a service provider's compliance with data protection legislative requirements and leading practices
- Provides a way to offer contractual protection against possible financial damages due to lack of compliance

### Service-Level Agreements (SLAs)

The SLA will set specific, quantified goals for these services and their provision over a certain timeframe.

One use of the SLA is to determine whether a customer is actually receiving the services outlined in the SLA. An independent third-party can objectively affirm whether the requirements outlined in the SLA are being met.

The SLA should contain elements of the contract that can be subject to discrete, objective, repeatable, numeric metrics. For example:

- There will be no interruption of connectivity to data storage longer than three (3) seconds per calendar month.

SLAs are negotiated with *customers*.

- Assessment of risk environment
- Risk profile
- Risk appetite
- Responsibilities
- Regulatory requirements
- Risk mitigation
- Risk frameworks

An SLA typically includes items that can be measured quantitatively:

*Availability*: What is the uptime?
*Performance*: What is the response time?
*Privacy of the data*: Does the data need to be encrypted?
*Logging and reporting*: What needs to be logged?
*DR expectations*: What is the RTO, RPO, and MTD?
*Location of the data*: What regulations may dictate where the data is stored?
*Data format and structure*: How will data be stored, saved, and retained?
*Portability of the data*: Will data be maintained such that it can be moved among CSPs?
*Identification and problem resolution*: Who is called when there are problems?
*Change-management process*: What is the process for changes to be submitted and verified?
*Dispute-mediation process*: Exit strategy with expectations on the provider to ensure a smooth transition.

Having an SLA separate from the contract allows the company to revise the SLA without revising the contract. The contract would then refer to the SLA. The term for the contract could be multiple 2-year periods while the SLA would be reviewed quarterly, for example. This reduces the need to engage legal for contract review.

!!!
I like to consider the SLA as the "performance contract" since it is more concerned with the performance-related aspects than the contract itself.
!!!
