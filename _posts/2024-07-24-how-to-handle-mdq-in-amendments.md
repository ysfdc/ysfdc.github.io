---
title: "How to Handle MDQ in Amendments"
date: 2024-07-24
categories: 
  - "cpq"
---

Handling amendments in Salesforce can be tricky, especially when Multi-Dimensional Quoting (MDQ) is in play. MDQ allows you to break down a single product into multiple segments, typically representing different time periods, for more granular pricing and quotes. But what happens when you need to amend these quotes? Let’s dive into three common scenarios: canceling and replacing lines due to price changes, updating existing lines, and removing future years.

### Scenario 1: Cancel and Replace Lines Due to Price Change

Price changes are inevitable; when they occur, you might need to cancel and replace lines on a quote. Here’s how to handle it correctly:

1. **Set the Quantity to Zero**: In Salesforce CPQ, locate the line item that needs the price adjustment. Instead of directly modifying the end date, set the quantity to zero. This action effectively cancels the existing line by terminating it automatically.

3. **Create a New Line**: Add a new line item with the updated pricing. Ensure this new line starts immediately after the old line is canceled.

5. **Adjust MDQ Segments**: If the product is MDQ, you’ll need to break down the new line into the appropriate segments to reflect the updated pricing across the time periods.

This method ensures that historical data remains intact while accurately reflecting the new pricing. Please note that Salesforce does not allow price changes of any kind during an Amendment, which is why this cancellation process is required.

\* If you are tracking ARR, it would be recommended to have a custom field that points back to the zeroed-out Quote Line so that you can generate logic that allows you to still follow the breadcrumbs when these types of changes occur.

### Scenario 2: Update Existing Lines

Updating existing lines in MDQ can be straightforward, but there are limitations to remember. Here’s what you can and cannot do:

**What You Can Do:**

- **Adjust Quantities**: You can update the quantity of the product in each segment. This can be an upsell or a downsell.

- **Add new products**: In some cases, you might be offering a new product related to an existing product. You can add net new products to the via that are intended to co-term with the Amendment's end date.

**What You Cannot Do:**

- **Change the Product**: Once a product is part of an MDQ line, you cannot switch it to a different product. If the product itself needs to change, you’ll need to cancel and replace the line.

- **Alter the Structure**: You cannot change the MDQ structure (e.g., from annual to quarterly) once the line is created. Structural changes require canceling the existing line and creating a new one with the desired structure.

### Scenario 3: Removing Future Years

Sometimes, a customer may decide to cancel future years of a subscription. Here’s how to handle it:

1. **Set the Start Date:** The start date for this Amendment should be the cancellation date so that the proration of the return value is accurate.

3. **Identify the Future Segments**: Locate the MDQ segments that correspond to the future years being removed.

5. **Terminate the Segments**: Set the quantity for these segments to zero. This effectively cancels any commitments beyond this point.

7. **Update the Contract**: Reflect these changes in the service contract to ensure all records are accurate and up-to-date. You do this through contracting the Amendment Opportunity back to the original Service Contract.

Removing future years requires careful attention to ensure that only the intended periods are affected and that all contractual obligations are met up to the point of termination.

Always ensure to test when cases involve anything with strange modifications in date. CPQ, particularly with MDQ in Amendments, tends to act wonky.

Handling amendments with MDQ in Salesforce can be complex, but you can manage changes efficiently and maintain accurate records with a clear understanding of the processes and limitations. Whether dealing with price changes, updating existing lines, or removing future years, following these best practices will help ensure smooth and effective amendments.

For more about Amendments, check out these posts:

[](https://sf9to5.com/2019/01/22/cpq-amendment-renewal-quotes/)[CPQ Amendment and Renewal Quotes](https://sf9to5.com/2019/01/22/cpq-amendment-renewal-quotes/)

[How to Cancel a Contract in CPQ](https://sf9to5.com/2022/07/06/how-to-cancel-contract-cpq/)

[How to Amend and Extend a Contract in CPQ](https://sf9to5.com/2022/03/29/how-to-amend-extend-contract-cpq/)

[The Implications of Changing the Contract Date in CPQ](https://sf9to5.com/2021/03/23/implications-changing-contract-date-cpq/)
