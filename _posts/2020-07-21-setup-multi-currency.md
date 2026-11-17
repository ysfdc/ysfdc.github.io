---
title: "How to Setup Multi-Currency"
date: 2020-07-21
categories: 
  - "admin-life"
  - "tips-tricks"
---

Multi-currency is a feature that comes with Salesforce that is very useful if your company either is multiple countries with different currencies or simply sells in more than one currency. Below I am going to walk you through the basic steps of setting up a secondary currency using GBP (Great British Pound).

1. Go to Setup --> Company Information ![2020-06-20\_13-50-19](/images/2020-06-20_13-50-19.png)
2. Click on the Edit button ![2020-06-20\_13-50-41](/images/2020-06-20_13-50-41.png)
3. Check the Activate Multiple Currencies box and click Save ![2020-06-20\_13-50-55](/images/2020-06-20_13-50-55.png)
4. You will now see an extra button called Currency Setup, click it ![2020-06-20\_13-51-15](/images/2020-06-20_13-51-15.png)
5. By default, Advanced Currency management will be off ![2020-06-20\_13-51-42](/images/2020-06-20_13-51-42.png)
6. By default Parethentical Currency Conversion will be on - this is what you will see on any currency field when your default currency and the currency of the record you are on do not match. ![2020-06-20\_13-51-42-1](/images/2020-06-20_13-51-42-1.png)
7. In the Active Currency section, click New ![2020-06-20\_13-51-42-3](/images/2020-06-20_13-51-42-3.png)
8. Select your Currency Type, add your conversion rate, and set your decimal places (used for rounding the Parenthetical value) ![2020-06-20\_13-54-02](/images/2020-06-20_13-54-02.png)
    1. Conversion rates in Salesforce are controlled by you; it is possible to purchase third-party products on the AppExchange if you need something more sophisticated for obtaining the values if Google does not work for you.

Other buttons/features

Change Corporate Currency - this allows you to change the default currency for the company as a whole. ![2020-06-20\_13-54-51](/images/2020-06-20_13-54-51.png)

Edit Rates button - this allows you to change the rates associated with your currencies ![2020-06-20\_13-55-08](/images/2020-06-20_13-55-08.png)

Edit on the Active Currency line - this allows you to change the decimal places associated with the currency ![2020-06-20\_13-55-26](/images/2020-06-20_13-55-26.png)

That's it for you basic multi-currency setup. Stay tuned for more.
