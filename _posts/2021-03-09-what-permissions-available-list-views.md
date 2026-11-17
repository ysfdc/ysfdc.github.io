---
title: "What Permissions are available for List Views?"
date: 2021-03-09
categories: 
  - "admin-life"
  - "tips-tricks"
---

First, let's start off with what a List View is - this is a list for any given object that can be accessed via the tab for that object. List Views are like reports in that you can change the columns, add filters, and even show charts. They are unlike reports though in two keys ways, one, List Views are limited to the fields on the object; two, List Views can be used to edit fields directly in the list without ever leaving the page. The latter feature is amazing when you are always trying to review a list of records and make quick modifications to them.

<img src="/images/image-1.png" alt="">

To control users' permissions on List Views, there are a few system based permissions that can be given either through [Permission Sets](https://sf9to5.wordpress.com/2019/03/19/salesforce-profile-auditing-guide-1/) or through the Profile level. There are also a couple of overall User Interface settings to look at.

### **Permissions in Profiles/Permission Sets**

**Create and Customize List Views** - This permission gives users the ability to create their own List Views and to customize their own List Views. It does not however allow a user to share their custom List Views with others.

**Manage Public List Views** - This permission gives the user the ability to share and edit any public List View regardless of the object. Be careful giving this one out.

### **Permissions in the User Interface**

<img src="/images/image.png" alt="">

**Enable Inline Editing** - This gives all users the ability to edit a field in a List View. This is dependent on that they can see the records and fields. There are also some considerations to keep in mind, so see the note at the bottom.

**Enable Enhanced Lists** - This gives users the ability to create a record from the List View, as well as, edit multiple records at once.

Some considerations from Salesforce regarding inline editing in a List View do include, objects that have multiple record types, need to have a single record type filter to be editable. There are also a series of fields and field types that are blocked. See [here](https://help.salesforce.com/articleView?id=sf.customviews_edit_inline_listview_lex_considerations.htm&type=5) for more information.
