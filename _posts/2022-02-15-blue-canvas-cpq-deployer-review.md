---
title: "Blue Canvas CPQ Deployer Review"
date: 2022-02-15
categories: 
  - "admin-life"
  - "cpq"
  - "reviews"
---

_This post is sponsored by [Blue Canvas](https://bluecanvas.io/cpq). All content and opinions are my own._

Recently a colleague introduced me to [Blue Canvas](https://bluecanvas.io/) - a company focused on CI/CD and DevOps tools for the Salesforce ecosystem. They recently launched [CPQ Deployer](https://bluecanvas.io/cpq), a tool to help administrators move CPQ data from one org to another. If you are not familiar with CPQ, it’s the Quote to Cash component within the Revenue Cloud from Salesforce. Almost all development for CPQ takes place as data, unlike most other configurations in Salesforce. Therefore, a [data migration](https://sf9to5.com/2017/09/28/cpq-data-migration/) tool can help simplify the process.

CPQ Deployer is taking on some of the competitors, like Prodly, founded by the original folks from Steelbrick (the company Salesforce bought CPQ from). The tool provides a web-based UI to interact with and deploy from one org to another.

I got my license for free as part of the community ambassador program (thank you, Blue Canvas), so I cannot say too much about the pricing. However, you can check out their pricing page for more information. The version of the tool that I will discuss is the professional level.

When you first log in to the CPQ Deployer tool, you are presented with a straightforward screen to set up your Source and Target org. One nice thing is the orgs you are connecting to do not need to be related to each other. This can be great if you built something in a CPQ dev org and now need to port it over to your company’s org.

![](/images/hxDgfSog9ZtF_ItUyEcpcBm-bFKxg-FmYcl8U-cxLVmSl4baJS1A1Hb3kyOILKQkzp2aiaduVWOBRmh80WTMFxQQ2fB-cw1GWnyxoycnHGqv-72PTuXvSSHQzeV1-q8VroLT34iT)

Once logged in, you are taken to the primary workspace. This is where you will do all of the work you need to complete a deployment.

You can search for products by name or other custom fields and filter based on specific attributes, including if the record is to be UPDATED or CREATED. One missing feature I noticed is that there is no sort function. There are also many places where I would have appreciated more columns, but there is no way to add them (e.g., Active).

![](/images/Fu_Zy32Mvr3esWA0nkV8NZOr1hODduG7qNKPXjcQynsvWFSe3z3Myz-vlWxDWSy7UgpiAuTyL2vkHEriHflZT-60Wilj0JBxqVzBLbDskIt6KzEiv0qhl8Crr8AS_0NSvCG4Dmvm)

You can select the records you want to deploy within each object on the sidebar. In addition, you may see tabs at the bottom called Required or Related. These are populated if another primary object has records needed for the migration. There will be a button to select them.

However, you do not get to choose which child-related records come over with the selected records. So, for example,  if you have a bundle with Features and Options, you will not get to pick which are ported over. I believe this is a significant missing feature, and I hope to see it added soon.

![](/images/xwa--srx_PWbGOwENrauTjJNd5QKFrqeLXjc-CGkLMTiRqXRaD_bwlLlSS6tfHHO-khQvgBLLK5gqT-aRyYbIqDEN3TuLmG7jvOyDjpB0AL00W0g7YeZZLSkR6OCUTPp-Zq3rmw3)

Deploying items is very simple, although a bit confusing. You will see the count on the sidebar wherever you have selected an item. 

![](/images/d9ZjEY5aZHW_SVdHuxeMHauaDfe8KU_E96m2JKSFIZWirxj-681z3KkU7LU6cA1EX5gSTQbl2AxeD7g27dLDckGsJ-isTx6FhB-MHs1V7x54qPHXIYXCLPEiub10NIcMVRUaaY6x)

You do not need to be in the section where you selected records for the Deploy button down in the far right corner to work. When you click that button, it will deploy anything you have selected. Once you deploy, you will get a success message and the ability to see the data moved in a JSON format; then, you can check out your Target org to ensure the data was successfully migrated.

![](/images/XVmjxVWz0Ta1oi4nl8u_3eY_5Dtgl4E9Q-ypKMeAKf3QkDjgHDV0O5alLvCujvTQyc-6oVNSMpWK7yHaAVdzg3xrHbptU7Kmado1wPCoJcZ_aG4gztt66BpEGEm8NOHLccJ8s-8Z)

Another thing to note is that if you leave the tab open and your session does expire, the way to reinstate it is by logging out of Blue Canvas and then opening a new tab and logging back in. You will also need to log in again to your Source and Target orgs. The system does not remember or store anything about the orgs you are syncing with.

Well, that pretty much covers the whole kit and kaboodle of the [CPQ Deployer](https://bluecanvas.io/cpq) product. You can use it to migrate CPQ data from one org to another. While I am no longer someone actively doing this, this could be an excellent and straightforward to use product with some feature updates. I am currently rating this product with a 3/5 star rating as I think that there is still room to grow. Personally, I believe the most significant missing feature is the ability to select independently which child records will come over with any given parent record. However, this is an upcoming product, and they are making updates frequently, so I have high hopes that this will become a tool most admins will find valuable with time.
