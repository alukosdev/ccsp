!!!danger
This page is currently queued for revision.
!!!

# Virtualization*

Virtualization can help with the following business problems:

- *Auditing*. The ability to create baselines for virtual machines aids in verifying the appropriate security controls are in place.

Data transforming from raw objects to virtualized instances to snapshotted images back into virtualized instances and then back out to users in the form of raw data may affect the organization's current classification methodology; classification techniques and tools that were suitable for the traditional IT environment might not withstand the standard cloud environment. This should be a factor of how the organization considers and perceives the risk of cloud migration.

## Hypervisors

A hypervisor can be software-based, hardware-based, or firmware-based.

### Type 1

Type 1 hypervisors reside directly on the host machine, often as bootable software.

!!!
Type 1 hypervisors are often called bare-metal or hardware hypervisors.
!!!

### Type 2

Type 2 hypervisors are software hypervisors that run on top of the operating system already running on a host device.

### Secure Configuration

If you are using VMware's distributed power management (DPM) technology, ensure you disable any power management settings in the host BIOS to avoid conflicting with the proper operation of DPM.

#### Recommendations

- *Secure build*. Every OS vendor has developed a list of best practices to securely deploy their OS.
- *Secure initial configuration*. Standard baselines are available to determine what a secure initial configuration will look like for an organization. The standard baselines should be scoped and tailored to the specific risk appetite of the organization to develop a secure initial configuration.

#### Best Practices

- *Host hardening*. Removing unnecessary services, changing default passwords, and renaming default accounts.
- *Host patching*. Contact the vendor to determine all patches that are available, review the patches to ensure all are appropriate, deploy the patches. Patches -typically include firmware updates (least deployed), driver updates, and OS updates.
- *Host lockdown*.
- *Secure ongoing configuration maintenance*.

#### Best practices to secure the tools used to manage virtual hosts

- *Defense in depth*. Security tools should always be deployed in layers so that access can be controlled even if one layer is compromised.
- *Access control*. Control who has access to the tools.
- *Auditing and monitoring*. Log who is using the tools and what actions are being taken.
- *Maintenance*. Update and patch the tools as vulnerabilities are found or as vendors release critical patches.

## Components

### VLANs

Benefits provided by VLANs:

- Performance
  - VLANs can break up broadcast domains limiting superfluous traffic from being propagated across the network.
- Establishment of virtual workgroups
  - Workstations can be moved from one VLAN with simple changes. People working together on a particular project can easily be put into a single VLAN.
- Flexibility
  - As users move around within a campus, the switchport can be updated with their VLAN allowing them to maintain the same IP address.
- Ease of partitioning resources
  - VLANs can be setup in software versus different physical networks.

### Virtual Switches

#### Secure Configuration

- Physical NIC redundancy to redundant physical switches
- Port channeling
- Network isolation (management plane vs. virtual switches vs. VM traffic)
- Internal and external network isolation
- Use security applications that are virtual network aware (IPS, etc.)
- vMotion is sent in clear

### Application Virtualization

Allows the ability to test applications while protecting the OS and other application on a particular system. Common implementations include:

- Linux WINE
- Microsoft App-V
- XenApp

## Features

### Distributed Resource Scheduling (DRS)

A method for providing HA, workload distribution, and balancing of jobs in a cluster.

### Live Migration

Live migration is the term used to describe the movement of functional virtual instances from one physical host to another and how VMs are moved prior to maintenance on a physical device.

- VMs are moved as "live instances" when they are transitioned from one active host to another.
- VMs are migrated in an *unencrypted* form.

VMs are moved as image snapshots when they are transitioned from production to storage. This is not live migration.

### Virtual Machine Introspection (VMI)

Allows for *agentless* retrieval of the guest OS stage, such as the list of running processes, active network connections, and opening files.

An agentless means of ensuring a VM's security baseline does not change over time. It examines such things as physical location, network settings, and installed OS to ensure that the baseline has not been inadvertently or maliciously altered.

Used for malware analysis, memory forensics, and process monitoring and for externally monitoring the runtime state of a virtual machine. The introspection can be initiated in a separate virtual machine, within the hypervisor, or within another part of the virtualization architecture. The runtime state can include processor registers, memory, disk, network, and other hardware-level events.

VMI is typically used:

- With external monitoring using an IPS
- To conduct malware analysis
- To perform memory forensics

## Threats

- Attacks on the Hypervisor
- Guest Escape
- Information Bleed
- Data Seizure

- *Hyperjacking*. The installation of a rogue hypervisor that can take complete control of a host through the use of a VM-based rootkit that attacks the original hypervisor, inserting a modified rogue hypervisor in its place.
- *Guest Escape*.
- *Information Bleed*.
- *Data Seizure*.
- *Instant-On Gaps*. Vulnerabilities that exist when, after VM has been powered off from an extended period of time and may be missing security patches, it is powered back on. Remedies for this would include ensuring these systems are isolated until fully patched.

## Operations

- *Personnel isolation*. Brewer-Nash might come in here.
- *Hypervisor hardening*.
- *Instance isolation*.
- *Host isolation*.
