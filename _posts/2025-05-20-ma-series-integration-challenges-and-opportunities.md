---
title: "M&amp;A Series: Integration Challenges and Opportunities"
date: 2025-05-20
categories: 
  - "cpq"
---

This article will start to discuss topics that might arise during acquisition, but considering them beforehand can still give you a leg up.

Let's start with overlapping functionalities between Salesforce systems. Things that would be important to look out for would be:

- Account hierarchy and structure - do the two systems manage accounts similarly? If not, how would you consider bringing over that data? How will the processes related to creating and managing accounts be merged?

- Opportunities and the sales process as a whole - The Opportunity object is one of the critical objects in the Salesforce ecosystem as it represents the deal sold. Typically, it also represents the bookings amount. As such, things to look for might be evaluating if the systems treat financial-related fields similarly or with the same definition? If they don't and you intend to migrate opportunities over, will you map the values to your current definition, or will you create new fields to track both versions simultaneously?

- Products - Assuming you bought the company for what it sells and not just the customers, understanding how you will sell the product via the system level will be a critical step in the evaluation process. I am not referring to the go-to-market strategy or product naming, but instead, based on your current catalog structure. I.e., price rules, product rules, and how the quote document is exported. All of these things will impact how you bring in the new product. Depending on the complexity on either side, this could require some significant setup.

Once you have addressed the different ways the team will operate within the new system and laid out any new workflows or approval processes, the next step is understanding the details of migrating the data.

Things to consider when migrating the data:

- Deduplication—You will want to ensure that any data that is brought over is not a duplicate of existing data. This can take some manual work, particularly if the two systems are not at parity in how they define objects or fields. However, if this is not taken into account, you run the risk of causing misinformation or delays to the customer, as it will make it more difficult for the rep to find the most accurate and up-to-date information.

- Historical data - For records that are not dupes but might contain historical information, you must consider how far back the data should go. Say you bought a company that has had Salesforce for 10 years, and do you want all 10 years' worth of accounts and opportunities? Or will you consider only bringing in live or active accounts and any in-flight opportunities, as well as existing booked records that are still being billed? Another element here to think about that can be a heavy data load is cases and contacts. From a contact perspective, if you have Marketing Cloud or Marketo, I would use their built-in options to do merges so you don't end up with an influx of dead contacts or contacts that may have opted out (GDPR and such). Cases have to be considered in the same way as Opportunities; how far back do you want the historical knowledge to be? Do you have a data warehouse where you could store all the historical data and let reps pull from that instead of the CRM if needed?

- Data governance is the last piece you need to consider here. Given that you may have defined new processes and that new people are joining the existing group, you will want to make sure that you have defined practices in place to ensure that the data stays clean and up to date.
