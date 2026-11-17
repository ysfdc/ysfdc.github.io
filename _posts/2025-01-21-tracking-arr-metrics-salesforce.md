---
title: "Tracking ARR Metrics in Salesforce"
date: 2025-01-21
categories: 
  - "cpq"
---

This has been a topic I have wanted to cover for a while. Throughout my CPQ career, I have gone through many iterations of helping customers achieve Annual Recurring Revenue numbers (ARR). The challenge I have faced with this over the years has always been a mixture of two key issues: 1) The ability to use Salesforce CPQ as it was designed and 2) An understanding that Salesforce is a single point-in-time in time tool and requires a third-party tool to really achieve these kinds of metrics.

Salesforce CPQ is essentially a box and doesn't play nicely when you go outside the processes of that box. That's why it's essential to fully leverage the renewals and amendments features in CPQ. These built-in tools are designed to handle the complexities of recurring revenue management right out of the box. Everything works smoothly if the steps are followed correctly, ensuring ARR can be tracked without missing a beat. Renewals and amendments allow you to [extend contracts](https://sf9to5.com/2022/03/29/how-to-amend-extend-contract-cpq/) and accurately capture recurring revenue changes from upgrades, downgrades, or contract changes. Staying disciplined using these features helps prevent manual errors and ensures all ARR changes are correctly reflected in your pipeline and reports.

Of course, once you have all of the revenue data in Salesforce, reporting on it requires additional customization. Standard reports may not always cut it, particularly if you need to track net new ARR, renewals, and any roll forward or backward metrics. Custom report types allow you to set up reports based on contract data for specified periods. However, while dashboards in general can be great for visualizing key metrics, without custom fields, seeing values like Net New ARR, Churn Rate, and Total ARR over time, as well as more complex scenarios - like multi-year contracts or split billing - may require more advanced reporting.

When looking for more advanced capabilities, a tool like Tableau can extend the data visualization and reporting options. These tools also allow you to combine Salesforce data with other sources like financial systems. Within Tableau, ARR metrics can be viewed for any time range, offering more flexibility for filtering by region, product, or customer type. With this type of tool, it is possible to generate complex dashboards showing upsell, downsell, crossell, etc., with much greater ease than trying to do in a Salesforce report or Dashboard.

Consistency is vital to keeping ARR data accurate and actionable. The business users who interact with CPQ must ensure that they follow through on the process and stay within the guidelines that CPQ provides. Regular training on CPQ, particularly around renewals and amendments, can prevent data gaps from forming. Automating reminders for upcoming renewals and conducting regular data audits to catch any discrepancies will ensure you maintain a clear and accurate view of your recurring revenue.

While Salesforce CPQ ensures all the necessary data is in the right place, extracting accurate and actionable ARR metrics requires going beyond the standard system. Tableau empowers you to create the visual representations and dynamic reports your business needs, enabling you to slice and dice ARR data in ways that Salesforce alone can't.
