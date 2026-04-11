+++ 
draft = false
date = 2026-04-11T13:03:05+05:30
title = "Google Cloud Fundamentals: Core Infrastructure (Day 3)"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++
# Virtual Private Cloud Networking
- A virtual private cloud, or VPC, is a secure, individual, private cloud-computing model hosted within a public cloud – like Google Cloud!
- VPCs combine the scalability and convenience of public cloud computing with the data isolation of private cloud computing.
- Google VPC networks are global. They can also have subnets, which is a segmented piece of the larger network, in any Google Cloud region worldwide. Subnets can span the zones that make up a region.

# Important VPC Capabilities
- VPCs have routing tables. VPC routing tables are built-in so you don’t have to provision or manage a router.
- They’re used to forward traffic from one instance to another within the same network, across subnetworks, or even between Google Cloud zones, without requiring an external IP address.
- VPCs provide a global distributed firewall, which can be controlled to restrict access to instances through both incoming and outgoing traffic.
- With VPC Peering, a relationship between two VPCs can be established to exchange traffic
- Alternatively, to use the full power of Identity Access Management (IAM) to control who and what in one project can interact with a VPC in another, you can configure a Shared VPC

# Compute Engine
- users can create and run virtual machines on Google infrastructure.
- The instance can run Linux and Windows Server images provided by Google or any customized versions of these images. You can also build and run images of other operating systems and flexibly reconfigure virtual machines.
- Compute Engine bills by the second with a one-minute minimum, and sustained-use discounts start to apply automatically to virtual machines the longer they run.
- So, for each VM that runs for more than 25% of a month, Compute Engine automatically applies a discount for every additional minute.
- Cloud Marketplace: which offers solutions from both Google and third-party vendors.
- Preemptible and Spot VMs: Let’s say you have a workload that doesn’t require a human to sit and wait for it to finish–such as a batch job analyzing a large dataset. You can save money, in some cases up to 90%, by choosing Preemptible or Spot VMs to run the job.
- A Preemptible or Spot VM is different from an ordinary Compute Engine VM in only one respect: Compute Engine has permission to terminate a job if its resources are needed elsewhere.
- preemptible VMs can only run for up to 24 hours at a time, but Spot VMs do not have a maximum runtime.

# Scaling Virtual Machines
- Compute Engine has a feature called Autoscaling, where VMs can be added to or subtracted from an application based on load metrics.
- Google’s Virtual Private Cloud (VPC) supports several different kinds of load balancing
- The maximum number of CPUs per VM is tied to its “machine family” and is also constrained by the quota available to the user, which is zone-dependent.

# Cloud Load Balancing
- Cloud Load Balancing is a fully distributed, software-defined, managed service for all your traffic.-
- You can put Cloud Load Balancing in front of all of your traffic: HTTP or HTTPS, other TCP and SSL traffic, and UDP traffic too.
- Cloud Load Balancing provides cross-region load balancing, including automatic multi-region failover, which gently moves traffic in fractions if backends become unhealthy.
- Application Load Balancers operate at the application layer and are designed to handle HTTP and HTTPS traffic. Application Load Balancers operate as reverse proxies, distributing incoming traffic across multiple backend instances based on rules you define.
- Network Load Balancers operate at the transport layer and efficiently handle TCP, UDP, and other IP protocols.
  - Proxy Network Load Balancers also function as reverse proxies, terminating client connections and establishing new ones to backend services.They offer advanced traffic management capabilities and support backends located both on-premises and in various cloud environments.
  - passthrough Network Load Balancers do not modify or terminate connections. Instead, they directly forward traffic to the backend while preserving the original source IP address.

# Cloud DNS and Cloud CDN
- One of the most famous free Google services is 8.8.8.8, which provides a public Domain Name Service to the world.
- Cloud DNS: It’s a managed DNS service that runs on the same infrastructure as Google. It has low latency and high availability, and it’s a cost-effective way to make your applications and services available to your users.
- Cloud DNS is also programmable. You can publish and manage millions of DNS zones and records using the Cloud console, the command-line interface, or the API.
- Edge caching refers to the use of caching servers to store content closer to end users. Google also has a global system of edge caches. You can use this system to accelerate content delivery in your application by using Cloud CDN - Content Delivery Network.
- After an Application Load Balancer is set up, Cloud CDN can be enabled with a single checkbox.
