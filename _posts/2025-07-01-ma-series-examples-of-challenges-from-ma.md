---
title: "M&amp;A Series: Examples of challenges"
date: 2025-07-01
categories: 
  - "cpq"
---

I thought it would be helpful to lay out some of the examples I have seen during my Salesforce career as to why I wanted to make the callout to ensure Salesforce and CPQ are evaluated as part of the due diligence process and not left to be something of an afterthought.

To avoid using company names, ACME will represent the acquiring company, and Universal Containers will be the company getting acquired. All of these represent different company combos.

**Example 1: Bad customer experience**

Universal Containers had done all the work to clean up their Salesforce org and the product they were tying into as their ERP. They had spent a couple of years doing a tech debt project and a complete revamp of the business processes and had them fully rolled out.

ACME, on the other hand, was in the opposite state. Depending on who you asked, they had different processes in place.

The decision had been to move everything UC had done into ACME but use ACME's processes. The challenge was that the process was no longer as clean because ACME was not as streamlined when the customer data was ported over. As such, when customers wanted updates, the reps could no longer provide the same level of support as they used to prior to the adjustment.

**Example 2: Using Salesforce as a Product UI**

This one is basically in the title. Universal Containers was using Salesforce as the UI for the product they owned. What this meant was that when ACME completed the acquisition, it became apparent that removing what would now be an extra Salesforce instance would be a challenging feat. In addition to being used as the UI, the UI itself was built by outside consultants; there was no documentation for it, and anyone connected with the original build was already long gone. One can imagine the headache for ACME once this came to light.

**Example 3: Integrated Billing**

This is probably a scenario I have seen as the most common one, Universal Containers has a product that has integrated it's billing into either Salesforce, the product, or both. While this can be fantastic in some cases, it will really hang on whether ACME wants to keep that structure and if it fits into their existing billing structure. In the cases I have seen, ACME got saddled with paying for different billing systems while they spent time unraveling the connection to move them into their existing ERP. Some of these projects can take months to years to complete, depending on how ingrained they are in the process and the impact level on customers. In one case, the customer had the ability to completely self-serve through the product, while on the one hand this was great for the product to run on its own, it was not an easy exercise to migrate this out of the product.
