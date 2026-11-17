---
title: "Why won't my Quick Action show in Lightning?"
date: 2019-02-26
categories: 
  - "admin-life"
  - "lightning"
  - "tips-tricks"
---

So you have a Quick Action that you want to add to either the Activity tab (if you on any Object but Cases) or on the Chatter tab (if you are on the Cases object). You have added it to the layout and clicked refresh and go to check out the new Quick Action, but you look and see it isn't there? You refresh a couple times and go back to look at the setup of the layout, you see it plain as day on the backend, but still no luck on the front end.

Well, there are three four things you can try to get that pesky Quick Action to show on the layout.

1. Make sure that what you added to the layout is actually a Quick Action and double check that you are adding it to the Salesforce Lightning and Mobile Action section, not the Classic one.
2. Make sure that you or the user is viewing the page during testing has access to all of the relevant fields that and objects in use by that Quick Action.
3. If your Quick Action references an Object that has a Record Type, make sure that is also set. For example, if your Task Object has record types, and you try to add Log A Call and it doesn't show up, it is likely because the Log A Call Quick Action is still unassociated to any record type.
4. Refresh, refresh, refresh, clear cache, refresh. Maybe make the clear cache earlier, but you get the point. Because most of Lightning is built on the Client side rather than the Server side, you can end up with a cached version of the page layout, which means, even though you made the updates and they should be working, you just simply aren't seeing them because of a caching issue.

If all of the above fails you, try reviewing some of the documentation on Lightning Quick Actions. Much like my comment at the beginning of this calling Cases out separately, Lightning still has some weird quirks when it comes to Quick Action and you may just need to sniff it out.

If you do find another reason why the Quick Action isn't showing on your Lightning page, please comment below and I will happily update this post.
