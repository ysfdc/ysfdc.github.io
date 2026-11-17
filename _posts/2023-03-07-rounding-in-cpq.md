---
title: "Rounding in CPQ"
date: 2023-03-07
categories: 
  - "cpq"
---

Rounding in CPQ is a common topic as it leads to many headaches, particularly if you add complexity to the situation/calculation.

In general, let's start with some use cases of why rounding can be problematic:

1. Rounding rules: The rounding rules can impact how a number is rounded. For example, you can round up or down to the nearest whole number, or you can round up or down to the nearest specified decimal place.

3.  Precision: The precision of the numbers being rounded can impact how the rounding is done. For example, suppose the numbers being rounded have high precision. In that case, it can take more work to determine the appropriate rounding rule to apply.

5.  Data types: The data type of the values being rounded can also impact the difficulty of rounding. For example, suppose the values being rounded are stored as floating point numbers. In that case, it may be more challenging to round these values accurately due to floating point arithmetic limitations.

7.  Currency: The currency of the numbers being rounded can also impact how the rounding is done. Different currencies may have different rounding rules or conventions that need to be followed.

9.  Business requirements: The specific business requirements of an organization can also impact how rounding is done in Salesforce CPQ. For example, an organization may have specific rules or policies in place for how to handle rounding in different situations.

So with all of that in mind let's add some specific CPQ variables that can add to this:

1. Unit price scale - this is the scale you set in the backend of the package, which only changes what you see in the calculator, NOT what the actual calculation is doing.

3.  Salesforce's only very complicated calculation logic that you can read about here: [https://help.salesforce.com/s/articleView?id=000313862&amp;type=1](https://help.salesforce.com/s/articleView?id=000313862&type=1)

5.  QCP and Price Rules - because many people inject pricing and use formulas to calculate the pricing, different rounding practices can be in play in both types and can lead to further headaches when stacked with the information previously listed

I have no direct solution for the rounding in Salesforce. However, suppose you see values are off and you are looking in the QLE. In that case, I recommend going to the Quote Line record directly and evaluating from there. The second recommendation would be to look at all of the possibilities of how the value is getting set and see if you have custom logic in place - if you do have logic, try to make sure that you are using consistent in how you are applying decimals and rounding.

I know rounding issues are annoying and can lead to rev rec issues down the road, so try and evaluate the above to see how best to approach it.
