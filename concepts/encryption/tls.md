---
label: TLS
---

!!!danger
This page is currently queued for revision.
!!!

# Transport Layer Security (TLS)*

## Acronyms, Abbreviations, and Initialisms

Short Form | Full Form
:--- | :---
DAR | Data at Rest
DIM | Data in Motion
DIT | Data in Transit
TLS | Transport Layer Security

## Glossary

=== TLS Authentication
When the server proves its identity to the client.
===

## Overview

In TLS, the parties will establish a shared secret, or *symmetric key*, for the duration of the session. The session key is uniquely generated each time a new connection is made. Asymmetric encryption is used in establishing a secure TLS connection.

TLS relies on PKI certificates authenticated and issued by a trusted third-party.

### Characteristics

- NAT friendly
- More performance intensive than IPsec
- More devices support TLS than IPsec

!!!
TLS is *communication* based (DIM/DIT), not storage based (DAR).
!!!

## Components

### Handshake Protocol

The Handshake Protocol allows the client and the server to authenticate each other and to *negotiate an encryption algorithm* and *cryptographic key exchange* before data is sent or received.

The TLS handshake protocol takes care of the *authentication and key exchange* necessary to establish or resume secure sessions. To establish a secure session, the Handshake Protocol handles the following:

- Cipher suite negotiation
- Authentication of the server and client
- Session key information exchange

This protocol is what negotiates and establishes the actual TLS connection.

### Record Protocol

The TLS Record Protocol *uses the keys* setup during the TLS handshake to *secure application data*.

Provides *connection security* and ensures that the connection is private and reliable. Used to encapsulate higher-level protocols, among them the TLS Handshake Protocol. The TLS Record Protocol is the actual *secure communication method for transferring the data*.

Provides connection security, reliability, and ensures the connection will be private. It is also leveraged to verify integrity and origin of the application data.

- Fragmentation and reassembly of messages.
- Compression and decompression of outgoing/incoming blocks.
- Applies a Message Authentication Code (MAC) to outgoing messages, and verifies incoming messages using the MAC.
- Encrypts and decrypts messages.
