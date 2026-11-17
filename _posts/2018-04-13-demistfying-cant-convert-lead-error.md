---
title: "Demistfying the Can't Convert Lead Error"
date: 2018-04-13
categories: 
  - "admin-life"
  - "tips-tricks"
---

Have you ever gotten this error message when trying to convert a lead?

_Error when converting: We can't convert this lead because some values are restricted on the contact, account, or opportunity_

The actual meaning behind this error is that there is a selected picklist value on the Lead record which is trying to map to a field on either a Contact, Account, or Opportunity, and those picklists do not have the value AND that the picklist in question has restricted values turned on.

Now, of course, the best way to solve this would be for Salesforce to include the field in the error message itself as is requested in this [idea post](https://success.salesforce.com/ideaView?id=0873A0000003XJ6QAM) (please vote by the way), however, this is not the case. As a workaround to this, I have taken the suggestion of the user who created the idea and expanded on it to include only the restricted picklist options.

```
Map<String, Schema.SObjectField> fieldMap = Schema.SObjectType.Lead.fields.getMap();

for (String field : fieldMap.keySet()) {
  if (fieldMap.get(field).getDescribe().getType() == Schema.DisplayType.PICKLIST 
      && fieldMap.get(field).getDescribe().isRestrictedPicklist()) { 
    system.debug(field); 
  }
}
```

This snippet of code will get you the list of restricted picklists on the Lead. You can easily modify it to give you the fields on the other three objects as well.

I have been able to use this a few times to reduce the amount of time spent looking for the field amongst many that could be causing the issue. I hope this helps you too!
