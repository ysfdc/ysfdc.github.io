---
title: "Understanding Salesforce Multi-Currency Implications"
date: 2020-10-06
categories: 
  - "admin-life"
  - "cpq"
  - "tips-tricks"
---

When [setting up multi-currency](http://sf9to5.wordpress.com/2020/07/21/setup-multi-currency/) in your org there are some implications that you need to be aware of.

When handling the building and testing of multi-currency in the sandbox, make sure to think about the following items:

- The first thing that you need to do when setting up multi-currency is to activate any additional currencies that you will be using. You can see the guide here on setting up multi-currency.
- Exchange rates are primarily for the purpose of two things:
    - Allowing your company to sell in other currencies - i.e. setup pricebook entry records in other currencies
    - Allow people in your company to see and report on values based on the exchange rates through the parenthetical values (values found inside of parathesis next to a currency field)
- Each user has their own default currency defined on the user record and typically is alignment with the geographical location
    - This default value is what will be used to determine what to display in the parenthetical/converted value. If the record is in the same currency as their default, they will not see any parenthetical value. If the record is in a different currency than their default, then they will the value times their currency conversion rate in the parenthetical.
- If you have any third-party integrations that utilize currency fields, make sure to include them in your testing.
    - You will also need to consider which value you are interested in either pulling from or pushing to the third party application; you have the option of either the converted value or the actual value.
- Keep in mind that going forward for any data load that occurs that includes a currency field, the Currency code field needs to be loaded as well.
- If you are using Standard quotes or CPQ, you will need to ensure that for every currency you want to use, you have a corresponding pricebook entry.
    - In the case of CPQ, you will need both a standard pricebook entry in that currency and a CPQ pricebook entry in that currency.
- Having currency rates does not mean that the pricebook entry values are automatically adjusted based on the rate.
- When testing and validating Opportunities, keep in mind that the amount field on Opportunity will always be in the currency of the Opportunity record.
- When working on the setup make sure to include validation to ensure related records (Opportunity and Quote) are in the same currency.
- If you are not using the dated exchange rates (see below for more information Advanced Currency management), then you need to conscious of the fact that changing the exchange rate will automatically apply to all parenthetical values.

There are also items to keep in mind if you decide to turn on Advanced Currency Management:

- The primary purpose behind setting up Advance Currency management is to hold closed-won amount conversion values at a set rate. As noted above, without this turned on, the value in parenthetical will continue to change every time the conversion rate is updated.
- Dated rates apply to the following objects, fields, and related reports:
    - Opportunities
    - Opportunity Products
    - Opportunity Product Schedules
    - Campaign Opportunity fields
    - Opportunity Splits
    - Standard Quotes
    - Standard Quote Lines
- When reviewing CPQ, keep in mind that Dated Exchanged rates are not applied. So while the Opportunity Amount may freeze, the Quote amount values will continue to roll with each currency rate updated.
- If you are using cross-object formulas, they will only use the static conversion rate and will continue to change if the rate changes - they do not use the dated rates.
- Rollup summary fields are heavily impacted by turning on Advanced Currency Management.
    - Rollup summary fields that are based on Opportunity fields that calculate currency cannot use dated exchange rates and are therefore disabled.
    - When implementing advanced currency management it will be necessary to delete the following:
        - Rollup summary fields on standard objects that summarize Opportunity fields.
        - Rollup summary fields on custom objects that are based on Opportunity fields.
- Please keep in mind that Dated exchange rates are not completely supported in Lightning
    - [https://success.salesforce.com/ideaView?id=0873A0000003fbgQAA](https://success.salesforce.com/ideaView?id=0873A0000003fbgQAA)

Related: [How to Setup Multi-Currency](http://sf9to5.wordpress.com/2020/07/21/setup-multi-currency/)
