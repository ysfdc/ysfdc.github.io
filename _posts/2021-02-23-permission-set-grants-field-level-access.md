---
title: "Why Permission Set Grants Extra Field Level Access?"
date: 2021-02-23
categories: 
  - "admin-life"
---

Alrighty, get ready for a slightly confusing scenario that hopefully teaches you something you didn't know about [Profiles and Permissions](https://sf9to5.wordpress.com/2019/03/19/salesforce-profile-auditing-guide-1/). I, for one, was surprised to learn that this is how Salesforce works, even after all these years.

So you have a Profile, Sales - Custom, and you have a Permission Set, called Camping.

On the Sales - Custom Profile for the Object Camping Items I have removed all Object level permissions:

<figure>

<img src="/images/image-2.png" alt="">

<figcaption>

Profile

</figcaption>

</figure>

You will also notice that I left the Field level permissions alone, but they are not relevant because the Object level permissions were removed.

Now, in the Camping Permission Set, you will see that I opened up access for Read and Edit and gave only certain fields Read/Edit access.

<figure>

<img src="/images/image-3.png" alt="">

<figcaption>

Permission Set

</figcaption>

</figure>

The field to call out is Packed - you will see in the Permission set there is no access, but now go back up and look at the Profile, you will see that those check boxes are still checked, but Profile isn't granting Read/Edit access to the object at all.

So at this point you probably see where I am going to end up; despite my understanding that the Permission Set was to open up access based on what it granted, that it apparently also grants any access to a field on the Profile level even if the Profile level for the object was essentially turned off.

Logged in a User with the combination above I was able to both Read and Edit the Packed field on the Camping Item object.

This means that when you are creating new fields, the FLS step where you check the boxes for the Profiles is very important, because assuming that the user doesn't have access because of the Profile, is an oversight because if they have a Permission Set that grants them Read/Edit on the Object level, then checking the FLS on the Profile will give them access regardless.
