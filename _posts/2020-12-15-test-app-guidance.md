---
title: "How to test In-App Guidance"
date: 2020-12-15
categories: 
  - "lightning"
  - "tips-tricks"
---

Recently I learned that testing In-App Guidance in a sandbox is not as straightforward as one might think. Apparently, for the purpose of not [affecting automated testing](https://help.salesforce.com/articleView?id=000349069&type=1&mode=1), Salesforce created a special testing method specifically for In-App Guidance.

Once you have created your [In-App Guidance](https://sf9to5.wordpress.com/2020/06/16/how-to-in-app-guidance/) prompt then you can go back to the Setup page and you will see a button called Start Testing.

<img src="/images/image.png" alt="">

Click on the Start Testing button to see your In-App Guidance prompts in action. The button takes you to a view of your org where you can navigate to where the prompt will be displayed.

<img src="/images/image-1.png" alt="">

Once you are done testing, you can either click Exit Testing at the top or click to go back into the builder to make further adjustments.

I hope this saves you some time in determining why your prompt in a sandbox is not showing.
