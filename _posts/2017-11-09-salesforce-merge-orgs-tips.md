---
title: "What I learned from merging SFDC Orgs"
date: 2017-11-09
categories: 
  - "admin-life"
---

I recently took on a project to merge a foreign separate instance of Salesforce into our main instance of Salesforce. The timeline was extremely tight and short, with very little wiggle room - I am talking about 4 weeks from when the instance would be shutting down for good.

The first step of getting our heads around this project was coming up with a project plan. I used Confluence to create a page that contained all the different sections with checklists of all the pieces of information we would need to collect. I must say, we got super lucky in this case. Despite the instance being in a foreign non-latin based language, their org structure was super simple, which made the collection of information much easier. (If you were wondering, they were in Professional with no API access so you can imagine the lack of things you would need to worry about in that case).

Here is the list of items I found to be important to collect:

- Full Metadata copy - if you don't have API access, getting this could be very difficult
- Full data backup - you will probably need to do this a few times, or at least once for testing and once for production
- Full list of all users, their roles, and profiles
- A comparison of fields and objects to create a list of items that need to be recreated, as well as, any new page layouts
    - Don't forget translations!
- Sharing settings
- Reports, Dashboards, etc.
- Workflow rules, validation rules, email templates
    - Quick note here about something I didn't catch until the testing phase - do not forget to look at the default case settings. There might be default templates that do not match the destination org and therefore you will need workflow rules and page layouts that help account for this difference
- Assignment rules
- Web2Lead and Web2Case
- In the case, the merging org has API access, make sure to check out all integration points, buttons, links, and any APEX
- 3rd party installed packages

Once we had the plan together and a checklist to keep me somewhat sane, we began the task of going through it all. Working with both our internal teams and the team abroad, we collected the answers, which took about a week. During this time, I was also prepping all of the foundational groundwork in a dev environment. This included creating the new fields, setting up the new roles, creating new page layouts, etc. Our plan was to give ourselves a week+ to get it all together and replicated in our full sandbox, leaving us with about 4 days to have users test and then roll out to production. This gave us an extra week in case something went horribly wrong.

While all intentions are a best-laid plan... or however that saying goes, our plans for testing the merged changes did not quite go as hoped. We had difficulty getting users correctly set up in time for the testing as we didn't have the correct emails for everyone and therefore only about 75% of the items got tested before we went live. Luckily, we knew nothing could break in any catastrophic way (no APEX thank goodness) so we continued on as planned regardless of testing not getting to 100%.

Quick comment on getting the users from the old org to the new one - this was the most difficult step in the entire process. Between 2 different email domains and some of the users already existing in the destination org, it became a tangle of excel sheets and reports working to get it all lined up correctly.

Once testing was done, we needed to push first the foundational work into production and then the data. Given I had already moved all of this once from dev to full, this part was a walk in the park. The data piece took about 2 days to do (and that's for a relatively small amount of data) - we did need to turn off validation rules, workflow rules, and triggers in order to easily get the data in there.

The last step in this process was the post-deployment step. This has been one of the more lengthy pieces of the process. As with any big project, there is always a bit of cleanup and polishing to do at the end and this merge left us with several days of that. I think, honestly, that no amount of additional testing or pre-work could have been done to avoid it. So, if you are going through this process, don't beat yourself up about it; just plan the time in advance to take care of it. The cleanup mostly encompassed sharing rule fixes, role hierarchy changes, and dashboard and report updates.

My 20/20 hindsight takeaways of this whole project are:

- Try to give yourself plenty of time from start to finish so it does not feel rushed
- Get users into the testing environment long before you are actually ready for them to test
- Have a clear understanding of the processes being currently used, as this will help understand what really needs to be ported over
- Keep even better documentation
- Remember to have fun!
