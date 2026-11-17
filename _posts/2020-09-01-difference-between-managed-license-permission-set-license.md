---
title: "What is the difference between Managed License and Permission Set License"
date: 2020-09-01
categories: 
  - "admin-life"
---

If you have ever installed a package from the App Exchange that has a specified number of licenses that can be given out to users then you are probably familiar with a Managed License. A managed license is a license required to be given to a user in order for that user to have access to the contents of the installed package. Typically, this is provided by either going to the Managed Packages on the User record or by going to Installed Packages --> Manage Licenses. After granting access to the package, the next step is to either adjust their profile to have the necessary read/write access or give them a Permission Set with the necessary read/write access.

<img src="/images/image.png" alt="">

In walks Permission Set Licenses which changes the whole game. Permission Set Licenses are like a cross-play between a Managed Package License and a Permission Set. When setting up a Permission Set License you can grant both access to the Package AND permissions related to the Package all at once.

Let's use Field Lightning Service as an example; when you go to a user record and click Edit Assignments on the Permission Set Licenses, you will see that you have a list of Licenses and the permissions that are included with those licenses.

<img src="/images/image-1.png" alt="">

Additionally, you can create these combos on your own, enabling you to provide the permissions and licensing with quick ease. Simply go to create a Permission Set, and at the bottom in the License selection, you will now see in the drop-down the ability to select any of the applications that support this License feature (not all App Exchange packages support this at the time of writing).

<img src="/images/image-2.png" alt="">

That's it, that is the difference between a Managed Package license and a Permission Set License.
