---
title: "How to create a single Accounts and Service Contracts report"
date: 2022-02-01
categories: 
  - "admin-life"
  - "tips-tricks"
---

This tutorial will walk you through how to create a report that meets the requirement of Accounts with Service Contracts. The goal is not to add any fields and to start from the Account object. Unfortunately, Salesforce does not support Accounts and Service Contracts together for a custom Report Type as of the day of writing, so we will use a joined report to get the same effect.

1. Go to Setup --> Report Types --> Create new Custom Report Type
2. Set the Primary Object to be Service Contract and fill out the rest as you want  
    

![](/images/2021-12-28_09-56-05.png)

3. You do not need to select any additional related objects on the next screen  
    

![](/images/2021-12-28_09-56-24.png)

4. Go to the layout, and the on the right select add from Lookup Field  
    

![](/images/2021-12-28_09-56-51.png)

5. You are going to want to add pretty much any Account field that are you going to want to use, also make sure to include Account Name and ID, otherwise you can end up with an error message later in the process  
    

![](/images/2021-12-28_09-56-58.png)

6. Go to reports, create a new report and select Accounts type
7. Change the type of report to a Joined Report  
    

![](/images/2021-12-28_09-54-07.png)

8. Add a block, and look for the Service Contract report  
    

![](/images/2021-12-28_09-54-14.png)

![](/images/2021-12-28_09-57-28.png)

9. If you did not bring in overlapping fields (I brought in all of the Account fields), you would get this error - keep adding account fields until this goes away  
    

![](/images/2021-12-28_09-57-39.png)

![](/images/2021-12-28_09-59-54.png)

10. Once you have added the block, you can update your filters and set your columns
11. Make sure to Group by Account Name, otherwise it will look like the Contracts belong to a different account  
     

![](/images/2021-12-28_10-01-44.png)

Final Result:

![](/images/2021-12-28_10-08-30.png)

If you do not need to do Accounts with and without Service Contracts, you can use the new Report Type you made and do Service Contracts with and without Accounts in a normal report using filters.
