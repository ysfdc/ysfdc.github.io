---
title: "How to Create Dynamic Field Sets for QLE"
date: 2020-01-28
categories: 
  - "cpq"
  - "tips-tricks"
---

Recently, I had a need to be able to change between two different sets of fields while looking at the columns in the QLE. The reason? There were two distinct sets of fields that the users needed to review, but including them in one Field Set led to an unbelievable amount of fields at once and way too much scrolling.

Here are the steps I took to make that scenario a reality, including the ability to change the fields right from the QLE:

1. Create the Field Sets that you want to have as options for the columns in the QLE (Setup --> Objects --> Quote Line --> Field Sets --> New Field Set)
2. Create a field on the Quote object with the Field Name - _EditLinesFieldSetName_
    1. The Field Label can be whatever you want, but the name needs to be as noted above because this is a special field that Salesforce offers to achieve this setup ![2019-12-24\_11-11-27](/images/2019-12-24_11-11-27.png)
    2. The field should be of type Picklist
    3. The values for the picklist should be the Field Names of the Field Sets you made in step 1 - this means no \_\_c but also no spaces ![2019-12-24\_11-11-34](/images/2019-12-24_11-11-34.png)
3. Now add the new field you created in step 2 to the Quote Line Editor Field Set (Setup -> Objects -> Quote -> Field Sets -> Line Editor) ![2019-12-24\_11-12-39](/images/2019-12-24_11-12-39.png)
4. Now go to a Quote to test it out! Switching the value in picklist and Quick saving will change the column headers that you see. You may set a default value if you want something other than the Line Editor to be the standard set of columns. ![2019-12-25\_12-18-31.gif](/images/2019-12-25_12-18-31.gif)

Unfortunately, at this time, this is only available for the columns in the QLE and not the header in the QLE. Here are two ideas that you can upvote if you would like to see that changed.

[https://success.salesforce.com/ideaView?id=0873A0000003aJkQAI](https://success.salesforce.com/ideaView?id=0873A0000003aJkQAI) [https://success.salesforce.com/ideaView?id=0873A000000CUciQAG](https://success.salesforce.com/ideaView?id=0873A000000CUciQAG)
