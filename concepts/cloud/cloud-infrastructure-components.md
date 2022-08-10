# Cloud Infrastructure Components

## Compute

==- Affinity
Grouping of resources.
==- Anti-affinity
Separation of resources.
==- Compute Parameters
A cloud server’s compute parameters depend on the number of *CPUs* and the amount of RAM used. The ability to allocate these resources is a vital compute concern.
==- Limits
A limit creates a *maximum* ceiling for a resource allocation.
==- Reservations
A reservation creates a guaranteed *minimum* resource allocation that the host must meet.
==- Shares
The concept of shares is used to arbitrate the issues associated with compute resource *contention* situations. Share values are used to prioritize compute resource access for all guests assigned a certain number of shares. Shares allow the cluster's *reservations* to be allocated and then addresses any remaining resources that may be available for use by members of the cluster through a prioritized percentage-based allocation mechanism.
==-

## Network

### Software-Defined Networking

Software-defined networking (SDN) is the idea of *separating* the network control plane from the actual network forwarding plane. This allows for greater control over networking capabilities and for the integration of such things as APIs.

#### Characteristics

=== Programmatically configured.
Allows network managers to configure, manage, secure, and optimize network resources very quickly via dynamic, automated SDN programs, === which they can write themselves because the programs do not depend on proprietary software.
=== Open standards-based and vendor-neutral.
When implemented through open standards, SDN simplifies network design and operation because instructions are provided by SDN controllers instead of multiple, vendor-specific devices and protocols.
=== Directly programmable.
Network control is directly programmable because it is decoupled from forwarding functions.
=== Agile.
Abstracting control from forwarding lets administrators dynamically adjust network-wide traffic flow to meet changing needs.
=== Centrally managed.
Network intelligence is (logically) centralized in software based SDN controllers that maintain a global view of the network, which appears to applications and policy engines as a single, logical switch.
===

#### Elements

=== Controller.
Enables centralized management and control, automation, and policy enforcement across physical and virtual network environments.
=== Southbound Interface (SBI).
Relays information between the controller (control layer) and the individual network devices (such as physical switches, access points, routers, and firewalls).
=== Northbound Interface (NBI).
Relays information between the controller (control layer) and the applications and policy engines, to which an SDN looks like a single logical network device
===

!!!
The SBI and NBI are considered the SDN architecture APIs, as they define the communication between the applications, controllers, and networking systems.
!!!

#### Benefits

The following are primary benefits are observed by using SDN:

- Hardware agnostic
- Management plane is separated from the data plane

#### L

### Traditional Networking

### Converged Networking

## Storage

### Storage Architectures

### Storage Networks

### Storage Operations

### Storage Types

## Virtualization

### Hypervisors

### Components

### Features

### Threats

### Operations

## Management

