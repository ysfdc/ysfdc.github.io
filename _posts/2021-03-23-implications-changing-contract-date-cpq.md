---
title: "The Implications of Changing the Contract Date in CPQ"
date: 2021-03-23
categories: 
  - "billing"
  - "cpq"
---

Recently I was asked whether or not the Contract Date on a non-activated Contract could be changed- specifically the Contract Start Date field. I had been extremely hesitant to say Yes to this change because, in the world of CPQ, dates mean everything, and the Contract Start Date has a lot of power and meaning. However, through some due diligence, I learned that it is possible to change the Contract Start Date, but it has some interesting results and implications.

The field here that will drive how your amendments and renewals will behave due to this change will be the 'Amendment and Renewal Behavior' field on the Contract. This field's options are to set the Renewal dates to either the Latest Date or the Earliest Date. More information can be found [here](https://help.salesforce.com/articleView?id=cpq_renew_subs_mult_end_dates.htm&type=5).

Results:

1. Changing the Start Date on the Contract level will push out the Contract Start Date by an equal amount of time
2. The Subscription Term on the Start Date is not impacted, therefore theoretically the dollars should not have been harmed (no strange proration should occur)
3. The Start Date for either the Subscription records or Contract Line Items (depending on if you are using Sales or Service) will not be adjusted by this change
4. The End Date for either Subscription records or Contract Line Items will be updated to match the contract

Implications: Since the Subscription records only adjust the end dates, when you generate a Renewal Quote, the change in the Contract Start Date will only impact the Quote level Start Date, it will not affect the Quote Line dates - this means that if you have users who are setting Quote Line level details, you will need to be cautious when changing the Contract Start Date, and review the Renewal Quote for accuracy.
