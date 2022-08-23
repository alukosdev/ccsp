---
icon: stop
---

!!!danger
This page has not yet been revised for 2022.
!!!

# Cloud Service Models

Cloud service models affect the *level of control* an organization has over their resources.

![Cloud Service Models](/static/cloud-service-models.webp)

There are three major cloud service models:

- IaaS
- PaaS
- SaaS

!!!
In all three models, the customer is giving up an essential form of control: physical access to the devices on which the data resides.
!!!

## IaaS

IaaS offers only hardware and administration, leaving the customer responsible for the OS and other software.

IaaS consists of a facility, hardware, an abstraction layer, an orchestration (core connectivity and delivery) layer to tie together the abstracted resources, and APIs to remotely manage the resources and deliver them to consumers

IaaS allows the customer to install all software, including operating systems (OSs) on hardware housed and connected by the cloud vendor. In this model, the cloud provider has a datacenter with racks and machines and cables and utilities, and administers all these things. However, all logical resources such as software are the responsibility of the customer.

!!!
Some examples of IaaS would include datacenters that allow clients to load whatever operating system and applications they choose. The cloud provider simply supplies the compute, storage, and networking functions.
!!!

### Boundaries

#### Provider

The provider is responsible for the buildings and land that compose the datacenter; must provide connectivity and power; and creates and administers the hardware assets the customer's programs and data will ride on.

#### Customer

The customer, however, is in charge of everything from the operating system and up; all software will be installed and administered by the customer, and the customer will supply and manage all the data.

### Characteristics

- Scale
- Converged network and IT capacity pool
- Self-service and on-demand capacity
- High reliability and resilience

### Risks

- Personnel Threats
- External Threats (malware, hacking, DoS/DDoS, MITM, etc.)
- Lack of Specific Skillsets

### Benefits

- Usage metered
- Dynamic scalability
- Reduced cost of ownership
- Reduced energy and cooling costs

## PaaS

PaaS allows a way for customers to rent hardware, operating systems, storage, and network capacity over the Internet from a cloud service provider.

PaaS contains everything included in IaaS, with the addition of OSs. The cloud vendor usually offers a selection of OSs, so that the customer can use any or all of the available choices. The vendor will be responsible for patching, administering, and updating the OS as necessary, and the customer can install any software they deem useful.

!!!
Some examples of PaaS include hosting providers that offer not only infrastructure but systems already loaded with a hardened operating system such as Windows Server or a Linux distribution.
!!!

### Boundaries

#### Provider

The provider is responsible for installing, maintaining, and administering the OS(s).

#### Customer

The responsibilities for updating and maintaining the software will remain the customer's.

### Characteristics

- Support multiple languages and frameworks
- Multiple hosting environments
- Flexibility
- Allow choice and reduce lock-in
- Ability to auto-scale

### Risks

- Interoperability Issues (OS and OS updates may not function with customer applications)
- Persistent Backdoors
- Virtualization
- Resource Sharing

!!!
Risks impacting IaaS also affect PaaS:

- Personnel Threats
- External Threats (malware, hacking, DoS/DDoS, MITM, etc.)
- Lack of Specific Skillsets
!!!

### Benefits

- Operating systems can be upgraded frequently
- Distributed teams can work together
- Services are not bound by national border
- Optimization of expenditures by leveraging a single vendor

!!!
PaaS and SaaS often include data replication in their services.
!!!

## SaaS

SaaS is a software delivery method that provides access to software and its functionality remotely as a web-based service. Allows organizations to access business functionality at a cost typically less than paying for licensed applications because SaaS pricing is based on a monthly fee.

SaaS includes everything listed in IaaS and PaaS, with the addition of software programs. The cloud vendor becomes responsible for administering, patching, and updating this software as well. The cloud customer is basically only involved in uploading and processing data on a full production environment hosted by the provider.

Within SaaS, two delivery models are currently used:

- *Hosted Application Management*. The provider hosts commercially available software for customers and delivers it over the web.
- *Software on Demand*. The CSP gives customers network-based access to a single copy of an application created specifically for SaaS distribution.

!!!
Some examples of SaaS would include things like customer relationship manager (CRM) software or accounting software hosted in the cloud. The provider takes care of all the infrastructure, compute, and storage needs as well as providing the underlying operating systems and the application itself. All of this is completely transparent to the end user who only sees the application they have purchased.
!!!

### Boundaries

#### Customer

The customer only supplies and processes data to and in the system.

### Characteristics

- Overall reduction of costs
- Application and software licensing
- Reduced support costs

### Risks

- Proprietary Formats
- Virtualization
- Web Application Security

!!!
Risks impacting IaaS also affect SaaS:

- Personnel Threats
- External Threats (malware, hacking, DoS/DDoS, MITM, etc.)
- Lack of Specific Skillsets

Additionally, the risks impacting PaaS also affect SaaS:

- Interoperability Issues
- Persistent Backdoors
- Virtualization
- Resource Sharing
!!!

### Benefits

- Limited administration
- Always running latest version of software
- Standardized software distribution
- Global accessibility

!!!
PaaS and SaaS often include data replication in their services.
!!!
