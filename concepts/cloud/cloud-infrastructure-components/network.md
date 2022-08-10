# Network

## Reference

![Network Models](/static/network-models.png)

## Traditional Networking

The traditional networking model is a *layered* approach with physical switches at the top layer and logical separation at the hypervisor level.

!!!
This model allows for the use of traditional network security tools. There may be some limitations on the visibility of network segments between VMs.
!!!

## Converged Networking

The converged model is optimized for cloud deployments and utilizes *standard* perimeter protection measures. The underlying storage and IP networks are converged (across the same infrastructure, as opposed to having a separate LAN and SAN) to maximize the benefits for a cloud workload.

You can think of a converged network model as being a super network, one that is capable of carrying a combination of data, voice, and video traffic across a single network that is optimized for performance.

!!!
This method facilitates the use of virtualized security appliances for network protection.
!!!

## Software-Defined Networking

SDN is the idea of *separating* the network control plane from the actual network forwarding plane. This allows for greater control over networking capabilities and for the integration of such things as APIs.

### Characteristics

==- Programmatically configured.
Allows network managers to configure, manage, secure, and optimize network resources very quickly via dynamic, automated SDN programs, which they can write themselves because the programs do not depend on proprietary software.
==- Open standards-based and vendor-neutral.
When implemented through open standards, SDN simplifies network design and operation because instructions are provided by SDN controllers instead of multiple, vendor-specific devices and protocols.
==- Directly programmable.
Network control is directly programmable because it is decoupled from forwarding functions.
==- Agile.
Abstracting control from forwarding lets administrators dynamically adjust network-wide traffic flow to meet changing needs.
==- Centrally managed.
Network intelligence is (logically) centralized in software based SDN controllers that maintain a global view of the network, which appears to applications and policy engines as a single, logical switch.
==-

### Elements

==- Controller.
Enables centralized management and control, automation, and policy enforcement across physical and virtual network environments.
==- Southbound Interface (SBI).
Relays information between the controller (control layer) and the *individual network devices* (such as *physical* switches, access points, routers, and firewalls).
==- Northbound Interface (NBI).
Relays information between the controller (control layer) and the *applications* and policy engines, to which an SDN looks like a single logical network device.
==-

!!!
The SBI and NBI are considered the SDN architecture APIs, as they define the communication between the applications, controllers, and networking systems.
!!!

### Benefits

The following are primary benefits are observed by using SDN:

- Hardware agnostic
- Management plane is separated from the data plane

### Layers

In the SDN architecture, the splitting of the control and data forwarding functions is referred to as “disaggregation,” because these pieces can be sourced separately, rather than deployed as one integrated system. This architecture gives the applications more information about the state of the entire network from the controller, as opposed to traditional networks where the network is only application-aware.

![SDN Architecture](/static/sdn-architecture.png)

#### Application Layer

The application layer provides:

- Business applications

!!!
APIs act as a bridge between the application and control layers using the NBI.
!!!

#### Control Layer

The control layer, also referred to as the *control plane*, refers to the processes that control the work done by the network device but do not directly impact the forwarding of individual frames or packets.

This layer provides:

- Network services
- SDN control software

#### Infrastructure Layer

The infrastructure layer, also referred to as the *infrastructure plane*, refers to the actions that devices take to forward data.

This layer provides:

- Physical network devices (which may be geographically disparate)
