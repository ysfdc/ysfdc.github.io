---
title: "Considerations for Privacy and OWD"
date: 2021-07-27
categories: 
  - "admin-life"
---

When you are starting in Salesforce, one of the first and most important things you will come across is organization wide defaults / org wide settings. These are the settings that define who can see the data inputted in your Salesforce org. There are many levels/layers of privacy and settings to get to a final setting of who sees what - I believe Salesforce has done an excellent of detailing out what each of these here:

Documentation: https://help.salesforce.com/articleView?id=security\_data\_access.htm&type=0

Video Series: https://admin.salesforce.com/blog/2017/data-visibility-made-easy-updated-video-series

Instead of walking through what is already well documented, I will walk through some of the pitfalls I see and the recommendations around them.

1. A user can see an Opportunity that they should not be able to - ensure that you always start with the org-wide settings to private, and then open the rules up through Sharing Rules. Sharing Rules should be constructed in the same manner, only open up as far as you want them to be - if you give to all internal users but then have a group that shouldn't see it, the rule has given too much access.
2. A user needs to be able to see a specific Opportunity or Case, and just this one that falls outside the rules - in this scenario, use the Sharing teams - while not yet great in Lightning, manual sharing is still a very valuable resource to use in these kinds of situations.
3. A collection of users see all of the Accounts in Salesforce - check the Profile and Permission sets assigned to these people. Were they given View All or Modify at the Record Level? Were they given View All or Modify at the System Level? These sorts of permissions should be well guarded and only given out to a select few. From a profile perspective, limit this to the System Administrative profile, and then create separate permission sets specifically for granting View all/modify all, so you have granular control over who gets these permissions. Especially in larger organizations where there may be entities that reside outside of the US, it is essential to ensure you comply with the relevant laws and only allow folks to see what they should see.
4. An external user is supposed to have access to cases their Account is related to - this is a good scenario for Sharing sets to open up the visibility for the external users.
5. A manager is supposed to see their subordinates Opportunities - two potentially different issues here; one - make sure that you are using grant access using hierarchies. Two - and important, start and maintain a clear role hierarchy. I have seen many a company fall to not keeping the Role Hierarchy in Salesforce aligned with what it is in the actual organization. This can be important not just for sharing records up in the chain but also for the route of approvals, which will help significantly. Role Hierarchies do not need to be complex; however the more granular you are, the more flexibility you will have when creating things like Sharing Rules.
