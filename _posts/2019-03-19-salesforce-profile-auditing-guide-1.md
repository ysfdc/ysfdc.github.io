---
title: "The Ultimate Profile Auditing Guide - Intro"
date: 2019-03-19
categories: 
  - "admin-life"
---

_The guide to help you audit your profiles, fields, permission sets, and more._

Over the next couple of months, I will be writing a series of posts about auditing profiles in Salesforce. I will write about the Why, the What, and the How, including some tips and tricks for using Excel to work with the data.

The intended audience for this guide is designed to be as widespread as a comptroller or business stakeholder in charge of IT policy and security, to the director of Sales Operations or for a Salesforce System Administrator responsible for managing and complying with all security and compliance protocols.

This guide is designed to help you quickly and efficiently navigate profiles and permissions that are granted to your Salesforce users and to help maintain and comply with your internal business needs.

In this first post, I will be walking through definitions that are necessary to understand from Salesforce perspective. The subsequent posts will be a series of instructions, tools, and tips for enabling you to comply or audit your Salesforce org and permissions therein easily.

**Definitions of permissions**

Permissions come in a few different formats in Salesforce and can be confusing on the onset without an understanding of which permissions control what, and which permissions take precedence over the other.

To start, you have organization-wide settings which determine the overall sharing structure of the record data. Going forward the term record indicates the Sharing Setting controls the actual record itself, i.e., an account record for company ABC and who has visibility to it. How your sharing settings are structured will determine which users can see which records. Org-wide settings are therefore your first level of security and take the first precedence over the next two items.

Next, you have profiles. Profiles are a requirement for every user in Salesforce. Profiles grant access to types of records and what they can do to a record, including Read, Edit, Create, or Delete otherwise known as CRUD. Profiles also control what visual force pages, apex classes, and all user, system, and app permissions - the definition of these will be described later.

Following profiles, you have permission sets. These are used to grant additional permissions to a specific user over and above profiles. They cannot take away permissions. Keep reading to learn more about the difference between a profile and a permission set.

**What is a Profile vs. a Permission Set**

While looking at a profile and permission set may appear very similar they perform two very different jobs. Every user is required to have a profile. That profile should contain the bare minimum requirements for the users who will use that profile.

Permission sets, on the other hand, are designed to provide additional permissions to a single user. Let me repeat that in another way, profiles are used by a specific group of people. I.e., You may have a sales profile that goes to specific sales people. In that profile, you will have all the necessary permissions like read and create on accounts. You may then though have one or two folks who need to be able to modify a specific field or to be able to delete the records, and you will then use a permission set to control this.

**Field level security (FLS)**

Field level security is the read and write accessibility for a specific field. The user would first need sharing rights to the record, then read/edit rights to the object and then lastly you can decide how they can interact with the specific fields.

At the Profile level, you can control FLS through Read and Edit. These have no impact on the visibility of the field on the page layout. However, even if the field is not on the layout and the user does have at least Read permission, then they will be able to view the field in a report.

At the field level, you can control the visibility of the field. You can make it Visible and Read-Only. Visible without Read-Only is the same as granting them edit access at the Profile level.

The page layout also provides some additional FLS. Adding a field on a page layout is how you ensure a user can see it on the actual record as opposed to only in a report. Also, at the page layout level, you can make a field Read-Only, but that Read-Only functionality extends as far as the user being on the specific layout.

There are many configurations to keep in mind when you are determining field level access.

**What about System and App Permissions**

Beyond the most commonly thought about permissions of objects and fields are the permissions that control what actions a user can take, like converting a Lead. These permissions are housed in the System and App Permissions sections of both Profiles and Permissions sets. You will want to ensure that these are included in your auditing as critical aspects and accesses are included here, for example, Modify All data.

 

Stay tuned for future posts as part of this guide.
