---
label: Application Programming Interfaces
---

# Application Programming Interfaces (APIs)

## Acronyms

| Acronym | Backronym |
| - | - |
| API | Application Programming Interface |
| REST | Representation State Transfer |
| SOAP | Simple Object Access Protocol |

## Overview

APIs allow secure communication from one web service to another. This is typically an interface that allows for proper communication to occur. They are the coding components that allow applications to speak to one another, generally through a web interface of some kind.

Regardless of what type of API you use to offer web services, you are granting another application access to the primary application and any data it may have access to.

!!!
APIs consume tokens rather than traditional usernames and passwords.
!!!

## Types of APIs

### REST

REST is a software architecture style consisting of guidelines and best practices for creating scalable web services. It allows web applications to access other applications, databases, and so on in order to extend their functionality. REST is not a protocol. It is a class/category of APIs.

The server does not need to store any temporary information about clients, so sessions are not required. Credentials are used to allow authentication between clients and servers. Generally, a REST interaction involves the client asking the server for data, sometimes as the result of processing; the server processes the request and returns the result. In REST, an enduring session, where the server has to store some temporary data about the client, is not necessary.

REST performs web service requests using uniform resource identifiers (URIs).

Request verbs describe what you will do with a resource. The most common HTTP verbs are POST, GET, PUT, PATCH, and DELETE. Some would say these are properly called "methods." REST HTTP methods correspond to CRUD methods:

- [C]reate (POST)
- [R]ead (GET)
- [U]pdate (PUT)
- [D]elete (DELETE)

#### Principles

REST is based on 5 principles:

- RESTful client-server
- Stateless (sessionless)
- Cache
- Layered System
- Uniform Contract

#### Characteristics

- Lightweight (no envelopes required)
- Caching (performant)
- Scalable
- Uses simple URLs
- Not reliant on XML
- Efficient (smaller messages than XML)
- Reliant on HTTP/S (HTTP/S-only)
- Supports multiple data formats (CSV, JSON, YAML, XML, etc.)
- Widely used

#### Uses

- When bandwidth is limited
- When *stateless* operations are used
- When caching is needed

#### Advantages

- No expensive tools required to interact with the web service
- Smaller learning curve
- Efficient (SOAP uses XML for all messages, REST can use smaller message formats); REST uses what is called "postcards"
- Fast (no extensive processing required)
- Closer to other web technologies in design philosophy

!!!
REST is seemingly the most widely used since it uses HTTP, which is everywhere.
!!!

### SOAP

SOAP is a protocol specification for exchanging structured information in the implementation of web services in computer networks.

SOAP allows programs to operate independently of the client operating system.

- SOAP envelope and then HTTP, FTP, or SMTP
  - Since everything must be "put in an envelope and addressed properly" it adds overhead
- Provides WS-* features
- Should only be used when REST is not available

SOAP uses message-level encryption.

#### Characteristics

- Standards-based
- Reliant on XML (XML-only)
- Reliant on SAML (SAML-only)
- Slower (no caching)
- Highly intolerant of errors
- Built-in error handling

#### Uses

- Asynchronous processing
- Format contracts
- *Stateful* operations

#### Advantages

- Language, platform, and transport independent
- Works well in distributed enterprise environments
- Standardized
- Provides significant pre-build extensibility in the form of the WS* standards
- Built-in error handling
- Automation when used with certain language products

!!!
SOAP should only be used when REST is not possible. Banks typically use SOAP because they can hide the business logic using the envelope and the envelope can be encrypted, which adds a layer of security as it is able to hide some of the logic in the envelope.
!!!

## API Security

- In order to detect possible erroneous or malicious modification of the organization's data by unauthorized or security-deficient APIs, it's important to take representative samples of the production data on a continual basis and perform integrity checks.
- Because untrusted APIs may not be secured sufficiently, increased vigilance for the possibility of introducing malware (such as by using antimalware detection capabilities) into the production environment is essential.
