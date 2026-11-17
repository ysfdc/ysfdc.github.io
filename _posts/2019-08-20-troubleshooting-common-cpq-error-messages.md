---
title: "Troubleshooting Common CPQ Error Messages"
date: 2019-08-20
categories: 
  - "cpq"
  - "development"
  - "tips-tricks"
---

We've all seen it, the random message that shows at the top of a CPQ Quote without any rhyme or a reason, at least not at the front of mind. I have compiled a list of common error messages and their troubleshooting steps, along with the relevant articles from Salesforce, in order to provide some clarity to these errors.

- **Could not calculate quote prices. This quote is now in an invalid state. Recalculate your quote to render it**
    - This is a generic error message that CPQ throws, potentially as a result of trying to sync/fire the CPQ triggers
    - Salesforce recommends three different ways of troubleshooting:
        - Option 1: Try to trigger from the Quote directly, not from the QLE, a calculation to fire. You can do this by editing any field that is part of the calculation process. Hopefully, this will result in a less generic error message and lead to the right place to fix it.
        - Option 2: You can try to run a query on the Quote Id to pull the Job ID that will lead you potentially to the APEX job that failed and caused the error. You can then do additional troubleshooting from there.
        - Option 3: Try recalculating from the QLE, either this will trigger a new error, possibly more detailed, or it might resolve the issue altogether.
    - [https://help.salesforce.com/articleView?id=000314558&type=1&mode=1](https://help.salesforce.com/articleView?id=000314558&type=1&mode=1)
- **Cannot create quote document. The quote is in an invalid state and pricing may be incorrect. Recalculate your quote to render it valid.**
    - Repeat the steps listed in the previous error message. Because this error states the Quote is in an invalid state, you likely need to recalculate it (option 3) to get it to behave correctly.
    - Following Option 2 from above may be able to get your more detail to potentially prevent the error from happening again.
- **Value not of Required Type:**
    - This error is typically found in the QLE when trying to save. It is a result of having a checkbox that is part of a Price Action that has been improperly set or is used a reference field in a QCP script
    - For Price Actions, Salesforce recommends changing the event on which the Price Rule actions from OnIntialization to anything else
        - [https://success.salesforce.com/issues\_view?id=a1p3A000000JWeRQAW](https://success.salesforce.com/issues_view?id=a1p3A000000JWeRQAW)
    - For using a checkbox as a reference field in a QCP script, Salesforce recommends creating a Referenced Fieldset and adding the checkbox to it.
        - Info on Referenced Fields: [https://help.salesforce.com/articleView?id=000314407&type=1&mode=1](https://help.salesforce.com/articleView?id=000314407&type=1&mode=1)
        - [https://success.salesforce.com/issues\_view?id=a1p3A000000FmjHQAS](https://success.salesforce.com/issues_view?id=a1p3A000000FmjHQAS)
- **Price Rule \[ID: XXX\] : multiple results returned from query. Please contact your Salesforce CPQ administrator.**
    - This error is caused when you have Price Rules firing that use Lookup records. If you have duplicated entries in your Lookup records, then this error will appear.
    - The solution to this is to find the Lookup record in question based on the ID and then find any duplicates of it. Deleting the duplicates should resolve the error.
    - [https://help.salesforce.com/articleView?id=000319066&language=en\_US&type=1&mode=1](https://help.salesforce.com/articleView?id=000319066&language=en_US&type=1&mode=1)

I hope you find the above information to be a helpful reference!
