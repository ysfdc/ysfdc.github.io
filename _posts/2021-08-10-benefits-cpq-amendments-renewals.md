---
title: "Benefits of CPQ Amendments and Renewals"
date: 2021-08-10
categories: 
  - "cpq"
---

Many of the Salesforce instances I work with have employed CPQ Amendments and Renewals and are experiencing the benefits of features that Salesforce provides out of the box. To learn about how to use Amendments and Renewals, please check out these two posts:

1. [Opportunity Renewal Creation](https://sf9to5.wordpress.com/2018/12/18/opportunity-renewal-creation-cpq/)
2. [Amendments and Renewal Quotes](https://sf9to5.wordpress.com/2019/01/22/cpq-amendment-renewal-quotes/)

On the flip side, many have implemented CPQ but have chosen not to transition from their existing way of handling expansions and renewals. Thus, while there can be some upfront work to enabling Amendment and Renewals, there are many reasons and benefits to doing so.

My colleague Cami Gumucio and I compiled a list of the reasons to transition to using what Salesforce provides out of the box.

**Benefits of using CPQ Renewals** **& CPQ Amendment**

When an Opportunity is Closed-Won, and you have a Primary Quote with Subscription products, you can automatically set up a workflow to generate a Contract (assuming you are not using Orders before contracting).

After a Contract is created, CPQ can automatically generate both the Renewal Opportunity and the Renewal Quote - this can help when forecasting and ensures that the Renewal is not missed.

As part of the Renewals process, uplifts can be auto-applied to the Renewal Quote.

Using Amendments and Renewals ensures continuity across assets and subscriptions tied to the account.

Once you have started consistently using CPQ, including Renewals and Amendments, everything the customer has purchased will be on their account. As a result of this, Amendments can track purchases based on the Contract they are associated with.

Amending is available from both Active Contracts and an Opportunity that has been contracted and has an active contract.

When doing an Amendment, you can add net new lines for the customer. These new lines are appropriately prorated till the end of the Contract, so your users do not need to do any math. The net new lines are then added to the existing Contract rather than generating a new one.

Similarly, when in the Amendment flow, you can also remove products from the Contract, and Salesforce will do the math to determine how much money is owed back to the customer.

If your Contract contains subscriptions with different end dates, you can control how Salesforce CPQ sets the end date of the amendment quote and the renewal quote. This feature is helpful if you don’t want an amendment quote to co-terminate with the original Contract.

Amending and Renewing through the CPQ process enables MDQ quotes to process correctly and provides a more significant benefit to using MDQ, as it ensures that you can modify during the Contract and renew the right products for the right amount of time.

Any adjustments made to the Contract through the Amendment process will show up on the Renewal Quote as long as they were completed before it was generated.
