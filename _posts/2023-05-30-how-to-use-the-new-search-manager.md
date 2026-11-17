---
title: "How to use the new Search Manager"
date: 2023-05-30
categories: 
  - "admin-life"
---

In the [Spring 23 release](https://sf9to5.com/2023/01/31/spring-23-my-favorite-things/), Salesforce launched a Search Manager for Einstein Search. Within the manager, you are able to control the details and configurations of search terms for a specific profile.

Go to Setup --> Search Manager  

![](/images/image.png)

Create a Configuration and select the Profile you want to be associated with it  

![](/images/image-1.png)

You will see which fields are available or already searchable (blank or checkmark) versus those that are locked (with a locked icon). You can edit any of those that are not locked, including picklist options (which is a new feature).

![](/images/image-2.png)

There is also a filter on the right-hand side to quickly reduce the list to show either only searchable or unsearchable, the type of field that it is, and whether it is standard or custom.  

![](/images/image-3.png)

While I think the UI is nice and makes it easy to understand what can/cannot be searched, I think making us still go to two totally different places for setting up search-related items to an object, is one too many steps for me. The fact that each search layout and their related profiles are still in the object setting simply makes no sense, they should be combined together.  

![](/images/image-4.png)
