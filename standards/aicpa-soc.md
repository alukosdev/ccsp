---
categories: [Auditing and Assurance Standards]
---

!!!danger
This page is currently queued for revision.
!!!

# AICPA SOC*

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
AICPA |	American Institute of Certified Public Accountants
IAASB | International Auditing and Assurance Standards Board
SAS	| Statement on Auditing Standards
SOC	| System and Organization Controls
SSAE | Statement on Standards for Attestation Engagements

## Overview

SOC is part of the SSAE reporting format created by the AICPA. SSAE 18 is the current audit standard. These are uniformly recognized as being acceptable for regulatory purposes in many industries, although they were specifically designed as mechanisms for ensuring compliances with the Sarbanes-Oxley Act, which governs publicly traded corporations.

The SAS 70 was replaced by SOC Type 1 and Type 2 reports in 2011 following changes and a more comprehensive approach to auditing being demanded by customers and clients. For years, SAS 70 was seen as the de facto standard for datacenter customers to obtain independent assurance that their datacenter service provider had effective internal controls in place for managing the design, implementation, and execution of customer information.

## Components

### SOC 1

SOC 1 reports are strictly for auditing the financial reporting instruments of a corporation. Similar to SOC 2, there are two subclasses of SOC 1 reports: Type 1 and Type 2. These are not relevant for the exam as they relate to financial reporting.

The international equivalent to the AICPA SOC 1 is the IAASB issued and approved ISAE 3402.

### SOC 2

SOC 2 reporting was specifically designed for IT-managed service providers and cloud computing. The report specifically addresses any number of the so-called Trust Services principles (TSP???), which follow:

> https://socreports.com/white-papers/soc-2/soc-2-privacy-principle-introduction-and-overview new as of 2022/08/23

- Security
- Availability
- Processing Integrity
- Confidentiality
- Privacy

The SOC 2 is an examination of the design and operating effectiveness of controls that meet the criteria for principles set forth in the AICPA's Trust Services principles.

Typically, SOC 2 reports are only provided to customers and require an NDA be signed.

A cloud provider intending to prove its trustworthiness would look to an SOC 2 report as the artifact that demonstrated it.

#### SOC 2 Type 1

SOC 2 Type 1 reports only reviews the design of controls, not how they are implemented and maintained, or their function.

A SOC 2 Type 1 report presents an auditor's opinion at a specific date. It is not extremely useful for determining the security and trust of an organization.

#### SOC 2 Type 2

SOC 2 Type 2 reports are a thorough review of the target's controls, including how they have been implemented and their efficacy. It gives the customer a realistic view of the provider's security posture and overall program.

A type 2 report presents an auditor's opinion over a declared period, generally between 6 months and 1 year.

Unlike the SOC 2 Type 1, the SOC 2 Type 2 is extremely useful for determining the security and trust of an organization. It provides a true assessment of an organization's security posture.

Cloud vendors will likely never share an SOC 2 Type 2 report with any customer or even release it outside the provider's organization. The SOC 2 Type 2 report is extremely detailed and provides exactly the kind of description and configuration that the cloud provider is trying to restrict from wide dissemination.

### SOC 3

The SOC 3 is the "seal of approval". It contains no actual data about the security controls of the audit target and is instead just an assertion that the audit was conducted and that the target organization passed.

SOC 3 reports are usually publicly available. Thus, if you are not a customer, you would likely receive a SOC 3 report.

This is currently the practice accepted in the industry.
