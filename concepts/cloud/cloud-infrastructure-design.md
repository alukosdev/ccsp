# Cloud Infrastructure Design

## Terminology

==- Chicken Coop
A design methodology in which a datacenter arranges racks within long rectangles with a long side facing the wind to provide natural cooling.
==- Redundancy
Deploying duplicate devices that can take over active operation if the primary device fails.
==- Resiliency
The ability to restore normal operations after a disruptive event. Redundancy is the foundation of resiliency.
==-

## Summary

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

### Logical Design

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

### Physical Design
