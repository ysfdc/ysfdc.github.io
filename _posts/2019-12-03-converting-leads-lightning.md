---
title: "Converting Leads in Lightning"
date: 2019-12-03
categories: 
  - "lightning"
  - "tips-tricks"
---

During the [transition process to Lightning](http://sf9to5.wordpress.com/2019/08/26/salesforce-lightning-guide/), one of the big user experience changes you may see is the difference in how the Convert button on a Lead works. The differences are completely beneficial to your users but may take some adjusting to the visual elements of it.

Let's step through the Convert screen in Lightning:

The first time you are converting a Lead that has no matching Account or Contact, this is the screen you will be presented with:

![2019-10-05\_12-02-12](/images/2019-10-05_12-02-12.png)

As you can see in the above image you have the ability to create all-new records for all three objects. In each row you also have a drop-down to make small adjustments, i.e. make changes to the Account Name.

You also have the ability to set the Converted Status for the Lead.

After you click Convert you will get a screen with links to all of the newly created records:

![2019-11-11\_19-21-33](/images/2019-11-11_19-21-33.png)

If you are converting a Lead that has a matching Account and/or Contact and/or Opportunity than these are options you will be presented with:

![2019-10-05\_12-03-032](/images/2019-10-05_12-03-032.png)

In each level where there is a matching record, you will see what Salesforce believes is the closet match.

Account: ![2019-10-05\_12-03-342](/images/2019-10-05_12-03-342.png)

Contact: Here you are also provided the ability to update the Lead Source to be based on this newly converted Lead![2019-10-05\_12-03-46](/images/2019-10-05_12-03-46.png)

Opportunity: ![2019-10-05\_12-04-012](/images/2019-10-05_12-04-012.png)

As you will note for all three options you always have the ability to search, which is a great added functionality.

Finally at the end when you click Convert, you will be given links to the records, whether new or existing:

![2019-10-05\_12-04-162](/images/2019-10-05_12-04-162.png)

As an added benefit of the Lightning conversion process, if you have turned on the Multiple Accounts to Single Contact functionality, you will also have the ability to select a Contact that belongs to one Account, but Convert to a different account and this will create the relationship.
