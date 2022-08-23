---
icon: stop
---

!!!danger
This page has not yet been revised for 2022.
!!!

# Storage

+++ IaaS
- Volume storage
- Object storage
+++ PaaS
- Structured storage
- Unstructured storage

!!!
If storage is accessible via API, then it's considered PaaS.
!!!
+++ SaaS
- Information storage and management (long-term)
- Content and file storage (long-term)
- Raw storage
- Ephemeral storage
- Content delivery network (CDN)
+++

## Storage Architectures

### Volume Storage

With volume storage, the customer is allocated a storage space within the cloud; this storage space is represented as an attached drive to the user's virtual machine. From the customer's perspective, the virtual drives performs very much in the same manner as would a physical drive attached to a tangible device.

Volume storage contains two subset storage types:

- File Storage
- Block Storage

=== File Storage
With file storage, the data is stored and displayed just as with a file structure in the legacy environment (as files and folders), with all the same hierarchical naming functions.

Features of file storage include:

- File sharing
- Local archiving
- Data protection

File storage is commonly implemented in:

- Big data analytical tools and processes
- NAS
=== Block Storage
Block storage is a blank volume that the customer or user can put anything into.

Features of block storage include:

- Flexibility
- Performance

Challenges of block storage include:

- Requires greater administration
- May require OS or application to store, sort, and retrieve data

Use cases for block storage include:

- Data of multiple types and kinds, such as enterprise backup services

Common implementations of block storage include:

- iSCSI
- SAN
- RAID
- VMFS
- Email servers (such as Microsoft Exchange)
===

### Object Storage

This type of cloud storage arrangement involves the use of associating metadata with the saved data. Data objects (files) are saved in the storage space along with relevant metadata such as content type and creation date. Data is stored as objects, not as files or blocks. Objects include the content, metadata describing the content and object, and a unique address identifier for locating that object.

An object storage system typically comes with minimal features. It gives the ability to store, copy, retrieve, and delete files and also gives authority to control which user can perform these actions. If you want to be able to search or have an object metadata central repository for other apps to draw on, you have to do it by yourself. Many storage systems such as Amazon S3 provide REST APIs and web interfaces to allow programmers to work with objects and containers.

Challenges of object storage include:

- Write-once, read many (WORM) makes object storage unsuitable for databases.
- Replication is not complete until all versions have been synchronized, which takes time. This makes object storage unsuitable for data that constantly changes, but a good solution for stagnant data.

Use cases for object storage include:

- When significant levels of description are required, including marking, labels, and classification and categorization.
- When data requires indexing capabilities.
- When data requires data policy enforcement (such as IRM/DRM or DLP).
- Centralization of some data management functions.
- Unstructured data such as music, images, and videos.
- Backup and log files.
- Large sets of historical data.
- Archived files.
- Big data endeavors.

Common implementations of object storage include:

- Amazon S3
- CDNs

Security for object storage can be provided by using:

- *IRM/DRM (file-level or file-based encryption)*. Protects against *hardware* theft. Any process or user that has access to the OS still has access to the data.

### Structured Storage

Structured storage includes information with a high degree of organization, such that inclusion in a relational database is seamless and readily searchable by simple, straightforward search engine algorithms or other search operations.

#### Databases

Databases are considered structured data. Data will be arranged according to characteristics and elements in the data itself, including a specific trait required to file the data known as the primary key. In the cloud, the database is usually backend storage in the datacenter, accessed by users utilizing online apps or APIs through a browser.

Databases may be installed on object (undesirable) or volume storage.

!!!
Databases are most often configured to work with PaaS and SaaS.
!!!

### Unstructured Storage

Unstructured storage includes information that does not reside in a traditional row-column database.

#### Examples

- Email messages
- Word processing documents
- Videos
- Photos
- Audio files
- Presentations
- Web pages

Although these sorts of files may have an internal structure, they are still considered unstructured because the data they contain does not fit neatly in a database.

### Information Storage and Management

Data is entered into the system through a web interface and stored within the SaaS application (usually a back-end database). This data storage utilizes database, which in turn are installed on object or volume storage.

### Content and File Storage

File-based content is stored within the application and made accessible via the web-based user interface.

### Ephemeral Storage

This type of storage exists only as long as the instance is online. It is typically used for swap files and other temporary storage needs and is terminated with its instance.

### Content Delivery Network (CDN)

With a CDN, content is stored in *object* storage, which is then distributed to multiple geographically distributed nodes to improve Internet consumption speed.
A CDN is a form of data caching, usually near geophysical locations of high use demand, for copies of data commonly requested by users.

Use cases for CDNs include:

- Online multimedia streaming services; rather than dragging data from a datacenter to users at variable distances across a continent, the streaming service provider can place copies of the most requested media near metropolitan areas where those requests are likely to be made, thus improving bandwidth and delivery quality.

### Raw Storage

Raw storage or raw device mapping (RDM) is an option in the VMware server virtualization environment that enables a storage LUN to be directly connected to a VM from the SAN.

## Storage Networks

==- Challenge Handshake Authentication Protocol (CHAP)
CHAP is used to periodically verify the identity of the client using a three-way handshake. This is done upon initial link establishment and may be repeated any time after the link has been established.
==- Initiators
The *consumer* of storage, typically a server with an adapter card in it called a HBA. The initiator commences a connection over the fabric to one or more ports on your storage system, which are called target ports.
==- Kerberos
Kerberos is a network authentication protocol that uses secret-key (symmetric) cryptography.
==- Network-Attached Storage (NAS)
A NAS is a network file server with a drive or group of drives, portions of which are assigned to users on that network. The user will see a NAS as a file server and can share files to it. NAS commonly uses TCP/IP.
==- Secure Remote Password (SRP)
SRP is a secure password-based authentication and key-exchange protocol. SRP uses a strong secret to enable parties to security communicate.
==- Storage Area Network (SAN)
A SAN is a group of devices connected to the network that provide storage space to users. Typically, the storage apportioned to the user is mounted to that user's machine, like an empty drive. The user can then format and implement a filesystem in that space according to their own preference. SANs usually use iSCSI or Fibre Channel protocols.
==- Simple Public-Key Mechanism (SPKM)
SPKM provides authentication, key establishment, data integrity, and data confidentiality in an online distributed application requirement.
SPKM is good for any application that uses GSSAPI calls.

The use of SPKM requires a PKI, which generates digital signatures for ensuring nonrepudiation.
==- Targets
The ports on your storage system that deliver storage volumes (called target devices or LUNs) to the initiators.
==-

### Protocols

#### iSCSI

iSCSI is an IP-based (layer 3) storage networking standard for linking data storage facilities. It provides *block-level* access to storage devices by carrying SCSI commands over a TCP/IP network. Because iSCSI is a layer 3 solution, it will permit routing of the traffic.

##### Best Practices

-  Storage network traffic should not be shared with other network traffic (management, fault tolerance, or vMotion). A dedicated, local LAN or private VLAN should be provisioned to segregate iSCSI traffic.
- iSCSI does not handle overprovisioning of resources in a graceful manner. This practice should be avoided.
- iSCSI is unencrypted. Encryption must be added separately through IPsec (tunneling) and IKE (security).
- iSCSI supports authentication from the following protocols:
  - Kerberos
  - SRP
  - SPKM
  - CHAP

## Storage Operations

### Tightly Coupled

All the storage devices are directly connected to a shared physical backplane, thus connecting all of them directly. Each component of the cluster is aware of the others and subscribes to the same policies and rulesets.

- Proprietary
- Shared physical backplane and network fixes the maximum size of the cluster
- Delivers a high-performance interconnect between servers
  - Allows for load-balanced performance
  - Allows for maximum scalability as the cluster grows (array controllers, I/O ports, and capacity can be added into the cluster as required to service the load)
- Fast, but loses flexibility*

!!!
A tightly coupled cluster is usually confined to more restrictive design parameters, often because the devices might need to be from the same vendor (proprietary) in order to function properly. Although this may be a limiting factor, a tightly coupled architecture will also enhance performance as it scales.
!!!

### Loosely Coupled

A loosely coupled cluster will allow for greater flexibility. Each node of the cluster is independent of the others, and new nodes can be added for any purpose or use as needed. They are only logically connected and don't share the same proximate physical framework, so they are only distantly physically connected through communication media.

A loose cluster offers performance, I/O, and storage capacity *within the same node*. As a result, performance scales with capacity and vice versa.

- Cost-effective
- Can start small and grow as demand requires
- Performance, I/O, and storage capacity are all contained within the same node
  - This allows performance to scale with capacity
- Scalability is limited by the performance of the interconnect

In a loosely coupled storage cluster, each node acts as an independent data store that can be added or removed from the cluster without affecting other nodes. This, however, means that the overall cluster's *performance/capacity depends on each node's own maximum performance/capacity*. Because each node in a loosely coupled architecture has its own limitations, the number of nodes will not affect overall performance.

- Distributed.
- Built for servers in multiple locations.

## Storage Types

### Primary Storage

- RAM

### Secondary Storage

- Media (HDD, CD/DVD, tape, etc.)
