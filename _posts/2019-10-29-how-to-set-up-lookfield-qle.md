---
title: "How to set up a Lookfield for the QLE"
date: 2019-10-29
categories: 
  - "cpq"
  - "tips-tricks"
---

Recently I was asked about adding a Lookup field on a Quote Line to be filled in on the Quote Line Editor. As a result, I learned something new about the backend of CPQ. There is a special way to adjust what fields show up in the Lookup filter view and how to set it up.

So let's dive into an example. Say I have a Case Lookup field that I have added to my Quote Line and the Line Editor fieldset. ![2019-10-05\_16-45-36](/images/2019-10-05_16-45-36.png)

The first time you click on the Lookup field from the Quote Line you are going to get some sort of error. This particular time I got this one: ![2019-10-05\_16-48-38](/images/2019-10-05_16-48-38.png)

Previously I had received an error that had more explanation as to what to do next, but I cannot seem to regenerate that message.

The reason you get the error is that you need to create a separate Field Set specifically for CPQ on the Object that you are looking up to. In my case, its Case. To create the Field Set, go to the Lookup Object, Case, and create a new Field Set called the "CPQ\_Lookup". It must be that exact name in order for this to work.

![2019-10-05\_16-54-09](/images/2019-10-05_16-54-09.png)![2019-10-05\_16-54-31](/images/2019-10-05_16-54-31.png)

After you create the Field Set you are ready to give it a try!

![2019-10-05\_16-56-54](/images/2019-10-05_16-56-54.png)![2019-10-05\_17-26-19](/images/2019-10-05_17-26-19.png)
