# Logging

## Quick Reference

| Acronym | Backronym |
| - | - |
| SIEM | Security Information and Event Management |

==- Aggregation
The ability of a SIEM to collect logs from several data sources.
==- Correlation
The ability of a SIEM to analyze and search logs.
==-

## Overview

Four key subsystems should be monitored in cloud environments:

- *Network*. Dropped packets.
- *Disk*. Slow reads/writes.
- *Memory*. Excessive usage.
- *CPU*. High utilization.

To maintain reasonable investigation capabilities, auditability, and traceability of data, it is recommended that you specify data access requirements in the cloud SLA or contract with the CSP.

Logging should suffice for the purpose of reconstructing the pertinent information (who, what, where, when, etc.) necessary to form a narrative of what transpired. This will be different for every organization and environment, and thus is not usually driven by standards or frameworks.

## Logging Methods

### SIEM

A SIEM *aggregates* data from many sources and is able to make *correlations* based on that data.

#### Characteristics

- Data aggregation (centralized collection of log data)
- Data correlation (enhanced analysis capabilities)
- Alerting (automated response)
- Dashboards (for management)
- Compliance (regulatory compliance requirements such as HIPAA or SOX)
- Retention (log management and retention)
- Forensic analysis (continuous monitoring and incident response)

#### Benefits

- Regulatory compliance requirements (HIPAA or SOX)
- Gaining or maintaining certifications (ISO 27001)
- Log management and retention
- Continuous monitoring and incident response
- Policy enforcement validation and policy violation detection
- Can detect repeated performance issues

## Logging by Service Model

### SaaS

- Webserver logs
- Application server logs
- Database logs
- Guest OS logs
- Host access logs
- Virtualization platform logs and SaaS portal logs
- Network captures
- Billing records

### PaaS

Application data that can be extracted and monitored is typically defined by the developers when building their PaaS application. At a minimum, however, OWASP recommends the following logs be available:

- Session management failures
- Application errors
- System events
- Application and related systems startups and shutdowns
- Logging initialization (starting, stopping, or pausing)
- Use of higher-risk functionalities, such as network connections and the addition or deletion of users
- Legal and other opt-ins, such as permissions for mobile phone capabilities and terms of use

### IaaS

- Cloud or network provider perimeter network logs
- Logs from DNS servers
- Virtual machine manager logs
- Host OS and hypervisor logs
- API access logs
- Management portal logs
- Packet captures
- Billing records
