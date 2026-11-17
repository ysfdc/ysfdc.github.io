---
title: "Should I use Orders in CPQ?"
date: 2022-10-12
categories: 
  - "billing"
  - "cpq"
---

The question in the title is one I have been asked on repeat over the last four years. The initial question is always at the object level, a wanting to understand which flavor they should pick:

Opportunity --> Quote --> Contract

Opportunity --> Quote --> Order --> Contract

While some might think the obvious answer is to go with fewer objects and, therefore, fewer data to maintain, this is not the case for most business cases, as the Order object provides a lot of additional flexibility that does not exist in the other flow.

Before I go any further, it is essential to note that if you are using Salesforce Billing, you do not have a choice; you must use Orders in your process. Please keep reading, _though, for additional benefits using Orders can provide._

The Order object is part of the standard Sales Cloud packaged, but with CPQ installed, it and its child object, Order Products, gain a series of extra fields, along with the ability to handle twin fields from the Quote and Quote Lines respectfully. However, the primary benefit to adding Orders into the flow has to do with dates. As you have probably noticed, as a theme in Salesforce CPQ, dates are crucial, but they also can be very tricky, and CPQ can be a stickler for how they are handled.

So let's go through a use case where Orders can help with dates:

Say you have a quote that has three products, a Subscription, a Hardware product, and then a support product for the Hardware product. The Subscription, a digital product, can be provisioned out to the user immediately. In contrast, it will take time to provision and ship out the Hardware product, along with its Support. Therefore, the company does not want to charge their customer for the Support until the Hardware has been received, but they want to start charging for the Subscription immediately.

In the scenario above, if you do not have Orders in the mix, you are going to need to rely on your Sales Rep to know the dates for everything while building out the Quote so that the Start and End Dates will be accurate on the Contract and Subscription Lines (or Contract Line Items in Service). In the majority of cases, though, the Sales Reps do not know this enough. So instead, a provisioning department handles this only after the Opportunity has been Closed Won and other processes kicked off. As such, this is where Orders come in.

<img src="/images/blank-diagram.png" alt="">

You can split this Quote into two different Orders, one that is just the Subscription product and one that contains both the Hardware and the Support products. By doing so, you can change the Start Date of the Order with the Hardware at the point it is provisioned, and that will automatically adjust the relevant Order Product dates. This helps because when that Order is Contracted, the dates will have been appropriately changed, the Contract will have the correct information, and the price will still be for the same amount of "time" initially purchased. So, regardless of whether the customer bought the product on June 1, but it didn't provision till August 1, they can still have it for the entire year term.

Scenes like the one above go on and on, usually requiring some split based on dates or locations for shipping. So the process goes from a singular Quote to multiple Orders to multiple Contracts.
