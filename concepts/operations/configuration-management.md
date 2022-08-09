# Configuration Management

## Quick Reference

| Acronym | Backronym |
| - | - |
| CI | Configuration Item |

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
===

## Summary

Configuration management *deals with the documentation of processes*.

Configuration management aims to maintain information about CIs required to deliver an IT service, including their relationships. Configuration management occurs when the configuration of an item, such as a network device, must be changed.

The process should include policies and procedures for each of the following:

- The development and implementation of new configurations that should apply to the hardware and software configurations of the cloud environment
- Quality evaluation of configuration changes and compliance with established security baselines
- Changing systems, including testing and deployment procedures, that should include adequate oversight of all configuration changes
- The *prevention* of any unauthorized changes in system configurations

## Operational Relationships

=== Availability Management
- If an existing configuration were to have negative impacts on system availability, they would have to be identified, monitored, and remediated as per the existing SLAs for the services and systems affected.
=== Change Management
- Change management has to approve modifications to all production systems prior to them taking place. There should never be a change that is allowed to take place to a CI in a production system unless change management has approved the change first.
- Configuration management aims to **prevent** *unauthorized changes* whereas change management aims to **allow** *changes through a formal approval process*.
=== Release and Deployment Management
- Once the release is officially live in the production environment, the existing configurations for all systems and infrastructure affected by the release have to be updated to accurately reflect their new running configurations and status within the configuration management database (CMDB).
===
