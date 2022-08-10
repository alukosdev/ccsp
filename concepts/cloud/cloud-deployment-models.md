# Cloud Deployment Models

Cloud deployment models affect the *extent of resource sharing* the organization will be subjected to.

There are four major cloud deployment models:

- Private Cloud
- Public Cloud
- Community Cloud
- Hybrid Cloud

## Private Cloud

> According to NIST SP 800-145, the private cloud infrastructure is provisioned for *exclusive use by a specific community of consumers* from organizations that have *shared concerns* (e.g., mission, security requirements, policy, and compliance considerations). It *may be owned, managed, and operated by one or more of the organizations in the community, a third party, or some combination of them,* and it *may exist on or off premises*.

A community cloud features infrastructure and processing owned and operated by an affinity group; disparate pieces might be owned or controlled by individuals or distinct organizations, but they come together in some fashion to perform joint tasks and functions.

Gaming communities might be considered community clouds. For instance, the PlayStation network involves many different entities coming together to engage in online gaming: Sony hosts the identity and access management (IAM) tasks for the network, a particular game company might host a set of servers that run digital rights management (DRM) functions and processing for a specific game, and individual users conduct some of their own processing and storage locally on their own PlayStations.

### Risks

- Resiliency Through Shared Ownership
  - Several points of entry
  - Configuration management unity
  - Baseline enforcement
  - Shared decision making
- Shared Costs
  - Shared access and control
- No Need for Centralized Administration for Performance and Monitoring
  - Removes reliability of centralized standards for performance and security monitoring

### Threats

- Malware
- Internal Threats
- External Attackers
- Man-in-the-Middle Attacks
- Social Engineering
- Theft/Loss of Devices
- Regulatory Violations
- Natural Disasters
- Loss of Policy Control
- Loss of Physical Control
- Lack of Audit Access

## Public Cloud

> According to NIST SP 800-145, the public cloud infrastructure is provisioned for *open use* by the general public. It may be owned, managed, and operated *by a business, academic, or government organization, or some combination of them*. It *exists on the premises of the cloud provider*.

The public cloud is what we typically think of when discussing cloud providers. The resources (hardware, software, facilities, and staff) are owned and operated by a vendor and sold, leased, or rented to anyone (offered to the public-hence the name).

Examples of public cloud vendors include Rackspace, Microsoft Azure, and Amazon Web Services (AWS).

### Risks

#### Multitenant Environments

- Conflict of Interest
- Escalation of Privilege
- Information Bleed
- Legal Activity

#### Vendor Lock-In

Vendor lock-in occurs when the organization creates a dependency on the provider.

- Limitations to moving (bandwidth from old provider or otherwise)
- Unfavorable contracts
- Using proprietary data formats
- Regulatory constraints (where other providers may not be able to meet needs)

!!!
While there are several ways to avoid vendor lock-in, the best way is through favorable contract language. To avoid lock-in, the organization has to think in terms of *portability*.
!!!

#### Vendor Lock-Out

When the cloud provider goes out of business, is acquired, or ceases operation for any reason.

To avoid lock-out, the organization should consider the provider's:

- Longevity
- Core Competency
- Jurisdictional Suitability
- Supply Chain Dependencies
- Legislative Environment

### Threats

- Loss of Policy Control
- Loss of Physical Control
- Lack of Audit Access
- Rogue Administrator
- Escalation of Privilege
- Contractual Failure

!!! Threats impacting the private model also affect the public model:

- Malware
- Internal Threats
- External Attackers
- Man-in-the-Middle Attacks
- Social Engineering
- Theft/Loss of Devices
- Regulatory Violations
- Natural Disasters
!!!

!!!
The terms "public" and "private" can be confusing, because we might think of them in the context of who is offering them instead of who is using them. Remember: A public cloud is owned by a specific company and is offered to anyone who contracts its provided services, whereas a private cloud is owned by a specific organization but is only available to users authorized by that organization.
!!!

## Community Cloud

> According to NIST SP 800-145, the community cloud infrastructure is provisioned for *exclusive use by a specific community of consumers from organizations that have shared concerns* (e.g., mission, security requirements, policy, and compliance considerations). It *may be owned, managed, and operated by one or more of the organizations in the community, a third party, or some combination of them*, and it *may exist on or off premises*.

A community cloud features infrastructure and processing owned and operated by an affinity group; disparate pieces might be owned or controlled by individuals or distinct organizations, but they come together in some fashion to perform joint tasks and functions.

Gaming communities might be considered community clouds. For instance, the PlayStation network involves many different entities coming together to engage in online gaming: Sony hosts the identity and access management (IAM) tasks for the network, a particular game company might host a set of servers that run digital rights management (DRM) functions and processing for a specific game, and individual users conduct some of their own processing and storage locally on their own PlayStations.

### Risks

- Resiliency Through Shared Ownership
  - Several points of entry
  - Configuration management unity
  - Baseline enforcement
  - Shared decision making
- Shared Costs
  - Shared access and control
- No Need for Centralized Administration for Performance and Monitoring
  - Removes reliability of centralized standards for performance and security monitoring

### Threats

- Malware
- Internal Threats
- External Attackers
- Man-in-the-Middle Attacks
- Social Engineering
- Theft/Loss of Devices
- Regulatory Violations
- Natural Disasters
- Loss of Policy Control
- Loss of Physical Control
- Lack of Audit Access

## Hybrid Cloud

> According to NIST SP 800-145, the hybrid cloud infrastructure is a composition of two or more distinct cloud infrastructures (private, community, or public) that remain unique entities, but are bound together by standardized or proprietary technology that enables data and application portability (e.g., cloud bursting for load balancing between clouds).

A hybrid cloud contains elements of the other models. For instance, an organization might want to retain some private cloud resources (say, their legacy production environment, which is accessed remotely by their users), but also lease some public cloud space as well (maybe a PaaS function for DevOps testing, away from the production environment so that there is much less risk of crashing systems in operation).

An example of a hybrid cloud environment might include a hosted internal cloud such as a SharePoint site with a portion carved out for external partners who need to access a shared service. To them it would appear as an external cloud; therefore, it would be operating as a hybrid.
