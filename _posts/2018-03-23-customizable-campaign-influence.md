---
title: "Tips for Customizable Campaign Influence"
date: 2018-03-23
categories: 
  - "tips-tricks"
---

If you are looking to expand your attribution model within Salesforce and already utilizing campaigns and campaign influence, then you may be interested in upgrading to customizable campaign influence. There are [two big benefits](https://help.salesforce.com/articleView?id=campaigns_influence_whats_the_diff.htm&type=5) that come from the upgrade: 1 - you have access to campaign influence through the API and 2 - you can actually set the weight of different types of campaigns.

When going to set up customizable campaign influence there are a couple tricks for getting the data to show up in a way that you expected. First and foremost is the [CRM User Permission set](https://help.salesforce.com/articleView?id=users_permissionset_licenses_assign.htm&type=5). Even if you are the admin and a marketing user, you will still need to add this permission to your user, as you otherwise not be able to see the Opportunities related list on Campaigns, or the Campaigns related list on Opportunites - both of which are important for your sales users to understand which campaigns are contributing to the Opportunity and for your marketing users to understand the ROI of their campaigns.

After you have added the permission set to your user, the related lists will not automatically be added to the view, you will need to go in and manually add them. One thing to keep in mind is that if you were previously using Campaign Influence 1.0, the Add to Campaign button on the related list of Opportunities goes away.

If you are planning on going down this route, make sure you have read through the [considerations from Salesforce](https://help.salesforce.com/articleView?id=campaigns_influence_customizable_supplemental.htm&type=5) about making the switch. In addition, make sure you are working closely with your marketing team and stakeholders as while this looks like a simple flip of a switch, even staying on the Primary Campaign only, it has some nuances that should be discussed first.
