---
title: "Lightning for Outlook, Lightning Sync, and Inbox, Oh my!"
date: 2018-10-23
categories: 
  - "admin-life"
---

So it may have crossed your mind recently that there seem to be a lot of Outlook/mail tools for Salesforce, and you have wondered what the heck the difference is.

Today I am going to give a super high-level breakdown of the differences and a couple of things to keep in mind.

## [Lightning for Outlook](http://sf9to5.wordpress.com/2017/07/05/quick-guide-lightning-outlook/)

First, let me know note that this IS the replacement for [Salesforce for Outlook](http://sf9to5.wordpress.com/2017/06/21/salesforce-for-outlook-or-lightning-for-outlook/), the old grandpa to Lightning for Outlook.

- Web-based application with no physical installs on the machine, which also means no manual updates (IT team - you should be happy about this)
- Associate to standard or custom objects with just a click (or maybe 2 if it has trouble finding the right record)
- Your reps DO NOT NEED TO LEAVE Outlook
- Sync Contacts and Events

Now you may be wondering why I crossed out that last line. While, technically the appexchange does boast about Lightning for Outlook having sync functionality, [Salesforce guides you not to use it](https://trailhead.salesforce.com/content/learn/modules/outlook_integration) and rather to use Lightning Sync.

### Lightning Sync

I think I pretty much covered this, you sync your contacts and events between Outlook and Salesforce. \*\*\*\*\* Please be careful with this. I have seen it go awry and people end up with duplicates in Salesforce, because they tried to delete something in Outlook.\*\*\*\*\*

## [Inbox](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N30000000rGckEAE)

This is the Salesforce magic email tool or so they will tell you. Most of the features to truly work require Lightning, so if you are still on Classic, be careful what you pay for.

- Logs email communication AUTOMATICALLY to Salesforce. Reps do not need to lift a finger.
- Einstein is plug and play here. It gives the rep all sorts of insights and helps out in scheduling and other Outlook related items.
- Your reps can create personalized messaging and templates
- As a note, if you pay for this product, as of [Winter '19](http://sf9to5.wordpress.com/2018/09/18/the-classic-side-of-winter-19-release/), it will no longer be a separate app, it will be part of Lightning for Outlook. But if you only have Lightning for Outlook, you do not benefit from Inbox.

Hope you found that helpful!
