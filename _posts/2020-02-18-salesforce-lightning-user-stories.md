---
title: "Moving to Lightning with User Stories"
date: 2020-02-18
categories: 
  - "lightning"
  - "tips-tricks"
---

I think by this point it is safe to say that everyone is either in the process of actually [moving to Lightning](http://sf9to5.wordpress.com/2019/08/26/salesforce-lightning-guide/) or you are in the planning stages of moving to Lightning. If you aren't in either category, get on board quick! as Salesforce is not making any more adjustments to Classic, so if you want the newest and greatest that Salesforce has to offer, you need to be in Lightning.

With that being said, one of the key elements to a strong transition from Classic to Lightning is understanding your users and what they do day-in and day-out in Salesforce. Compiling a list of things that your users do and even perhaps, what they wish they could do, can you help plan and construct the UX of your Lightning implementation. In case you are wondering what I mean by UX here, think about the Lightning record pages and all of the customization Salesforce has now put into our hands - you don't want to just flip the switch as you are likely to lose out on some of the benefits and you may also cause your users to be frustrated if the system is now running slower than before.

The best way to capture the list I am referring to is to capture the user stories of ALL of the different users that in your Salesforce org. I highlight all, because you may focus most of your time making adjustments for a particular group, but moving to Lightning impacts every single person who uses Salesforce. For example, you have pre-sales, renewals, customer support, finance, marketing and more!

To capture user stories is relatively simple, although potentially time-consuming depending on how many groups of users you have. Schedule time to sit down with one to two people per group (you want to get the generic outline, you will have always have people with the edge cases, this isn't for that). During that session, have them walk you through what they do every day in the system.

Try not to coach them in what they are supposed to be doing (this isn't a training session), but do prod them if you feel they aren't giving you the whole story. For example, the user says "I do this, this and that", respond back by asking them to directly show you in Salesforce, as you will see there are additional steps that they take. Also, ask them "is that all you do?" you are likely to get responses, like "no sometimes I have to do this other thing", so whatever that other thing is to make sure they show you that too. As they do the demonstration take note of the buttons, links, tabs, etc that they click on.

Also, pay attention to the data that the user focuses on. These two items can help you ensure that a) the elements the user needs to use will work in Lightning and b) that you have the system set up in the most efficient way for the user to complete their job. One last trick is to record the sessions you do with a screen capture of the user's screen so you have the recording to refer back to later.

Below is an example of how a Business Analyst would use a user story for Pre-Sales (related items are color-coded):

| **User Story** | **Business Analyst Process** | **UX Implementation** |
| --- | --- | --- |
| **Click on the Leads tab**  **Select My List View**  **Click on Import to a Sales Engagement Product (3rd party button)**  **Update a couple of fields**  **Update the status** | **Annotate the steps and clicks the user takes**  **Talk with the vendor of the Sales Engagement Product to understand how to update for Lightning**       | **Use Pinned Related List (keeps their personal list view as the automatic view)**  **Create a VF button (the Import button is a JavaScript with URL – not supported) and add it to the list view page layout**  **Include Path on the Lead record and included the key fields in the Guidance section** |

The process noted above was repeated for every user group.

Once you have captured all of the user stories, you can work with your team to determine what elements need to change or be moved around, and what processes can be added in Lightning to enable your users to be the most efficient that they can be.

**Related: [Salesforce Lightning Reference Guide](http://sf9to5.wordpress.com/2019/08/26/salesforce-lightning-guide/)**
