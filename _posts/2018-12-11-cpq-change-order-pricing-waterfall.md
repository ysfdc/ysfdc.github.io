---
title: "CPQ: How to Change the Order of the Pricing Waterfall"
date: 2018-12-11
categories: 
  - "cpq"
  - "tips-tricks"
---

Recently, I learned that the pricing waterfall for CPQ, which is known to be a set structure of when discounts are applied, can, in fact, be modified. Kept in the list of [CPQ special fields](https://help.salesforce.com/articleView?id=000270984&language=en_US&type=1), which are fields that do not come with CPQ out of the box, but can be created manually and CPQ will know what do with them, are several fields that will allow you to reorder the pricing waterfall.

To use special fields in CPQ, the trick is to make both the label and the API name match exactly to what is listed in the Salesforce instructions. Once you make these fields and set them accordingly, they work without any further build.

The first of these fields for updating the Price Waterfall is ApplyAdditionalDiscountLast. This changes the order of the waterfall to allow that the additional discounts, which are typically manually entered by reps to be applied as the last and final discount on the price. As noted by [Salesforce](https://help.salesforce.com/articleView?id=000271124&language=en_US&type=1), the new order would be:

List Unit Price -> Regular Unit Price -> Partner Unit Price -> Net Unit Price -> Customer Unit Price

Next up for making adjustments to the waterfall order is ApplyPartnerDiscountFirst. This changes the order of the waterfall to allow for the partner pricing discount to occur before any other discounts. This can be useful if you want to give your partners a discount before applying additional manual discounts. Again, as noted by [Salesforce](https://help.salesforce.com/articleView?id=000271078&language=en_US&type=1), the new order would be:

List Unit Price-> Partner Unit Price -> Regular Unit Price -> Customer Unit Price ->Net Unit Price

Lastly, for changing the Pricing Waterfall is ChannelDiscountsOffList. This doesn't so much change the order as much as change which value the partner and distributor discounts are taken from. Instead of taking those discounts off the Customer Unit Price or the Regular Unit Price, those discounts will be taken off the List price. However, the subtraction order will remain as it was. The article from Salesforce ([see here](https://help.salesforce.com/articleView?id=000270686&language=en_US&type=1)) also provides additional information on how this one impacts Renewals and Amendments. The one asterisk I would make that Salesforce also makes is that doing this prevents discounts from being applied on Amendments.

**Studying for the CPQ Specialist Exam? Check out SF9to5's** **[Study Guide](http://sf9to5.wordpress.com/2017/09/12/salesforce-cpq-exam-study-guide/)** **and** **[Practice Exam](http://sf9to5.wordpress.com/cpq-practice-questions/)**
