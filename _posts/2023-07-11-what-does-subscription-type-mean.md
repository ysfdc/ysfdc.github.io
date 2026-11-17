---
title: "What does Subscription Type really mean?"
date: 2023-07-11
categories: 
  - "cpq"
---

Recently I have been explaining to users the foundations of Subscription Type and the implications on a product. The question is typically around how you setup a one-time product, which truly is a loaded question as it requires understanding the value of proration before you can move forward.

Before we jump into the field, a definition of Prorate is required. When a product prorates, it means that its net dollar value will change based on the length of time it is set to.

Let's take the most basic example where the Subscription Term of the Product is 12, and the unit price is $100.

| Product | Subscription Term (Quote) | Unit Price | Net Total |
| --- | --- | --- | --- |
| Product A | 12 | $100 | $100 |
| Product A | 6 | $100 | $50 |
| Product A | 24 | $100 | $200 |

As you can see by the above example, proration means that the value of the Net Total changes as a result of the Subscription Term on the Quote. (\*reminder that this is a very simple example; this can be complex, _but we are not going to cover that here)._

Alright, now on to the Subscription Type field on Product. The field has three options - definitions below:

**Renewable**: This means that the product will prorate and will show up as a Subscription or Contract Line Item on the Contract or Service Contract, respectively. When the Renewal Quote is generated, the Product will show as a Quote Line on the Renewal Quote.

**One-Time**: This means that the product WILL prorate and will show up on the Contract as well; however, they will NOT show up on the Renewal Quote.

**Blank**: If this field is left blank, the product WILL NOT prorate. This is important if you want to have a product that, no matter how much time is on the Quote, the value of the product will not change.

While not covered here, if you are going the route of setting up Subscriptions, make sure you understand Subscription Pricing and MDQ as well.
