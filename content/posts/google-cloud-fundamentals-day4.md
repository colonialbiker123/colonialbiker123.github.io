+++ 
draft = false
date = 2026-04-12T20:51:53+05:30
title = "Google Cloud Fundamentals: Core Infrastructure (Day 4)"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++
# Connecting Networks to Google VPC
- Many Google Cloud customers want to connect their Google Virtual Private Cloud networks to other networks in their system, such as on-premises networks or networks in other clouds.
1. Virtual Private Network connection: over the internet and use Cloud VPN to create a “tunnel” connection. To make the connection dynamic, a Google Cloud feature called Cloud Router can be used.
2. “peering” with Google using Direct Peering: Peering means putting a router in the same public data center as a Google point of presence and using it to exchange traffic between networks.
3. Carrier Peering: Carrier Peering gives you direct access from your on-premises network through a service provider's network to Google Workspace and to Google Cloud products that can be exposed through one or more public IP addresses.
4. Dedicated Interconnect: If getting the highest uptimes for interconnection is important. If these connections have topologies that meet Google’s specifications, they can also be covered by an SLA of up to 99.99%. Also, these connections can be backed up by a VPN.
5. Partner Interconnect: which provides connectivity between an on-premises network and a VPC network through a supported service provider.
6. Cross-Cloud Interconnect: Cross-Cloud Interconnect helps you establish high-bandwidth dedicated connectivity between Google Cloud and another cloud service provider. Google provisions a dedicated physical connection between the Google network and that of another cloud service provider. Cross-Cloud Interconnect supports your adoption of an integrated multicloud strategy. Cross-Cloud Interconnect offers reduced complexity, site-to-site data transfer, and encryption.

# Google Cloud Storage options
- Google Cloud has storage options for structured, unstructured, transactional, and relational data.
- Google Cloud’s five core storage products: Cloud Storage, Cloud SQL, Spanner, Firestore, and Bigtable.

# Cloud Storage:
- Object Storage: Object storage is a computer data storage architecture that manages data as “objects” and not as a file and folder hierarchy (file storage), or as chunks of a disk (block storage).
- These objects are stored in a packaged format which contains the binary form of the actual data itself, as well as relevant associated meta-data (such as date created, author, resource type, and permissions), and a globally unique identifier.
- These unique keys are in the form of URLs, which means object storage interacts well with web technologies.
- Data commonly stored as objects include video, pictures, and audio recordings.
- Cloud Storage’s primary use is whenever binary large-object storage (also known as a “BLOB”) is needed for online content such as videos and photos, for backup and archived data and for storage of intermediate results in processing workflows.
- Cloud Storage files are organized into buckets. A bucket needs a globally unique name and a specific geographic location for where it should be stored, and an ideal location for a bucket is where latency is minimized.
- The storage objects offered by Cloud Storage are immutable, which means that you do not edit them, but instead a new version is created with every change made.
- Administrators have the option to either allow each new version to completely overwrite the older one, or to keep track of each change made to a particular object by enabling “versioning” within a bucket.
- With object versioning enabled, you can list the archived versions of an object, restore an object to an older state, or permanently delete a version of an object, as needed.
- Using IAM roles and, where needed, access control lists (ACLs), organizations can conform to security best practices, which require each user to have access and permissions to only the resources they need to do their jobs, and no more than that.
- Each access control list consists of two pieces of information. The first is a scope, which defines who can access and perform an action. The second is a permission, which defines what actions can be performed, like read or write.
- Cloud Storage also offers lifecycle management policies. For example, you could tell Cloud Storage to delete objects older than 365 days; or to delete objects created before January
