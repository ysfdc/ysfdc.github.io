---
title: "Review: Enabler4Excel"
date: 2017-04-06
categories: 
  - "reviews"
---

Do you ever have one of those days that you just wish you could do all your data migration to Salesforce directly from Excel? Well, today is your lucky day! [Enabler4Excel](https://www.xappex.com/index.php/products/enabler4excel) is the solution to most if not all of your data uploading, updating, downloading, and deleting problems.

Enabler4Excel is a product from [Xappex](https://www.xappex.com/), a company that specializes in integration solutions for Salesforce. The goal of this product is to enable you, the user, to not have to upload or download files between Salesforce and say DataLoader.io.

I find this tool extremely helpful in my day-to-day. I typically get 2-3 requests a day for data imports to Salesforce. (We keep all of our data uploads centralized to the Admins, which in this case is just me).

To install Enabler4Excel you need to download either their trial or paid version and then open Excel and look for it in the ribbon. (If it isn't there you may need to do some troubleshooting with the add-in tools). Once you have it loaded, it is a matter of inputting your credentials - it works with Sandboxes and Production orgs - and you are good to go.

The ribbon looks like this:

![image001](/images/image0011.png)

On the far left, you have the login icon, which will prompt you to enter your org type, email, password, and security token. If you don't have your security token on hand, you can go via Salesforce to My Settings -> Personal -> Reset My Security Token and you will get a new one in your email.

Moving towards the right gets into all the good stuff. _Get Data_ allows you to run an SOQL query on the database and pull data from Salesforce (keep in mind you can only comfortably do this with one object at a time); _Delete, Upsert, Update_ and _Insert_ are all fairly self-explanatory and will be probably your most used elements. _Merge_ and _Convert Leads_ are great if you need to do a massive clean up as this allows you to do things at scale, you cannot otherwise do in Salesforce, like merge multiple accounts to multiple accounts at once.

To be honest, in the last section, _Utilities_, I haven't really utilized anything beyond the _Convert IDs_, which is a really nifty tool to quickly convert the 15 digit IDs to the 18 digit IDs (if you are looking for more info on that go [here](https://help.salesforce.com/articleView?id=000004383&type=1)).

Overall, this is a great time-saving tool and is really worth the $299.

**I give this product a B+.** The reason it doesn't make the A mark is I really wish I could upload and download for more than one object at a time to save myself all the various V-LOOKUPs.
