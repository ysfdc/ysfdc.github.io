---
title: "Winter '21 Changes for CPQ Licensing"
date: 2020-09-08
categories: 
  - "admin-life"
  - "cpq"
---

As part of the Winter '21 release anyone who has Salesforce CPQ or Advanced Approval packages will be required to make updates to their system. This includes licenses, permission sets, and profiles. The information you will see below is based on the CPQ package, but the same logic pertains for the Advanced Approvals package.

**NOT COMPLYING WITH THESE CHANGES WILL RESULT IN THE CPQ ORG NOT BEING UPDATED!**

You may have seen the banner below on the top of your Quote Line Editor in recent weeks, this a warning message about completing the steps noted in this article.

<img src="/images/image-3.png" alt="">

To understand what changes you need to make in your system, go to Setup --> Installed Packages --> CPQ --> Configure --> Additional Settings tab.

<img src="/images/image-4.png" alt="">

At the bottom you will see a message that looks like the above image. The first step in this process is to run the tool to determine who needs a Permission Set License. Read more about [**Permission Set License vs. Managed License**](https://sf9to5.wordpress.com/2020/09/02/difference-between-managed-license-permission-set-license/).

The tool will help you learn the number of users per each of the following categories:

CPQ Managed Package Licenses Provisioned: #x  
CPQ Managed Package Licenses Assigned: #x  
Users with CPQ Permission Sets Assigned: #x  
CPQ Permission Set Licenses Provisioned: #x  
CPQ Permission Set Licenses Assigned: #x

You will need to clear any users that are inactive from the Permission Sets Licenses, as having an inactive user assigned to it will break the License. You will also need to ensure all users have a Permission Set and Permission Set License for CPQ.

As noted by Salesforce on the [Help page](https://help.salesforce.com/articleView?id=000351486&language=en_US&type=1&mode=1):

> "**Custom permission sets may contain access to CPQ objects that could be flagged by the Readiness Tool as needing provisioning.  Users whose assigned custom permission sets contain this access will require a CPQ license and CPQ PSL.**"

Once everyone is properly assigned the Permission Set License, you should then review your Profile level access. Going forward you cannot use Profiles to grant CPQ object permissions. Please ensure to read this document from Salesforce outlining the changes that are mandatory to avoid error messages : [Best Practices for CPQ Winter '21 Profiles and Permission Sets](https://help.salesforce.com/articleView?id=000354205&type=1&mode=1)

Again, this process is extremely important to follow and complete prior to the Winter '21 release. To learn when your org will be transitioned visit [status.salesforce.com](https://status.salesforce.com/).
