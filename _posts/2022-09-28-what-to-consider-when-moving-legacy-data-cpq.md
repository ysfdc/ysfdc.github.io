---
title: "What to consider when moving Legacy Data into CPQ?"
date: 2022-09-28
categories: 
  - "cpq"
  - "tips-tricks"
---

The audience for this post is those who are moving or doing one of the following:

- Moving into Salesforce CPQ from a third-party tool
- Transitioning from standard Salesforce Quotes to CPQ
- Completing an implementation of CPQ, where previously Amendments/Renewals were not correctly in use

_This article does not account for any data related to the Salesforce Billing package._

Setting up Salesforce CPQ when you are coming from a different platform can seem like a daunting undertaking and, depending on the complexity of previous systems, can be, in fact, a heavy lift. Below are some tips and tricks I have learned over the last several years when trying to move into Salesforce CPQ.

- If you are in a third-party system and have active contracts, the ideal solution is to create the Opportunities, Quotes, and Contracts that match those existing contracts.
    - These can be data loaded, but you need to ensure that if you do this, you hit all required fields on the Quote and Quote Lines for Contracts to generate correctly.
    - Make sure to load into the Net Total if you are concerned about proration if this was not a previously available function.
    - It is recommended that the Contracts not be loaded but instead use the automation built into CPQ to generate them.
- Data loading into Salesforce can be tricky if the pricing and previous product model do not match the current structure. For example, you were selling multi-year deals with custom pricing as multiple lines on a quote, and now CPQ has introduced MDQ - data loading; this will be near impossible without a lot of manual overhead.
    - If this is your scenario, I recommend creating a shell contract record and generating a net new Quote in CPQ with the latest pricing and product model on renewal.
- Moving from standard Quotes to CPQ Quotes should not be considered a one-to-one exercise. Similar to the note above, pricing models can be set up different in CPQ, as well as the introduction of proration based on time can impact pricing; thus, it is crucial to understand this before trying to move/load any data into CPQ
- It can often make more sense to start from scratch where the first Quote for an Account is in CPQ, and the previous contracts are not loaded. However, if you need Assets or Entitlements based on past/existing contracts, those can be created outside the standard CPQ stream to enable any required flows until a new Quote is generated.
- Suppose you are currently using CPQ but only now looking into Contracts, Amendments, and Renewals. In that case, it is essential to understand how you were generating upsell/cross-sell, downgrades, cancellations, and renewals before making the change. The reason is that Salesforce CPQ provides out-of-the-box methodologies for all of these, and if you were not following them previously, you would likely need to start with the next Quote you can contract for that Account.
    - For more information on the standard practice, check out the following posts:
        - [Opportunity Renewal Creation in CPQ](https://sf9to5.com/2018/12/18/opportunity-renewal-creation-cpq/)
        - [CPQ Amendment and Renewal Quotes](https://sf9to5.com/2019/01/22/cpq-amendment-renewal-quotes/)
        - [How to Amend and Extend a Contract in CPQ](https://sf9to5.com/2022/03/29/how-to-amend-extend-contract-cpq/)
