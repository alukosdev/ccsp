---
label: Federated Identity Management
---

# Federated Identity Management (FIM)

## Acronyms

| Acronym | Backronym |
| - | - |
| FIM | Federated Identity Management |
| IAM | Identity and Access Management |
| IdP | Identity Provider |
| OIDC | OpenID Connect |
| SAML | Security Assertion Markup Language |
| SCIM | System for Cross-domain Identity Management |
| SPML | Service Provisioning Markup Language |
| SSO | Single Sign-On |

## Overview

FIM is the process of asserting an identity *across different systems or organizations*. This is the key enabler of SSO and also core to managing IAM in cloud computing.

FIM is an arrangement that can be made among multiple enterprises that allows subscribers to use the same identification data to obtain access to the networks of all enterprises in the group.

!!!
FIM could essentially be considered SSO but for multiple organizations.
!!!

## Federation Responsibilities

### Cross-Certification Federation / Web-of-Trust

In a cross-certification federation, each member of the federation has to review and approve every other member for inclusion in the federation. This does not scale well, and once the number of organizations gets fairly substantial, it becomes unwieldy.

### Third-Party Certification Federation (Proxy Federation)

In a third-party certification federation, member organizations outsource their responsibilities to review and approve each other to some external party who will take on this responsibility on behalf of all the members.

- In federations where the participating entities are sharing data and resources, *all of those entities are usually the service providers* because they're providing the services.
- In a third-party certification model, the *third-party is the identity provider*; this is often a CASB because they are maintaining the identity repository.
- The cloud provider is neither a federated identity provider nor a federated service provider, unless the cloud provider is specifically chosen as the third-party providing this function.

This is popular in the cloud environment, where the identifier role can often be combined with other functions and outsourced to a CASB.

## Federation Standards

### SAML

SAML is an OASIS standard for federated identity management that supports both *authentication* and *authorization*. It uses XML to make assertions between an IdP and a relying party. Assertions can contain authentication statements, attribute statements, and authorization decision statements. SAML is very widely supported by both enterprise tools and cloud providers but can be complex to initially configure. It is a means for users from outside organizations to be verified and validated as authorized users inside or with another organization without the user having to create identities in both locations.

SAML can include *attributes* like specific features of an app based on job role.

- SCIM or SPML syncs accounts to IdP
- User identity using alukos.com accesses an app (such as O365); this is the service provider
- Service provider recognizes alukos.com and sends request to IdP
- IdP verifies whether user can access the application
- IdP sends back SAML token that asserts the user's legitimacy

In some cases, instead of the service provider sending the request to the IdP, it can send a redirect instead. This means the service provider is informing the client to request their token from the IdP:

1. User tries to access the web application
2. The application redirects the user to the IdP
3. IdP issues a claims token and redirects the user back to the application
4. The application validates the token and authorizes the user by asserting claims, allowing the user to access the authorized protected resources
5. The token is then stored in the session cookie of the user's browser, ensuring the process doesn't have to be repeated for every request.

!!!
SAML 2.0 is the most widely used standard today.
!!!

### OAuth

OAuth is an IETF standard for *authorization* that is very widely used for web services (including consumer services). OAuth is designed to work over HTTP. It is most often used for delegating access control/authorizations between services.

OAuth provides the next step after authentication, specifically authorization, and allows for delegation of permissions. It enables a third-party application to obtain limited access to an HTTP service on behalf of a resource owner by managing an approval interaction between the resource owner and the HTTP service, or by allowing the third-party application to obtain access on its behalf. For example, it may allow Spotify to update Facebook that you're listening to a particular song.

- OAuth is *not* designed for SSO
- OAuth provides delegation of rights to applications

### OIDC

OpenID is a standard for *federated authentication* that is very widely supported for web services. It is based on HTTP with URLs used to identify the identity provider and the user/identity (e.g., identity.alukos.com). OIDC uses REST and JSON.

OIDC allows developers to authenticate their users across websites and applications without having to manage usernames and passwords; it allows information from an IdP to be used instead.

!!!
OIDC is more of an Open Provider (OP) rather than an IdP. For the apps, they're called relying parties.
!!!

### WS-Federation

WS-Federation defines mechanisms to allow different security *realms* to federate, such that authorized access to resources managed in one realm can be provided to security principals whose identities reside in other realms.

!!!
WS-Federation is reliant on SOAP
!!!

!!!
WS-Federation was used mostly by Microsoft and IBM.
!!!

## Federation Roles

When a system or user who is part of a federation needs access to an application and the local system has accepted the credentials, the system or user making the request must obtain local tokens through their own authentication process.

### Identity Provider (IdP)

An IdP is responsible for providing identifiers for users looking to interact with a system, asserting to such a system that an identifier presented by a user is known to the provider, and possibly providing other information about the user that is known to the provider. This can be achieved via an authentication module, which verifies a security token that can be accepted as an alternative to repeatedly explicitly authenticating a user within a security realm.

The IdP is usually referred to as the *source* of the identity in federation. The identity provider isn’t always the authoritative source, but can sometimes rely on the authoritative source, especially if it is a broker for the process.

The IdP *holds all the identities* and generates a token for known users. The IdP is usually the *customer*.

### Relying Party

The relying party is the entity that takes the authentication tokens from an identity provider and *grants access* to resources in federation. The relying party is usually the *service provider* and consumes these tokens.

Said another way, the relying party is the system that *relies* on an identity assertion from an IdP.

!!!
In a cloud environment, it is desirable that the organization itself continues to maintain all identities and act as the IdP.
!!!

![FIM](/static/fim-flow.png)
