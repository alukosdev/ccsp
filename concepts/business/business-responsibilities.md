!!!danger
This page is currently queued for revision.
!!!

# Business Responsibilities*

## Responsibilities in the Cloud

### Shared Responsibilities

### Shared Administration

### Cloud Provider Responsibilities

#### The Physical Plant

- Buy versus lease.
- Secure Hardware Components
- Manage hardware configuration.
- Set hardware to log events and incidents.
- Determine compute component composition by customer need.
- Configure secure remote administrative access.

#### Secure Logical Framework

- Installation of Virtual OSs
- Secure Configuration of Various Virtualized Elements

#### Secure Networking

- Firewalls
- IDS/IPS
- Honeypots
- Vulnerability Assessments
- Communication Protection
  - Encryption
  - Virtual Private Networks (VPNs)
  - Strong Authentication

#### Mapping and Selection of Controls

### Data Access

#### Customer Directly Administers Access

- User contacts the organization's administrator to request an account
- The administrator confirms the account necessity and permissions (perhaps with the user's manager or HR)
- The administrator logs onto the cloud system and makes the necessary modification to the ACL(s)
- The administrator notifies the user, and the user now has access

#### Provider Administers Access on Behalf of the customer

- User contacts the provider's administrator to request an account
- The administrator confirms the account necessity and permissions with the cloud customer POC
- The customer POC confirms the account necessity and permissions with the user's office/HR
- The customer POC passes verification to the cloud administrator
- The cloud administrator makes the necessary modification to the ACL(s)
- The administrator notifies the user, and the user now has access

#### Third-Party (CASB) Administers Access on Behalf of the Customer

- User contacts the CASB to request an account
- The CASB confirms the account necessity and permissions with the cloud customer POC
- The customer POC confirms the account necessity and permissions with the user's office/HR
- The customer POC passes verification to the CASB
- The CASB logs onto the cloud system and makes the necessary modification to the ACL(s)
- The CASB notifies the user, and the user now has access

### Physical Access

#### Audits

- SOC

#### Policy

#### Monitoring and Testing
