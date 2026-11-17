---
title: "How to make Lightning Run Faster"
date: 2019-06-25
categories: 
  - "admin-life"
  - "lightning"
  - "tips-tricks"
---

Many people are resistant to the movement from Classic to Lightning. However, with the ever-increasing push from Salesforce to switch platforms, understanding how to make Lightning work for you, instead of against you, is critical.

First, a little bit of background about Lightning. Classic is a server run platform, what that means is all of the queries and placement of data are held on the server and then pushed to the browser for you to see. In Lightning, the primary elements that you see are client side - this means that when a page load is reliant on the browser and the cache to display the information to you (there's still plenty of server-side workloads). In addition to the difference of client vs. server side, Lightning is also working on more popular web platforms, which are more adherent to current day protocols, security, and setup. Both of these things are important to keep in mind when making the move to Lightning and when building in Lightning.

Now for some tips to help with the speed of Lightning, the slow down of which can be caused by the two elements noted above.

Since Lightning is client-side heavy, every added element to a page causes the page to take longer to load. This is very important when thinking both about the detail page layout and the record page layout. Reducing fields to the necessary ones, instead of maintaining 100-200 fields on the page will help with load time. Also, reducing the number of Active related lists that need to be displayed can help with the load time. Consider using the Related Quick Links as a replacement for Related lists as they do not require loading all of the data onto the page, but still, make it easy for the user to access the information.

Another common mistake that slows things down is not updating your browser or using a non-supported browser. Since the browser is now doing the heavy lifting, making sure you are up-to-date is an essential step in ensuring quicker speeds. From a business perspective, another element to keep in mind is ensuring users have access to good Internet connections, along with devices that can support higher CPU usage. While harder to quickly adjust the last two items, they do play a role in the speed-time of the page.

Lastly, I recommend reading through this piece of documentation provided by Salesforce. It specifies guidelines and tools for ensuring you have the most optimized pages and thereby speedier items.

[https://help.salesforce.com/articleView?id=000250291&language=en\_US&type=1](https://help.salesforce.com/articleView?id=000250291&language=en_US&type=1)

While the move to Lightning may seem daunting, especially with the bad press out there, I can tell from experience that once you make the move, and you keep these things in mind, you are likely to never want to return to Classic. The pros and ever-increasing features of Lightning now heavily outweigh the negatives and the need to stay on Classic.
