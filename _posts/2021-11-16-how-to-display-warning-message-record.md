---
title: "How to display a warning message on a record"
date: 2021-11-16
categories: 
  - "lightning"
  - "tips-tricks"
---

The requirement is to display a warning message on the top of a record. The message should only display if the record contains certain information. In the days of old, and by the I mean Classic, Visualforce was usually required to make a nice banner that sat on the page and could be dynamic. Today, in Lightning, code is no longer needed to complete such a task, as you can do it entirely with components and filters.

1. On the relevant Lightning Record page, add the Rich Text component  
    

<img src="/images/2021-10-30_11-07-44-2.png" alt="">

2\. On the right-hand side fill in the Rich Text Editor with the message you want to display  

<img src="/images/2021-10-30_11-09-04.png" alt="">

3\. Underneath the message section, you can set up the component filter. For example, I am setting it up to display based on Case Reason.  

<img src="/images/2021-10-30_11-10-06-1.png" alt="">

<img src="/images/2021-10-30_11-10-27.png" alt="">

4\. After you have finished setting that up, save the page, and make sure it is Activated. Then go test it out!  

<img src="/images/2021-10-30_11-12-07-1.png" alt="">
