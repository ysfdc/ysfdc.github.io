---
title: "How to: Create an Alert in CPQ"
date: 2017-08-18
categories: 
  - "cpq"
  - "tips-tricks"
---

If you use CPQ in your organization, your users may not always remember to add related products when they configure a quote, and you may not necessarily the items bundled. What do you do to ensure they don't forget? You use the built-in alert function of CPQ.

## Business Case

You have two products, Laptop and Charger, and you want to ensure that when a quote is created for a Laptop that the user didn't forget the Charger. Your users may forget to include the Charger as part of the quote and you need to remind them about this product.

## Business Solution

Since we only need to remind the user to add the Charger, but not force the purchase of it, we can use an Alert in CPQ to the tell user 'Hey, Don't Forget to add a Charger!'. This will still allow the user to proceed with the quote in the case that the customer already has a charger and doesn't need another one.

To create an Alert, we will need to create a Product Rule, 2 Summary Variable, and 2 Error Conditions. The connection between these objects is depicted in the following diagram: ![UML Diagram](/images/2017-08-17_17-59-51.png)

My Summary Variables are going to be the variables we are checking for in the Product rule; in my case, I am looking for LAPTOP and CHARGER as the Product Code. For my Error Conditions on the Product Rule, I am going to specify to look for at least one Laptop (greater than or equal to) and that there is less than one Charger.

## Steps

### Create the Summary Variables

_Since we need the Summary Variables for the Error Conditions within the Product Rule, we will create them first._

1. Go to the Summary Variable object and click New ![New Summary Variable](/images/2017-08-17_17-30-442.png)
2. For the first rule fill out the fields that are highlighted below (\*note that in your own environment you may need to make some adjustments) ![Summary Variable 1](/images/2017-08-17_17-32-18.png)
3. For the second rule fill out the fields that are highlight below ![Summary Variable 2](/images/2017-08-17_18-51-29.png)

### Create the Product Rule

1. Go to the Product Rules object and click New ![New Product Rule](/images/2017-08-17_17-33-10.png)
2. Create a name that is relevant and meaningful to you and future folks
3. Fill out the fields as they highlighted below. IMPORTANT - Do not forget to mark the rule as Active! ![Product Rule Details](/images/2017-08-17_17-38-24.png)

### Create the Error Conditions

1. After you have saved the rule, click New in the Error Conditions related table ![New Error Condition](/images/2017-08-17_19-01-43.png)
2. For the first rule, fill out the fields that are highlighted below (\*note that in your own environment you may need to make some adjustments) ![Error Condition 1](/images/2017-08-17_17-45-23.png)
3. For the second rule, fill out the fields that are highlight below ![Error Condition 2](/images/2017-08-17_17-45-35.png)

### Test! Test! Test!

1. Create or open an existing quote ( I recommend using a quote that doesn't have any line items to prevent misfires of other rules if you are testing this use case specifically)
2. Click Edit Lines
3. Add your Laptop Product ![Add Laptop](/images/2017-08-17_17-41-50.png)
4. Click Save ![Click Save](/images/2017-08-17_17-42-04.png)
5. You should see an Alert pop-up with the message that you entered in the Product Rule ![Alert](/images/2017-08-17_17-46-14.png)

You are all set!
