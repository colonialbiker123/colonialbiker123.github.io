+++ 
draft = false
date = 2026-04-09T21:07:34+05:30
title = "Google Cloud Fundamentals: Core Infrastructure (Day 1)"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++
# Google Cloud Fundamentals: Core Infrastructure (Day 1)

## Introduction
- Google Cloud offerings can be broadly categorised as compute, storage, big data, machine learning, and application services for web, mobile, analytics, and back-end solutions.
- 5 important traits:
  - Customers get computing resources that are on-demand and self-service.
  - Customers get access to those resources over the internet, from anywhere they have a connection.
  - the cloud provider has a big pool of those resources and allocates them to users out of that pool.
  - the resources are elastic–which means they’re flexible, so customers can be.
  - customers pay only for what they use, or reserve as they go.
- Some history:
  - a first wave known as colocation. Colocation gave users the financial efficiency of renting physical space, instead of investing in data center real estate.
  - Second Wave: The components of virtualized data centers match the physical building blocks of hosted computing—servers, CPUs, disks, load balancers, and so on—but now they’re virtual devices. it also remains a user-controlled and user-configured environment.
  - Third Wave: Google switched to a container-based architecture— a fully automated, elastic third-wave cloud that consists of a combination of automated services and scalable data.
- Compute Engine is an example of a Google Cloud IaaS service.
- App Engine is an example of a Google Cloud PaaS service.
- SaaS provides the entire application stack, delivering an entire cloud-based application that customers can access and use.
- In the IaaS model, customers pay for the resources they allocate ahead of time; in the PaaS model, customers pay for the resources they actually use.
- As cloud computing has evolved, the momentum has shifted toward managed infrastructure and managed services.
- Serverless allows developers to concentrate on their code, rather than on server configuration, by eliminating the need for any infrastructure management.
- Cloud Run: allows customers to deploy their containerized microservices based application in a fully-managed environment.
- Cloud Run functions: manages event-driven code as a pay-as-you-go service.

## The Google Cloud Network
- Google Cloud’s infrastructure is based in seven major geographic locations: North America, South America, Europe, Africa, the Middle East, Asia, and Australia.
- Regions represent independent geographic areas and are composed of zones. For example, London, or europe-west2, is a region that currently comprises three different zones. A zone is an area where Google Cloud resources are deployed.
- Spanner multi-region configurations allow you to replicate the database's data not just in multiple zones, but in multiple zones across multiple regions, as defined by the instance configuration.

## Security
- Hardware Infrastructure Layer:
  - hardware design and provenance: Google also designs custom chips, including a hardware security chip that's currently being deployed on both servers and peripherals.
  - secure boot stack: to ensure that they are booting the correct software stack, such as cryptographic signatures over the BIOS, bootloader, kernel, and base operating system image.
  - premises security: limited to only a very small number of Google employees.
- Service deployment layer
  - encryption of inter-service communication: Google’s infrastructure provides cryptographic privacy and integrity for remote procedure call (“RPC”) data on the network. Google has started to deploy hardware cryptographic accelerators that will allow it to extend this default encryption to all infrastructure RPC traffic inside Google data centers.
- User Identity Layer
  - Google’s central identity service, which usually manifests to end users as the Google login page, goes beyond asking for a simple username and password. Users can also employ secondary factors when signing in, including devices based on the Universal 2nd Factor (U2F) open standard.
- Storage services layer
  - encryption at rest security feature: encryption using centrally managed keys is applied. Google also enables hardware encryption support in hard drives and SSDs.
- Internet communication layer:
  - Google services that are being made available on the internet, register themselves with an infrastructure service called the Google Front End, which ensures that all TLS connections are ended using a public-private key pair and an X.509 certificate from a Certified Authority (CA), as well as following best practices such as supporting perfect forward secrecy.
  - Denial of Service (“DoS”) protection: multi-tier, multi-layer
- Operational security layer
  - intrusion detection: Rules and machine intelligence give Google’s operational security teams warnings of possible incidents. Red Team exercises to measure and improve the effectiveness of its detection and response mechanisms.
  - Reducing insider risk: Google aggressively limits and actively monitors the activities of employees who have been granted administrative access to the infrastructure.
  - employee U2F use: employee accounts require use of U2F-compatible Security Keys.
  - stringent software development practices: Google employs central source control and requires two-party review of new code. Google runs a Vulnerability Rewards Program where we pay anyone who is able to discover and inform us of bugs in our infrastructure or applications. Google also provides its developers libraries that prevent them from introducing certain classes of security bugs.

## Open Source Ecosystems:
- For example, TensorFlow, an open source software library for machine learning developed inside Google, is at the heart of a strong open source ecosystem.
- Kubernetes and Google Kubernetes Engine give customers the ability to mix and match microservices running across different clouds, while Google Cloud Observability lets customers monitor workloads across multiple cloud providers.

## Pricing and Billing:
- How can I make sure I don’t accidentally run up a big Google Cloud bill?
  - You can define budgets at the billing account level or at the project level.
  - To be notified when costs approach your budget limit, you can create an alert. Alerts are generally set at 50%, 90% and 100%, but can also be customized.
  - Reports is a visual tool in the Google Cloud Console that allows you to monitor expenditure based on a project or services.
  - Google Cloud also implements quotas, which are designed to prevent the over-consumption of resources because of an error or a malicious attack, protecting both account owners and the Google Cloud community as a whole.
  - Rate quotas reset after a specific time. For example, by default, the GKE service implements a quota of 3,000 calls to its API from each Google Cloud project every 100 seconds.
  - Allocation quotas govern the number of resources you can have in your projects. For example, by default, each Google Cloud project has a quota allowing it no more than 15 Virtual Private Cloud networks.
