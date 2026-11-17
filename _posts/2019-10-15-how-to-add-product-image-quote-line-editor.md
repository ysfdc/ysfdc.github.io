---
title: "How to add Product Image in Quote Line Editor"
date: 2019-10-15
categories: 
  - "cpq"
  - "lightning"
  - "tips-tricks"
---

Recently, a customer wanted to display the images of the products they sell within CPQ to make it easier for their sales reps to identify the differences in the products. After much research and digging through the Salesforce documentation, I found it to be lacking in the context needed to do it in Lightning.

Here are the step by step instructions for adding a Product Image in the QLE:

1. Upload all product images as Files ![2019-10-05\_11-14-40](/images/2019-10-05_11-14-40.png)
2. Create two fields on product
    1. Text area field: to be filled in with URL of the image
        1. Go to the actual image in the Files, where you can see the details ![2019-10-05\_11-18-58](/images/2019-10-05_11-18-58.png)
        2. Right-click on the image and select Open Image in new Tab
        3. Copy everything in the URL after "version/" and put into the Text Area field you created on the Product record ![2019-10-05\_11-21-05](/images/2019-10-05_11-21-05.png)
            1. Make sure to associate the correct image with its corresponding product
    2. Formula field for Image: IMAGE("/sfc/servlet.shepherd/version/"+Product\_Link\_\_c+".png","photo",32,32) \*\* swapping name of custom field for the text area name
3. Create two fields on Quote Line
    1. Twin field from product:
        1. Text area with same API name as the product text area
    2. Image field:
        1. Use the same formula as you did for the Formula field on the Product record
4. Add image field form quote line to line editor Field Set.
    1. Field Sets --> line editor

Final Result:

![2019-10-05\_11-22-18](/images/2019-10-05_11-22-18.png)

* * *

Related: [How to Set up Twin Fields in CPQ](http://sf9to5.wordpress.com/2019/10/08/how-to-set-up-twin-fields-cpq/)
