---
title: "5 Practice Problems for APEX Triggers"
date: 2018-04-19
categories: 
  - "admin-life"
  - "development"
---

As part of my journey from a "Point and Click Admin" to a "Dev Admin", I wanted to be able to get more hands-on challenges for triggers than what Trailhead provides. Fortunately for me, I have some very good resources available to me and from such was able to get five different APEX trigger scenarios that are good for any beginner. They are designed to be able to test your ability in understanding how triggers work.

**[Click Here to purchase the complete Practice Problem set with Solutions!](https://www.e-junkie.com/i/yrvp?card)**

For someone who is more advanced and reading this, please keep in mind that this is merely for the purpose of learning. I would not otherwise advise putting multiple triggers on the same object, with all of the logic living in those triggers. Please see the [Salesforce APEX best practices](https://developer.salesforce.com/page/Apex_Code_Best_Practices) for more information.

### Problem 1:

#### Pre-Reqs:

Create a field on Account called "Only\_Default\_Contact", checkbox, default off

#### Assignment:

When a new Account is created, create a new Contact that has the following data points:

- First Name = "Info"
- Last Name = "Default"
- Email = "info@websitedomain.tld"
- Only\_Default\_Contact = TRUE

When the Account has more than 1 Contact, update Only\_Default\_Contact to FALSE.

### Problem 2:

#### Pre-Reqs:

Create a field on Account called "Out\_of\_Zip", checkbox, default off

#### Assignment:

When a Billing Address is modified, get the new Postal Code. Then check which Contacts on the Account are outside that Postal Code. If 1 or more Contacts are outside of the Postal Code, mark Out\_of\_Zip as TRUE.

### Problem 3:

#### Pre-Reqs:

Create a field on Contact called Profile, text, 255

#### Assignment:

When an Account is updated and the Website is filled in, update all the Profile field on all Contacts to:

- Profile = Website + '/' + First Letter of First Name + Last Name

### Problem 4:

#### Pre-Reqs:

Create a field on Account called "is\_gold", checkbox, default off

#### Assignment:

When an Opportunity is greater than $20k, mark is\_gold to TRUE

### Problem 5:

#### Pre-Reqs:

Create a field on Account called "need\_intel", checkbox, default off

Create a field on Contact called "Dead", checkbox, default off

#### Assignment:

If 70% or more of the Contacts on an Account are Dead, mark the need\_intel field to TRUE

Hope these questions help you practice as much as they helped me!

**[Click Here to purchase the complete Practice Problem set with Solutions!](https://www.e-junkie.com/i/yrvp?card)**
