!!!danger
This page is currently queued for revision.
!!!

# Cloud Infrastructure Design*

## Glossary

=== Chicken Coop
A design methodology in which a datacenter arranges racks within long rectangles with a long side facing the wind to provide natural cooling.
=== Redundancy
Deploying duplicate devices that can take over active operation if the primary device fails.
=== Resiliency
The ability to restore normal operations after a disruptive event. Redundancy is the foundation of resiliency.
===

## Overview

Location is the major and primary concern when building a data center. It's important to understand the jurisdiction where the datacenter will be located. This means understanding the local laws and regulations under that jurisdiction. In addition, the physical location of the datacenter will also drive requirements for protecting data during threats such as natural disasters.

The industry standard for uptime in cloud service provision is "five nines," which means 99.999% uptime. This equates to less than six minutes per year.

!!!
A customer's ability to connect to a datacenter may be limited by a failure within the own customer's ISP. This would be a lack of availability from the customer's perspective but not a lack of uptime on the part of the provider.
!!!

## Design Principles

- *Hardening*.
- *Encryption*.
- *Layered Defense*. Also referred to as "defense-in-depth", this is the practice of having multiple overlapping means of securing the environment with a variety of methods. These should include a blend of administrative, logical, technical, and physical controls.

### Isolation

- Restricted physical access to devices
- Secure KVMs
- Restricted logical access to devices

=== Secure KVMs
Secure kernel-based VMs allow you to turn Linux into a hypervisor that allows a host machine to run multiple, isolated environments called guests or VMs. Secure KVMs differ from their counterparts in that they are designed to deter and detect tampering using the following means:

- Isolated data channels
- Tamper-warning labels
- Housing intrusion detection
- Fixed firmware
- Tamper-proof circuit board
- Safe buffer design
- Selective USB access
- Push-button controls

!!!
It's important to note that KVM could mean secure Linux-based kernel virtual machine or Keyboard, Video, Mouse. Ensure you understand the difference between each of these.
!!!
===

## Logical Design

The following is true about the logical design for a network:

- It lacks specific details such as technologies and standards while focusing on the needs at a general level.
- It communicates with abstract concepts, such as a network, router, or workstation, without specifying concrete details.

Abstractions for complex systems, such as network designs, are important because they simplify the problem space so humans can manage it (such as a WAN diagram).

Logical designs are often described using terms from the customer's *business* vocabulary.

!!!
An important aspect of a logical network design is that it is part of the requirements set for a solution to a customer problem.
!!!

Virtualization will leverage a hypervisor to assist with logical separation. A number of items should be considered in the logical design. These include:

- *Communications access*. What is allowed and what is not allowed?
- *Secure communications across the management plane*.
- *Secure storage*.
- *Disaster recovery*.

## Physical Design

==- Cable Mining
The process of reviewing, identifying, and removing cables that are no longer being used.
==- Mean Time Before Failure (MTBF)
A measure of component reliability. It provides the average time between system or component failures.
==- Mean Time to Repair (MTTR)
Represents the average time required to repair a device that has failed or requires repair.
==- Mean Time to Switchover (MTTS)
The average time to switch over from a service failure to a replicated failover instance (backup).
==- Plenum
In building construction, a plenum is a separate space provided for air circulation for heating, ventilation, and air-conditioning (sometimes referred to as HVAC) and typically provided in the space between the structural ceiling and a drop-down ceiling.

!!!
Cold air is usually circulated through plenums.
!!!
==-

The basic idea of physical design is that it communicates decisions about the hardware used to deliver a system. The following is true about a physical network design:

- It is created from a logical design.
- It often expands elements found in a logical design.

For instance, in terms of networking, a WAN connection on a logical design diagram can be shown as a line between two buildings. When transformed into a physical design, that single line can expand into the connection, routers, and other equipment at each end of the connection. The actual connection media might be shown on a physical design, along with manufacturers and other qualities of the network implementation.

Four items that would be considered in datacenter design:

- MTBF
- MTTR
- Automating service enablement
- Consolidating monitoring capabilities

### Facilities and Redundancy

The following factors should be taken into consideration when designing a datacenter:

- Regulatory issues
- Geographic location
- Redundancy issues

#### Geography

##### Rural Design

- Availability of emergency services is a concern.

##### Urban Design

- Municipal codes can restrict building design.

#### Redundancy

##### Power Redundancy

- Power Provider Redundancy
- Power Line Redundancy
- Power Conditioning and Distribution Redundancy

##### Communications Redundancy

##### Personnel Redundancy

- Cross-Training
- Water
- Egress
- Lighting

##### Security Redundancy

- Perimeter defenses should use layered approach
- Vehicular approach/access, to include driveways that wind and curve and/or include speed bumps as well as bollards
- Guest/visitor access through a controlled entry point
- Proper placement of hazardous or vital resources
- Interior physical access controls
- Specific physical protections for highly sensitive assets
- Fire detection and suppression systems
- Sufficient power for all these functions

##### Holistic Redundancy

- Uptime Institute (link me)

##### External Redundancy

- Power feeds/lines
- Power substations
- Generators
- Generator fuel tanks
- Network circuits
- Building access points
- Cooling infrastructure

##### Internal Redundancy

- Power distribution units (PDUs)
- Power feeds to rack
- Cooling units
- Networking
- Storage units
- Physical access points

### Efficiency

A minimum effective (clear) height of 24 inches should be provided for raised floor installations. Additional clearance can help achieve a more uniform pressure distribution in some cases, but is not necessary.

The power requirements for cooling a datacenter depend on the amount of heat being removed (not generated) and the temperature delta between the data center and the outside air.

- Temperature: 64.4 to 80.6 F (18 to 27 C)
- Humidity: 40%-60%
- Dew point: 41.9 to 59 F (5.5 to 15 C)

### Safety

#### Fire Suppression

=== FM-200
FM-200 is used as a replacement for older Halon systems specifically because it (unlike Halon) does not deplete the ozone layer. It is discharged into the room within 10 seconds and suppresses fire immediately.

- Odorless
- Colorless
- Liquefied compressed gas (at room temperature)
- It is stored as a liquid and dispensed in to the hazard as a colorless, electrically non-conductive vapor that is clear and does not obscure vision.
- Classified as a "clean agent" which means that it is safe to use within occupied spaces. It is nontoxic at levels used for fire suppression.
- Does not leave a residue after discharge.
- Does not deplete the ozone and has a minimal impact on the environment relative to the impact a catastrophic fire may have.
=== Halon
It is considered a good practice to avoid all unnecessary exposure to Halon.

- Effective gaseous fire suppression agent.
- It depletes the ozone and is harmful to the environment.
===

#### Fire/Smoke Detection

Codes require detectors under the floor or above the ceiling where HVAC piping, electrical feeders, or IT cables are placed within these plenum spaces.

##### Spot-type Detectors

- *Ionization-based*. Uses a small amount of radioactive material.
- *Photoelectric*. Uses a light source and a photosensitive sensor.

##### Aspirating/Air Sampling Smoke Detectors (ASSD)
