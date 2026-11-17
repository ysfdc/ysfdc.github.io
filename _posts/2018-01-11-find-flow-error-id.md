---
title: "How to find which flow caused an error?"
date: 2018-01-11
categories: 
  - "tips-tricks"
---

Have you ever gotten an email or seen the screen with the error:

_The record couldn't be saved because it failed to trigger a flow. A flow trigger failed to execute the flow with version ID XXXXXXXXXXXXXXX. Contact your administrator for help._

Then, like any good admin, you try to put the id in the URL to see where it goes and you get absolutely nothing useful from it? Well, thanks to the Salesforce community I have learned that there is a "magic URL" that allows you to access that ID and see exactly which Flow (or Process Builder) caused the issue.

The URL is:

_**hxxps://xxx.my.salesforce.com/designer/designer.apex#Id=\[place the ID here\]**_

It's not over yet, though! You need to keep refreshing the page until you see the flow designer page and you see a spinning wheel. Then, take 30 seconds to relax while the page finishes loading.

Viola! You can see the flow that caused the error and dig into what happened. This is especially useful if it was a Process Builder that caused the problem because you are now behind the scenes of the usual GUI and can more easily figure out what is causing the error.
