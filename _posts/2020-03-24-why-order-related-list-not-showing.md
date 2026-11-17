---
title: "Why is the Order related list not showing?"
date: 2020-03-24
categories: 
  - "cpq"
  - "lightning"
---

Why is the Order related list not showing up on my Opportunity page layouts? This may seem like a simple thing to fix, you may be saying. Add it to the layout and make sure the user has access to the Orders object.

 

![2020-03-14\_15-56-51](/images/2020-03-14_15-56-51.png)![2020-03-14\_15-57-23](/images/2020-03-14_15-57-23.png)

 

Despite going through all of the usual checks, including logging in and out, to make sure the [Lightning cache](http://sf9to5.wordpress.com/2019/02/26/why-quick-action-not-show-lightning/) wasn't getting in the way, I was still unable to resolve such a simple issue. It took some very thorough and deep googling in order to find the solution. Apparently, reasons unbeknownst to us, Salesforce has a random requirement that the Opportunity Lookup field is on the Order layout and that the field not be hidden from the User.

![2020-03-14\_15-59-31](/images/2020-03-14_15-59-31.png)![2020-03-14\_16-00-19](/images/2020-03-14_16-00-19.png)

Once you have done that, refresh your page and you should be golden! Shout out to the community members who managed to figure this one out!

![2020-03-14\_16-01-14](/images/2020-03-14_16-01-14.png)
