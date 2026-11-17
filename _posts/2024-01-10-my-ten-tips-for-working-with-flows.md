---
title: "My Ten Tips for Working with Flows"
date: 2024-01-10
categories: 
  - "admin-life"
---

I am currently working on a tech debt project where the topic of moving to flows is a big one. So I wanted to gather up the tips I have collected thus far in the journey.

1. Do whiteboard or draw on paper first the intended design - while Salesforce is adding a cut-and-paste option, it may not work for all scenarios and it can lead to having to redo quite a bit of work if you need to delete something upstream.

3. When working on flows be considerate of the type of flow you want - do you need the user to interact with it? Should it run on a clock? Or does it always happen on a record trigger? When you were using process builders, these different flavors didn't exist, it always started as a record trigger action, so this is a mental exercise of moving away from that.

5. If you find yourself working on a flow and see something that has a field value with a “.” In the front of it and a warning message about using a valid field value, then you do not have access to the field. This is a horrible way to show this, but it is the reality of it.

7. When moving to flows from process builders or workflows, really consider the following:
    - Should this be a flow? Could it be Slack or something else altogether? (e.g. email alerts)
    
    - Is a flow the best implementation? If you have a lot of logic that runs on the same event, but some of that logic doesn't need to happen point in time, consider moving to a scheduled batch class (assuming you have a developer).
    
    - Did you map out all of the existing processes to ensure you are not creating duplicates? You don't want to have more than one flow doing the same thing. Even with being able to control the order, this could lead to unexpected results.

9. Do not overload a single flow with too many nodes. Each node adds to the evaluation time and CPU consumption and can lead to it being more consuming than a Process Builder.

11. Consider splitting flows by business process and labeling them as such - this will give future you a better way to understand why something was done a certain way.

13. When creating a flow that needs to collect the details of the record, limit it to the fields you actually need. Even if selecting all is an option, it is not efficient particularly if you have hundreds of fields on the object, as it will have to store in cache all of that data and iterate over all of the fields for those actions. This can lead to a serious slowdown in performance.

15. Try to incorporate test classes. This finally came out of beta in Spring 23 and I will have another post detailing how this works. Incorporating test classes as part of the flow will make it easier for any future changes to be implemented and easily tested against the current framework.

17. Always try to use a _before_ flow instead of an _after_ flow when you can. The before flows run significantly faster since they fire prior to the save and DML actions. However, of course, this is not always an option, so if you have to use it after, try to ensure to optimize the flow where you can.

19. If you are using a _before_ flow then you do not need to use the update node, but rather you can use the assignment node, which has been optimized for the before flow actions.

Alright, that is my list for now. I will make a new one if I learn more tricks to share.
