# Data Classification

## Overview

Data is classified based on its *value or sensitivity level*. This is performed in the *create phase* of the data lifecycle.

Data classification can be defined as a tool for categorization of data to help an organization effectively answer the following questions:

- What data types are available?
- Where is certain data located?
- What access levels are implemented?
- What protection level is implemented, and does it adhere to compliance regulations?

Virtualization has the potential to affect data classification processes and implementations in the cloud. Data transforming from raw objects to virtualized instances to snapshotted images back into virtualized instances and then back out to the users in the form of raw data may affect the organization's current classification methodology. Techniques and tools that were suitable for the traditional IT environment might not withstand the standard cloud environment.

!!!
The purpose of classification is to dictate *how to protect data*. You protect top-secret data differently than you protect secret data.
!!!

| Datasets | Input Entities |
| - | - |
| Primary set | P&DP law <br /> Scope and purpose of the processing <br /> Categories of the personal data to be processed <br /> Categories of the processing to be performed |
| Secondary set | Data location allowed <br /> Categories of users allowed <br /> Data retention constraints <br /> Security measures to be ensured <br /> Data breach constraints <br /> Status |

## Classification Process

The data classification section describes how and when data should be classified, and gives security procedures and controls for handling the data classifications.

Ask yourself, "how much damage could it cause if this data got inadvertently exposed?" (This is harm.) Data's value includes harm, time to create data, liability/compromise, etc. Similarly, what would the impact be in the following scenarios:

- If the information was widely distributed (such as SSNs or government information).
- If an employee of the CSP accessed the data.
- If the data was manipulated by an outsider or was unexpectedly changed.
- If the information was unavailable for a period of time.

The following items help determine classification:

- Sensitivity
- Jurisdiction
- Criticality

The following process should be followed:

- Execute data discovery
- Define data classification policies
- Execute data classification process
- Implement enforcement technologies to protect classified data

!!!
Data is classified by a certain trait. For example "to encrypt" or "not to encrypt" when using encryption; or "internal use" and "limited sharing" when using DLP. It can be manual (a task assigned to the user creating the data) or automatic based on policy rules (according to location, creator, content, and so on).
!!!

!!!
The relationship between data classification and data labeling is important. Data labeling is usually referred to as tagging the data with additional information (department, location, and creator). One of the labeling options can be classification according to certain criteria: top secret, secret, classified. *Classification is usually considered part of data labeling*.
!!!

### Data Labeling

Labeling is a technology which can be used to group data elements together.

When the data owner creates, categorizes, and classifies the data, it also needs to be labeled. It is the data owner's job to label data, not the CSP.

Labels might include the following types of information:

- Data owner
- Date of creation
- Date of scheduled destruction/disposal
- Confidentiality level
- Handling directions
- Dissemination/distribution instructions
- Access limitations
- Source
- Jurisdiction
- Applicable regulation

!!!
Data *classification* and labeling are most likely to affect the *Create, Store, Use, and Share* phases. Data *disposal* is most likely to affect the *Destroy* phase.
!!!

## Data Protection and Control

- Data retention
- Data deletion
- Data archiving

### Data Retention

The retention periods section details how long the different data classifications should be retained.

The data retention policy should include the following:

- *Retention periods*.
- *Applicable regulations*.
- *Retention/data formats*. The retention formats section details the medium on which the different data classifications should be stored. It also contains any handling procedures that should be followed.
- *Data security*.
- *Data classification*.
- *Archiving and retrieval procedures*.
- *Monitoring, maintenance, and enforcement*.

!!!
The data *retention* policy addresses the activities that take place in the *Archive* phase of the data lifecycle.
!!!

### Data Disposal

Disposal options in the legacy environment:

- Physical destruction of media and hardware
- Degaussing
- Overwriting
- Cryptoshredding

!!!
The data disposal policy addresses activities that take place in the Destroy phase of the data lifecycle.
!!!

### Data Archival

The archiving and retrieval procedures section of the data retention policy will contain information on how data should be sent into storage to support later recovery if needed.

- Data encryption procedures
- Data monitoring procedures
- Ability to perform e-discovery and granular retrieval
- Backup and DR options
- Data format and media type
- Data restoration procedures
