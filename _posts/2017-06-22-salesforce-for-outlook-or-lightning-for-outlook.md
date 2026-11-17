---
title: "Salesforce for Outlook or Lightning for Outlook, that is the question."
date: 2017-06-22
categories: 
  - "admin-life"
---

I know that this post may be a little late to the game since [Lightning for Outlook](https://www.salesforce.com/blog/2016/06/introducing-lightning-for-outlook.html) came out back last summer (Summer '16) but I think it an important topic that could relieve many of the stresses I find people have with Salesforce for Outlook.

First, let me address the question I know you have, Lightning for Outlook DOES work with Salesforce Classic and of course, Lightning.

I find that there are many benefits to point out with the Lightning for Outlook. The first being the fact that is it not an application that you have to download onto your desktop, which is a good thing as I have seen those downloads cause quite a bit of trouble. Lightning for Outlook is an add-in for Office 365.

Lightning for Outlook is an add-in for Office 365. Your IT team can set it up in such a way that users don't even need to download or install it themselves, they can just see it appear, like magic! Another lovely feature is that it can work on both Mac and Windows, a serious downfall for the Salesforce for Outlook app is that it is only for Windows.

Next on my list is something that may not be for all users, but if it is could be quite impactful. As of July 22nd, Salesforce will not longer support TLS 1.0 and today when I ran a login history report I saw that anyone that was logging in via Salesforce for Outlook was going over TLS 1.0 - not good! Confirming via the documentation and found that anyone still running the v2.9.3 after Jully 22nd will run into issues as TLS 1.0 will no longer be supported and therefore this version will no longer be supported. To learn more [click here](https://releasenotes.docs.salesforce.com/en-us/summer17/release-notes/rn_sales_sfo_crit_upgrade.htm). You will not have the same issues with Lightning for Outlook as there are [no manual updates](https://releasenotes.docs.salesforce.com/en-us/summer17/release-notes/rn_sales_sfo_migrate.htm) to maintain, Salesforce does the work for you.

Lastly, is the design, oh such a lovely design upgrade. Lightning for Outlook, as expected looks like Lightning and has the grace of the UI of it.

\[caption id="" align="aligncenter" width="512"\]<img src="/images/panelinfo1updated525v2.png" alt=""> \*https://store.office.com/en-us/app.aspx?assetid=WA104379334&ui=en-US&rs=en-US&ad=US&appredirect=false\[/caption\]

Whereas Salesforce for Outlook has its own more outdated design:

\[caption id="" align="aligncenter" width="531"\]<img src="/images/sfo_side_panel.png" alt=""> \*https://help.salesforce.com/articleView?id=outlookcrm\_side\_panel\_about.htm&type=0&language=en\_US\[/caption\]

 

If you haven't figured my decision from above then I will note it shall be Lightning for Outlook. It looks lovely and it works smoothly like a mini-Salesforce at your Outlook fingertips.

 

P.S. for those of you who may have had issues with the lack of being able to attach to a record when composing like you could in Salesforce for Outlook, that has been resolved the [Summer '17 release](https://releasenotes.docs.salesforce.com/en-us/summer17/release-notes/rn_sales_lightning_for_o_relate_flexibility.htm).

For additional FAQ information please check out the [Office 365 blog](https://blogs.office.com/2016/06/28/sell-smarter-and-faster-with-the-new-salesforce-lightning-for-outlook-add-in/) and the [Salesforce Documentation](https://help.salesforce.com/articleView?id=app_for_outlook_overview.htm&type=0).
