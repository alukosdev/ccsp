---
label: Software Development Lifecycle
---

# Software Development Lifecycle (SDLC)

## Quick Reference

| Acronym | Backronym |
| - | - |
| IaC | Infrastructure as Code |
| SDLC | Software Development Lifecycle |

==- Application Accreditation
The application has been approved by management.
==- Application Certification
The application meets technical requirements.
==- Infrastructure as Code (IaC)
A type of IT setup wherein developers or operations teams automatically manage and provision the technology stack for an application through software, rather than using a manual process to configure discrete hardware devices and operating systems.
===

## Overview

The purpose of the SDLC to ensure that applications are properly secured prior to an organization using them. Several software development lifecycles have been published with most of them containing similar phases.

For the purposes of the exam I have consolidated a few popular models into a single model using the following phases:

1. Analysis (planning and requirements analysis)
2. Define
3. Design
4. Develop (implement)
5. Test (verify)
6. Deploy/Release/Maintain
  - Secure Operations (could also be considered part of deploy/release)
  - Secure Disposal

## Lifecycle

Verification and validation should occur at *every stage* of development and during the software development lifecycle, and in line with change management components.

### 1. Analysis

In this phase, business and security requirements and standards are being determined. Calls for all business requirements are to be defined even before initial design begins:

- Functional requirements are determined
- Nonfunctional requirements are determined
- Planning for QA requirements and identification of risks
- Feasibility study (especially if bound by regulations such as HIPAA)
- *Security* requirements
- The requirements are then analyzed for their validity and the possibility of incorporating them into the system to be developed.

The analysis phase of the SDLC is when requirements of the project are put into a project plan. This plan will outline the specifications for the features and functionality of the software or application to be created. ~~At the end of the analysis phase, there will be formal requirements and specifications ready for the development team to turn into actual software.~~

### 2. Define

Identify the business needs of the application. Refrain from choosing any specific tools or technology at this phase, as it's too early to make these decisions.

We're trying to determine the purpose of the software, in terms of meeting the user's needs; therefore, we may solicit input from the user community in order to determine what they want. Develop user stories. The following questions should be answered:

- What will the *user* want to accomplish and how will you approach it?
- What will the user interface look like?
- Will it require the use or development of any APIs?

The defining phase is meant to clearly define and document the *product requirements* to place them in front of the customers and get them approved. This is done through a requirement specification document, which consists of all the product requirements to be designed and developed during the project lifecycle. For example, if we determined during the analysis phase that a regulation such as HIPAA is required, here is where we specify that we need 256-bit encryption.

!!!
User involvement is most crucial in this stage. While some development models allow for user involvement in the entirety of the process, user input is most necessary in this phase, where developers can understand the user requirements-what the system/software is actually supposed to produce, in terms of function and performance.
!!!

### 3. Design

Business requirements are most likely to be mapped to software construction in this phase.

System design helps in specifying hardware and system requirements and helps in defining overall system architecture. Formal requirements for risk mitigation/minimization are integrated with the programming designs. The system design specifications serve as input.

!!!
While the requirements for risk mitigation and minimization may be *determined* during the *analysis* phase of the SDLC, they are not integrated with the programming designs until the design phase of the SDLC.
!!!

This is the phase where we would want to identify what *programming language* and architecture we will use as well as specific hardware and system requirements. Threat modeling and secure design elements should also be undertaken and discussed here. For example, since we need to use 256-bit encryption, we should choose AES. Additionally, MFA should be implemented using passwords and retina scans.

Logical design is the part of the design phase of the software development lifecycle in which all *functional* features of the system chosen for development in the analysis phase are described independently of any computer platform.

### 4. Develop

Upon receiving the system design documents, work is divided into modules or units and *actual coding starts*. This is typically the *longest phase* of the software development lifecycle.

Activities include:

- Code review
- Unit testing
- Static analysis

As each portion of code is created and completed, *functional testing* is done on it by the *development team*. This testing is done to ensure that it compiles correctly and operates as intended.

### 5. Test

After the code is developed, it is tested against the requirements to make sure that the product is actually solving the needs gathered during the requirements phase.

In the testing phase, we will use techniques and tools such as:

- Unit testing
- Integration testing
- System testing
- Acceptance testing (users)
- Certification and accreditation (management)

This includes DAST and SAST testing, vulnerability assessments, and penetration tests. Functional *and* nonfunctional (security) testing are performed. If the application does not work *securely*, it does not work at all.

- *Functional testing*. Does the application do what we designed it for?
- *Nonfunctional testing*. Does the application do what we designed it for in a secure manner, with cool graphics, and bells and whistles?

### 6. Maintain

Most software development lifecycle models include a maintenance phase as their endpoint. Overall, this phase includes continuous monitoring and updates as needed, as well as disposal.

The maintenance phase will go on through the entire lifetime of the software or application. The maintenance phase includes pushing out continual updates, bug fixes, security patches, and anything else needed to keep the software running securely and operating as it should.

#### 6.1 Secure Operations

We enter this phase after thorough testing has been successfully completed and the application and its environment are deemed secure.

Proper software configuration management and versioning are essential to application security. The following applications can be useful:

- Puppet
- Chef

This phase calls for the following activities to take place:

- Dynamic analysis
- Vulnerability assessments and penetration testing
- Activity monitoring
- Layer 7 firewalls (such as WAFs)

#### 6.2 Secure Disposal

Once the software has completed its job or has been replaced by a newer or different application, it must then be securely disposed of.
