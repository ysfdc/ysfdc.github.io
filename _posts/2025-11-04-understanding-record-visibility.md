---
title: "Understanding Record Visibility"
date: 2025-11-04
categories: 
  - "admin-life"
  - "tips-tricks"
---

Understanding how Roles, Profiles, and Sharing Rules interact is crucial when controlling access to records in Salesforce. Each serves a different purpose, but they help ensure the right users see the correct data. Let’s explore the differences by walking through a simple scenario.

### Scenario: Managing Record Access for Sales Teams

Your organization has two teams: **Enterprise Sales** and **Small Business Sales**. You want to control who can view an opportunity record for a high-value client, "Big Tech Co."

Here’s how Roles, Profiles, and Sharing Rules work together to manage record access.

### Profiles: The Baseline of What Users Can Do

Profiles broadly define what users can do—permissions tied to objects, fields, tabs, and apps. They don’t determine _which_ records a user can access but control actions like viewing, editing, deleting, or creating records.

For this scenario:

- Both **Enterprise Sales** and **Small Business Sales** reps use the **Sales User** profile.

- The **Sales User** profile allows users to **view, edit, and create** Opportunities.

**Profiles** apply equally across the organization. At this stage, whether the opportunity belongs to Enterprise Sales or Small Business Sales doesn’t matter. Users with the Sales User profile will have the same object-level permissions.

### Roles: Who Sees What Records

While Profiles control what you can do, **Roles** determine what you _can see_ regarding record access. Roles create a hierarchy where users higher up in the role hierarchy automatically access records owned by users below them.

For this scenario:

- The **Enterprise Sales** team has its own role: **Enterprise Sales Rep**.

- The **Small Business Sales** team has the **Small Business Sales Rep** role.

- Above them, there’s a **Sales Manager** role who oversees both teams.

<img src="/images/image-1.png" alt="">

Let's say "Big Tech Co." is an opportunity owned by an Enterprise Sales rep.

- That rep’s peers in the **Enterprise Sales Rep** role can see the opportunity because they belong to the same team.

- The **Sales Manager** (above them in the role hierarchy) can also see the opportunity.

- Small Business Sales Reps are not in the same role hierarchy and cannot see the opportunity record, even though they share the same profile.

- This also assumes that the Role setup for opportunity access is set to the most strict version; otherwise, account access can also be involved.

<img src="/images/image.png" alt="">

In short, roles control access up the hierarchy but don't allow lateral access across different teams.

### Sharing Rules: Extending Access Beyond Roles

**Sharing Rules** are used when you extend record access to users outside the role hierarchy. They allow exceptions to be made without changing roles or profiles.

For example:

- You want **Small Business Sales Reps** to see opportunities owned by **Enterprise Sales Reps** when they work on high-value deals together.

- You can create a **Sharing Rule** that opens access to records owned by the **Enterprise Sales Rep** role and shares those opportunities with users in the **Small Business Sales Rep** role.

With this Sharing Rule, Small Business Sales Reps can now view "Big Tech Co." opportunities without changing their roles or profile permissions.

### How It All Fits Together:

- **Profiles** determine that both sales teams can view and edit opportunities.

- **Roles** ensure that Enterprise Sales can see their own records, while the Small Business team can’t see these records by default.

- **Sharing Rules** are applied to make an exception, giving visibility of certain records (like high-value opportunities) to users who wouldn’t usually have access.

This layered approach keeps your Salesforce org secure while allowing flexible collaboration between teams. By leveraging profiles, roles, and sharing rules, you can manage data access efficiently without overcomplicating permissions.

* * *

### How to Check What Access a User Has to a Record

Now that you've set up record access, how can you check what level of access a specific user has to "Big Tech Co."?

Salesforce makes this easy with the **"Sharing" button** and the **"View All" access tools**. Here’s how to use them:

1. **Enable the "Sharing" Button** (if it's not already visible):
    - Go to **Setup** > **Object Manager**.
    
    - Find and select **Opportunity** (or the object you’re working with).
    
    - Under **Page Layouts**, select the relevant layout and drag the **Sharing** button onto the page layout.

3. **View Sharing Hierarchy**:
    - Navigate to the specific **Opportunity record** (e.g., "Big Tech Co.").
    
    - Click the Sharing Hierarchy button (top-right).
    
    - This shows who can see that record and how, including which users have access via Roles, Profiles, Sharing Rules, or manual sharing.

<img src="/images/image-3.png" alt="">

This helps you quickly identify how access is granted and troubleshoot any permission issues in record visibility.

\*_written with the help of custom ChatGPT_
