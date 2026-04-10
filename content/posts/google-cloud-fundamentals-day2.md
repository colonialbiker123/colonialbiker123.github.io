+++ 
draft = false
date = 2026-04-10T21:01:23+05:30
title = "Google Cloud Fundamentals: Core Infrastructure (Day 2)"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++
# Google Cloud Fundamentals: Core Infrasrucutre (Day 2)

# Google Cloud Resource Hierarchy
- Google Cloud’s resource hierarchy contains four levels, and starting from the bottom up they are: resources, projects, folders, and an organization node.
- Resources:
  - Resource represent virtual machines, Cloud Storage buckets, tables in BigQuery, or anything else in Google Cloud.
- Projects:
  - Resources are organized into projects. each resource belongs to exactly one project
  - Projects are the basis for enabling and using Google Cloud services, like managing APIs, enabling billing, adding and removing collaborators, and enabling other Google services.
- Folders:
  - Projects can be organized into folders/ subfolders. A folder can contain projects, other folders, or a combination of both. Folders allow you to group these resources on a per-department basis.
- Organization Node:
  - And then at the top level is an organization node, which encompasses all the projects, folders, and resources in your organization. you can designate an organization policy administrator so that only people with privilege can change policies. You can also assign a project creator role, which is a great way to control who can create projects and, therefore, who can spend money.
- Policies can be defined at the project, folder, and organization node levels.
- Policies are also inherited downward.
- Each Google Cloud project has three identifying attributes: a project ID, a project name, and a project number.
- Google Cloud’s Resource Manager tool is designed to programmatically help you manage projects. It’s an API that can gather a list of all the projects associated with an account, create new projects, update existing projects, and delete projects.

# Identity and Access Management
- Principal:
  - The “who” part of an IAM policy can be a Google account, a Google group, a service account, or a Cloud Identity domain. A “who” is also called a “principal.”
  - Each principal has its own identifier, usually an email address.
- Role:
  - An IAM role is a collection of permissions.
- You can define deny rules that prevent certain principals from using certain permissions, regardless of the roles they're granted.
- There are three kinds of roles in IAM: basic, predefined, and custom.
  - Basic: quite broad in scope. Basic roles include owner, editor, viewer, and billing administrator.
  - predefined: Specific Google Cloud services offer sets of predefined roles, and they even define where those roles can be applied.
  - Custom: if you need to assign a role that has even more specific permissions. Many companies use a “least-privilege” model in which each person in your organization is given the minimal amount of privilege needed to do their job. Custom roles will allow you to define those exact permissions. custom roles can only be applied to either the project level or organization level.

# Service Accounts
- Service accounts allow you to assign specific permissions to a virtual machine, so it can interact with other cloud services without human intervention.
- Service accounts are named with an email address, but instead of passwords they use cryptographic keys to access resources.
- Service accounts do need to be managed.

# Cloud Identity
- When new Google Cloud customers start using the platform, it’s common to log in to the Google Cloud Console with a Gmail account and then use Google Groups to collaborate with teammates who are in similar roles.
- With a tool called Cloud Identity, organizations can define policies and manage their users and groups using the Google Admin Console.
- Admins can log in and manage Google Cloud resources using the same usernames and passwords they already use in existing Active Directory or LDAP systems.
- Using Cloud Identity also means that when someone leaves an organization, an administrator can use the Google Admin Console to disable their account and remove them from groups.

# Interacting with Google Cloud
- Google Cloud console:
  - Google Cloud’s graphical user interface, or GUI, that helps you deploy, scale, and diagnose production issues in a simple web-based interface.
- Google Cloud SDK and Cloud Shell:
  - These include the Google Cloud CLI, which provides the main command-line interface for Google Cloud products and services, and bq, a command-line tool for BigQuery.
  - When installed, all of the tools within the Google Cloud SDK are located under the bin directory.
  - Cloud Shell provides command-line access to cloud resources directly from a browser.
- APIs
  - The Google Cloud console includes a tool called the Google APIs Explorer that shows which APIs are available, and in which versions.
  - Google provides Cloud Client libraries and Google API Client libraries in many popular languages
- Google Cloud app
  - used to start, stop, and use SSH to connect to Compute Engine instances and see logs from each instance. It also lets you stop and start Cloud SQL instances.
  - The Google Cloud app provides up-to-date billing information for your projects and billing alerts for projects that are going over budget.
  - You can set up customizable graphs showing key metrics such as CPU usage, network usage, requests per second, and server errors.
  - The app also offers alerts and incident management.
