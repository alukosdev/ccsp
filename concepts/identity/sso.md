---
icon: stop
label: SSO
---

!!!danger
This page has not yet been revised for 2022.
!!!

# Single Sign-On (SSO)

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
FIM | Federated Identity Management
RSO | Reduced Sign-On
SCIM | System for Cross-domain Identity Management
SPML | Service Provisioning Markup Language
SSO | Single Sign-On

## Glossary

=== Federated SSO
Federated SSO is typically used for facilitating interorganizational and intersecurity domain access to resources leveraging federated identity management.
=== Reduced Sign-On (RSO)
Not to be confused with SSO or federated SSO, RSO refers to not having to sign into each piece of data or store once authorization has been granted. It generally operates through some form of credential synchronization. RSO introduces security issues not experienced by SSO because the nature of SSO eliminates usernames and other sensitive data from traversing the network.

!!!
The foundation of federation relies on the existence of an identity provider; therefore, RSO has no place in a federated identity system.
!!!
===

## Overview

SSO refers to a situation where the user signs in once, usually to an authentication server; then when the user wants to access the organization's resources, each resource will query the authentication server to determine if the user is logged in and properly authenticated; the authentication server then approves the request and the resource server grants the user access.

SSO ensures that a single user authentication process grants access to multiple systems or even organizations.

SSO is a subset of FIM, as it relates only to *authentication* and technical interoperability. It leverages federated trusts to implement a streamlined process of SSO in the cloud account provisioning process (using SPML or SCIM).

- Authentication occurs a single time using SAML, OIDC, or WS-Federation.
- Authorization occurs using SAML or OAuth.
