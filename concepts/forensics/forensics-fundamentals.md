# Forensics Fundamentals

## Glossary

==- Cloud Computing Forensic Science
The application of scientific principles, technological practices, and derived and proven methods to reconstruct past cloud computing events through identification, collection, preservation, examination, interpretation, and reporting of digital evidence.
==- Digital Forensics
Digital forensics is generally considered the application of science to the identification, collection, examination, and analysis of data while preserving the integrity of the information and maintaining a strict chain of custody for the data.
==- Forensic Science
Forensic science is generally defined as the application of science to the law.
==- Network Forensics
Network forensics is defined as the capture, storage, and analysis of network events. The idea is to capture every packet of network traffic and make it available in a single searchable database so that the traffic can be examined and analyzed in detail.
==-

### Associated Standards

The goal of the following standards is to promote best practices for the acquisition and investigation of digital evidence.

| Standard | Description |
| - | - |
| ISO/IEC 27037	| Guide for collecting, identifying, and preserving electronic evidence |
| ISO/IEC 27041 | Guide for incident investigations |
| ISO/IEC 27042 | Guide for digital evidence analysis |
| ISO/IEC 27043 | Incident investigation principles and processes |
| ISO/IEC 27050 | Overview and principles for eDiscovery |

## Overview

Challenges with forensics:

- Control over data (trustworthiness)
- Multitenancy
- Data volatility
- Evidence acquisition

Access to data will be decided by the following:

- The service model
- The legal system in the country where data is legally stored

!!!
There are certain jurisdictions where forensic data/IT analysis requires licensure (Texas, Colorado, and Michigan, for example).
!!!

## Investigation Process

### Identify

Identify and preserve evidence and begin chain of custody documentation.

### Collect

Label, record, acquire evidence, and ensure that modification does not occur.

1. Develop a plan to acquire the data; important factors for prioritization include:
  i. Likely value
  ii. Volatility
  iii. Amount of effort required
2. Acquire the data
3. Verify the integrity of the data

Network forensics has various use cases for data acquisition and collection:

- Uncovering proof of an attack
- Troubleshooting performance issues
- Monitoring activity for compliance with policies
- Sourcing data leaks
- Creating audit trails for business transactions

#### Prioritization Order for Volatile Data

1. Network connections
2. Login sessions
3. Contents of memory
4. Running processes
5. Open files
6. Network configuration
7. Operating system time

#### Alternative Prioritization for Volatile Data

1. CPU cache, registers, RAM
2. Virtual memory
3. Disk drives
4. Backups and printouts

### Examine

After data has been collected, the next phase is to examine the data, which involves assessing and extracting the relevant pieces of information from the collected data.

Yields data. Just the facts. For example:

- File opened at 10:23 AM
- DNS stopped at 7:02 AM
- etc.

### Analyze

The analysis should include identifying people, places, items, and events and determining how these elements are related so that a conclusion can be reached.

Often, this effort includes correlating data among multiple sources. For instance, a NIDS log may link an event to a host, the host audit logs may link the event to a specific user account, and the host IDS log may indicate what actions that user performed.

How to identify who completed an event:

- Source address
- User identity (if authenticated or otherwise known)
- Geolocation
- Service name and protocol
- Window, form, or page (such as URL address)
- Application address
- Application identifier

Information. Taking data and putting it into context. For example:

- DNS stopped at 7:02 AM but nobody should have had access to DNS at 7:02 AM...

### Report

The final phase is reporting, which is the process of preparing and presenting the information resulting from the analysis phase. Many factors affect reporting, including the following:

- Alternative explanations
- Audience consideration
- Actionable information

!!!
The ultimate recipient of all forensic evidentiary collection and analysis-the entity getting the reports-will be the court, in order to make a final determination of its merits and insights.
!!!

### Lessons Learned

Document what was learned. Something is always learned.
