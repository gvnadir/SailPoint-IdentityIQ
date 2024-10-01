# SailPoint - IdentityIQ Introduction

# Table of Contents

1. **[Introducing IdentityIQ](#introducing-identityiq)**
	1. [Benefits](#benefits)  
	2. [IdentityIQ Capabilities](#identityiq-capabilities)  
		1. [Lifecycle Management](#lifecycle-management)  
		2. [Compliance Management](#compliance-management)  
2. **[Identities: Core of Security](#identities-core-of-security)**
   1. [Attribute](#attribute)  
   2. [Entitlement](#entitlement)  
   3. [Aggregation](#aggregation)  
   4. [Correlation](#correlation)  
		1. [Governance Model Steps](#governance-model-steps)  

4. **[Access Requests](#access-requests)**
   1. [Provisioning Plan](#provisioning-plan)  
   2. [Workflow](#workflow)  

5. **[Provisioning](#provisioning)**
   1. [Event-Driven Provisioning](#event-driven-provisioning)  
   2. [Event-Driven Provisioning Process](#event-driven-provisioning-process)  
   3. [Lifecycle Events with Rapid Setup](#lifecycle-events-with-rapid-setup)  

6. **[Certification and Access Reviews](#certification-and-access-reviews)**
   1. [Certification Steps](#certification-steps)  

7. **[Policies](#policies)**
   1. [Separation of Duties (SoD)](#separation-of-duties-sod)  
   2. [Dormant Accounts](#dormant-accounts)  
   3. [Acting on Violations](#acting-on-violations)  

8. **[Analytics and Reports](#analytics-and-reports)**
   1. [Advanced Analytics](#advanced-analytics)  
   2. [IdentityIQ Reports](#identityiq-reports)  

9. **[Roles](#roles)**
   1. [IdentityIQ Roles](#identityiq-roles)  
   2. [Increase Efficiency](#increase-efficiency)  
   3. [Reduce Risk](#reduce-risk)  
   4. [Automatic Role Assignment](#automatic-role-assignment)  
   5. [Role Modeling Options](#role-modeling-options)  

10. **[Extending IdentityIQ](#extending-identityiq)**
    1. [Extended Attributes](#extended-attributes)  
    2. [Rules & Branding](#rules--branding)  
    3. [Workflows](#workflows)  
    4. [Quicklinks](#quicklinks)  
    5. [Custom Connectors](#custom-connectors)  
    6. [More on extended attributes](#more-on-extended-attributes)
    7. [Other Objects to Extend](#other-objects-to-extend)  

11. **[IdentityIQ Plugins](#identityiq-plugins)**


## Introducing IdentityIQ

SailPoint IdentityIQ provides:

- Operational efficiency
- Integration with existing systems
- Access to all your identities
- Compliance to enterprises with complex environments

### Benefits

- Stregthen security and lower risk
- Improve compliance and audit performance
- Deliver fast, efficient access for the business

### IdentityIQ Capabilities

**IdentityIQ Compliance Manager** and **Lifecycle Manager** are **IdentityIQ modules** that provide access management for the applications used by an enterprise and they share:

- Data and Database (Application Access Data)
- User Interface
- Implementation process

**Integrated solutions** are **not** IdentityIQ modules, and have separate:

- Databases
- User Interface
- Implementation processes
- AI-Driven Identity Security (discover, manage, and control all your access-related data using machine learning and data intelligence)
- File Access Manager (helps locate and secure sensitive data, meet data privacy requirements and certify data access)

#### Lifecycle Management

- Flexible approval model
- Policy enforcement
- Automated lifecycle event management (as user join the company, switch roles, or leave)
- Batch updates (allow an IT team to make changes for a set of users)
- Automated provisioning to connected applications

#### Compliance Management

- Functionality for applying security standards
- Access Certifications to ensure the users hold only the access they need
- Policy scanning and violation detection

## Identities: Core of Security

> **Identities** represent the users who have access to your corporate system and data. They include anyone or anything that has access to your enterprise systems, including employees, contractors, partners, even robotic users.

IdentityIQ represents each user with an **Identity cube**. It stores all the data collected and used by IdentityIQ for a single user, including identity attributes, enterprise accounts, and type of access held by the user.

### Attribute

A property of an identity, account, application, or entitlment. Attributes often drive IdentityIQ processes. For example, a user's location may be used to give them application access.

### Entitlement

Also known as **permissions**, are the type of access a user has when logging into an application.

### Aggregation

The process of collecting or **reading** data from applications in your organization. Regular, periodic aggregation is key to keeping identity cubes up to date.

### Correlation

Correlation rules ensure that the right data is associated with the right identity. 

#### Governance Model Steps

1. **Aggregation**: Process of collecting data from the applications in your origanization, the key to keeping identities up-to-date
2. **Compliance Management**: With this module, the enterprise can confirm that the users have only the access they need
3. **Lifecycle Management**: Changes management to identities over time

## Access Requests

>Users can ask for changes to access by requesting the _addition_ or _removal_ of **roles** and **entitlements**. Access requests are a function of the IdentityIQ Lifecycle Manager module.

### Provisioning Plan

Submitting the request creates a **provisioning plan** to represent the request and kicks off the appropriate **workflow**.

### Workflow

The workflow definition determines how iiq process the request. For example the workflow can include a policy evaluation. Then the workflow handles submitting the request provisioning.	

## Provisioning

> Provisioning refers to the **process of granting or revoking access** to various systems, applications, and resources based on defined policies and rules. It involves creating, modifying, or deleting user accounts, roles, and permissions across an organization's IT infrastructure. 

### Event-Driven Provisioning

>Event-driven provisioning is an **automated** process used to keep an identity's access current with their job needs and responsibilities. With it, enterprises can automatically provision or change access that’s required and remove access that's no longer necessary.

### Event-Driven Provisioning Process

1. _IdentityIQ monitors data_: looking for changes, also known as **events**
2. _IdentityIQ detects changes_: when an event, or change, is detected by IdentityIQ, provisioning is initiated. For example, an identity's department attribute has changed
3. _IdentityIQ provisioning data_: the process of **writing** the changes to the systems or applications that are defined to IdenitityIQ

### Lifecycle Events with Rapid Setup

Event-driven provisioning is provided in IdentityIQ using **lifecycle events**. Rapid Setup provides pre-configured processes to streamline these lifecycle events:

- **Joiners** are new identities that are starting with the company. 
- **Movers** include identities that are moving to a new location or department or those changing job titles.
- **Leavers** are identities that are departing the company. 

## Certification and Access Reviews

> **Certification**, also called access certification, is the process of collecting and reviewing the access that identities hold on IT-controlled systems in your organization.

During the certification process, a user's set of access is reviewed by certifier, often a manager or application or entitlement owner. The certifier makes the decision to approve or reject the access that a user currently holds. Certifications should be performed regularly, such as quarterly or annually, to ensure users have only the access they need.

### Certification Steps

Steps of a sample manager certification campaign:

1. **A certification campaign is created**

   A compliance officer creates a manager certification campaign to require all managers to review and certify the access of their direct reports. The campaign creator also specifies when the campaign will run, how long it will last, and other key dates.

2. **Access information is collected**

   IdentityIQ collects and compiles all the required information related to identities, points of access, applications, and more. This process can take minutes, hours, or even days depending on the size of the campaign.

3. **Access reviews are created for certifier review**

   During the generation phase, an access review is created for each certifier designated in the certification campaign, and you can configure IdentityIQ to notify the certifiers that they have access reviews awaiting their action. A typical certification campaign may require certifiers to complete their reviews in a 2 or 4 week timeframe.

4. **Each manager approves or revokes access**

   Managers open their assigned access reviews and approve or revoke access for their employees. If AI-Driven Access Recommendations is deployed in the organization, managers will see a suggestion, based on comparisons with other identities, for each access.

5. **Challenge, sign-off, and revocation**

   An optional challenge phase allows users who would lose access to challenge that decision, and certifiers can reconsider their decisions.

   Once finalized, the managers sign-off on the access review, then IdentityIQ begins the revocation process, as needed.

## Policies

> An IdentityIQ policy defines user access conditions that are _unwanted_ by the organization. IdentityIQ policies define the access business policies of your enterprise. First, you define a policy, then IdentityIQ can prevent that condition from occurring or check the identities for that condition.

### Separation of duties (SoD)

SoD policies ensure that users do not hold conflicting access; these policies are very common in many organizations. Generally, SoD policies ensure that no single user has access or responsibility for entire process, such as approving new vendors and also paying those vendors.

### Dormant accounts

Accounts that are unused for excessive lengths of time, can lead to two problems:

- They can cost an organization money for application accounts that aren't being used and they can become a security risk
- If no one is using an account, no one will notice if it is compromised

### Acting on Violations

The person assigned as the violation owner can take action on the violation through an assigned work item. Depending upon the type of violation, there are three possible actions that the owner can take:

- Allow it
- Correct it
- Certify the identity. Administrators have this option, which allows them to take a look at all access held by the user and make decisions about that access

A key purpose of the policy detection process is to ensure that someone is aware of undesired access and can take action to fix the problem. Once you've seen the violation, you can take steps to address it, which may involve actions outside of IdentityIQ. In IdentityIQ, you can allow the violation as an exception for a certain period of time. If the problem still exists after that time period ends, IdentityIQ will flag it again so it isn't forgotten.

## Analytics and Reports

### Advanced Analytics

IdentityIQ's powerful search mechanism is called Advanced Analytics. This feature allows you to easily search the IdentityIQ database. Search options will vary according to the configuration of IdentityIQ. For example, only attributes designated as searchable, will appear for selection.

The results can be viewed in IdentityIQ, saved for future searches, saved as a report, or exported as a CSV file.

The **identity search** is the most common type of search but there are many types of searches you can perform, including activity, role, entitlement, and audit.

### IdentityIQ Reports

IdentityIQ reports provide up-to-date information to meet compliance needs and ease decision-making for your implementation.

IdentityIQ provides over 50 standard report options, organized by category, to display your data in a variety of meaningful ways, minimizing the need to manually search for information. Standard reports can be run without making any changes, or they can be configured to meet your specific needs.

## Roles

> A **role** is a collection of one or more entitlements (permissions) encapsulated into a single object.

### IdentityIQ Roles

In IdentityIQ, roles provide a way to define access for an individual. IdentityIQ provides a robust role model and role types to help model the access of users in your organization.

While roles are not required in IdentityIQ, they are beneficial in two significant ways:

- Increased efficiency
- Reduced risk

### Increase Efficiency

When you use a role to group individual entitlements, you ensure that every time an interaction, such as a request or access review, occurs, users are dealing with one role instead of numerous entitlements. This increases the efficiency of items like access requests and approval and access reviews

### Reduce Risk

If users must work with many individual entitlements, it's easier to make a mistake and request or approve inappropriate access. Managers may not be aware of which exact entitlements are required by employees. Working with a single role decreases the chances that they will request or approve more access than is necessary.

### Automatic Role Assignment

Roles can be automatically assigned to users based on a rule. An assignment rule will commonly match an attribute of the identity, like a department or job title, with the attribute specified in the rule.

If the user's job title changes, IdentityIQ will recognize that his job title no longer matches the rule, and the role and its entitlements will be de-provisioned.

### Role Modeling Options

Roles are typically modeled, built, and maintained by business analysts working in conjunction with application owners and business teams.

## Extending IdentityIQ

IdentityIQ’s robust functionality can be extended to meet the needs of businesses that have complex processes, detailed data requirements, and stringent industry regulations. There are multiple levels for extension.

### Extended Attributes

All implementations include extended attributes, such as department, location, job title. These are **data that your enterprise needs to manage your identity access program**.

### Rules & Branding

Most implementations use rules, **little snippets of code injected into the IdentityIQ logic**. Most will also brand IdentityIQ with their own colors and logos.

### Workflows

While the workflows shipped with IdentityIQ provide many configuration options, many implementations will also include custom workflows.

### Quicklinks

Some implementations add their own Quicklinks that can trigger a custom workflow to meet business-specific needs.

### Custom Connectors

While SailPoint provides over 100 connectors, you may have specialized systems or home-grown applications that require a custom connector.

### More on extended attributes

Extended attributes are essential for a robust IdentityIQ implementation. These attributes are _your_ organization’s important data – data that allows you to run your identity and access management program. These often include job titles, locations, and department names. Extended attributes add _implementation-specific_ information to IdentityIQ objects.

Extended attributes drive IdentityIQ functionality and automated processes. Extended attributes can also be critical to provisioning processes; they can be examined when checking for policy violations and more.

- Standard attributes: The standard attributes are automatically included for each identity cube

- Extended attributes: Extended attributes are specific to each implementation (department, location, ID, job title etc)

When extended attributes are added to the system, the implementer can choose to designate them as **searchable**. Those that are searchable are automatically added to options throughout IdentityIQ.

### Other objects to extend

There are six objects to which extended attributes can added. In addition to identity cubes, there include:

- Entitlements
- Roles
- Applications
- Accounts
- Certifications

## IdentityIQ Plugins

A **plugin** is a software component that adds functionality to an existing program. You can use them to extend IdentityIQ functionality.

Plugins can be downloaded from Compass, and many SailPoint partners also provide IdentityIQ plugins. Examples include:

- A support plugin developed by SailPoint helps collect data from your IdentityIQ instance and provides it to the SailPoint support team. The plugin collects the required data into one zip file for uploading.

- The SQL Browser Tool provides administrators with view-only access to the IdentityIQ database to help implement and support IdentityIQ.
