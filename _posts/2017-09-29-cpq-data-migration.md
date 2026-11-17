---
title: "CPQ Data Migration"
date: 2017-09-29
categories: 
  - "cpq"
---

One of the most challenging issues with Salesforce's CPQ structure is that the majority of the setup is actually data instead of metadata. This results in not being able to use change sets to move the information across instances. Also, it can produce testing problems as it is hard to replicate all of the data in a developer instance.

When going through the implementation process of CPQ, the concept of migrating data should be taken into consideration. The best practice for mitigating potential duplicates in updates/uploads is to put External IDs in place on all commonly migrated objects. At the bare minimum, this list should include:

- Products
- Product Features
- Product Options
- Configuration Attributes
- Price Book Entries (not to be confused with Price Books which should be created manually)
- Option Constraints
- Any custom lookup object created for CPQ

The benefit of having the External ID on all of these objects is that when you go to load a file you are able to use the Upsert function instead of the Insert/Update function. This prevents duplicates from entering into the system as Upsert will update any existing record (known by the External ID) and will create any missing records when the External ID is not found.

If you use External IDs, it is critical that they are maintained over time and do not change without conscious awareness, as this could cause duplicates and possibly other downstream issues with Product and Price rules.

When pushing the data from one instance to the next (most likely following the pattern of [Developer Pro -> Full Sandbox -> Production](http://sf9to5.wordpress.com/2017/07/18/release-management-for-salesforce-admin/)), I highly recommend that you keep your "changesets" small and keep them well organized in a folder system. I find that using [Enabler4Excel](http://sf9to5.wordpress.com/2017/04/06/review-enabler4excel/) allows for easier trackability than Dataloader as you can maintain everything in one sheet. This is particularly helpful if there is an error and only a certain number of rows need to be re-upserted (you can do this using the Upsert Selected option).

When doing the uploads of the data, order really does matter as you will essentially be building one piece from the previously uploaded piece. At a high level, the order should be something similar to:

1. Products
2. Standard Price Book Entries
3. Custom Price Book Entries
4. Product Features
5. Product Options
6. Configuration Attributes

If you intend on loading Product rules and Price rules, which I don't really recommend due to the complexity that they can take on and the number of related records involved, these would need to follow after the above have been created. You can reference a [post on Steelbrick's community](https://community.steelbrick.com/kemxp52623/attachments/kemxp52623/SteelBrickCPQ/425/1/SteelBrick%20CPQ%20-%20Migration%20Plan%20\(5\)-1.txt) for a fuller list of objects and their order.

If you are not using CPQ as your Product Master and are loading the data from another system, it is important to always review the fields within the file for uploading or you may end up with incorrect or accidental duplicated data.

Finally, always make sure to TEST TEST TEST and document each upload that you do. You'll be very thankful for it later.
