---
title: "Winter '25 Release - Is this the End?"
date: 2024-10-14
categories: 
  - "admin-life"
---

Before I jump into my usual list of things I found excellent or valuable in this release cycle, I wanted to discuss the elephant in the room. In the Spring '24 release notes, it was evident that Revenue Cloud was missing, with no updates to share. In the Summer '24 release notes I didn't cover this year, Revenue Cloud was back with the start of the Revenue Lifecycle Management (RLM) and some updates to Subscription Management and Billing. The RLM updates at the time did not fully show how much of an overtake this was going to be to CPQ, however I feel with the Winter '25 release notes this becomes very obvious.

So why am I saying, is this the end? Well, I have heard that we will no longer receive updates on CPQ as Salesforce moves into life support and focuses on its new baby, which is RLM. I won't be delving into RLM on my site for several reasons. 1) I do not have access to it in any way, shape, or form, as there are no dev orgs or playgrounds with it. 2) The work I have been doing doesn't use RLM, so I would be missing the real-world scenarios. I highly recommend checking out Neocol's blog or others focusing on this as Salesforce shifts. While Salesforce has acknowledged that they are not forcing companies to migrate over, RLM is what is being pushed to new customers rather than CPQ. I will also note that moving from CPQ to RLM is a migration and a new implementation; there is no quick and easy lift and shift process. On that note, here is the link to the Revenue Cloud release notes: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_revenue.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_revenue.htm&release=252&type=5)

Alright, now to jump into the more usual updates:

**Forecasting**—This has seemingly been getting a lot of attention, presumably to draw competition away from the likes of Clari. If you were previously cautious about using native forecasting, I would highly recommend reviewing what has come out in this update and the last.

Capture forecasting information PIT (point in time) - something that conceptually has not been possible before in SFDC: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_sales\_forecasts\_submissions.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_submissions.htm&release=252&type=5)

Want managers to make different judgment calls from the reps? Well, now you can: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_sales\_forecasts\_judgment\_enhancements.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_judgment_enhancements.htm&release=252&type=5)

I am not sure how this didn't exist before. See your opportunity splits by territory when looking at forecasts: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_sales\_forecasts\_opportunity\_splits\_territory.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_opportunity_splits_territory.htm&release=252&type=5)

**Flows** - the item that seems to have a never-ending list of updates while also inundating admins with more work

Find things more efficiently while building:

- Children resources [https://help.salesforce.com/s/articleView?id=release-notes.rn\_automate\_flow\_builder\_find\_flow\_child\_resources\_more\_easily.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_find_flow_child_resources_more_easily.htm&release=252&type=5)

- Resource variables: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_automate\_flow\_builder\_find\_flow\_child\_resources\_more\_easily.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_find_flow_child_resources_more_easily.htm&release=252&type=5)

Probably my favorite flow update; get help on whether you are making a good flow or not so you don't blow things up: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_automate\_flow\_builder\_loop\_tips.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_loop_tips.htm&release=252&type=5)

Another Einstein trick, get help with formulas in flow builder: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_automate\_flow\_builder\_get\_help\_creating\_flow\_formulas\_with\_einstein\_beta.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_get_help_creating_flow_formulas_with_einstein_beta.htm&release=252&type=5)

The create node can now also update: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_automate\_flow\_builder\_upsert.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_upsert.htm&release=252&type=5)

**Permissions** - Slowly, I see Salesforce unraveling what is left of the Classic UI in the backend, and Permissions is definitely one of those areas.

See why or how someone has a particular permission: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_permissions\_granted\_by.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_granted_by.htm&release=252&type=5)

See why or how someone has access to a particular object: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_permissions\_object\_summary.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_object_summary.htm&release=252&type=5)

Updated UI for public group management: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_manage\_public\_group\_membership.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_manage_public_group_membership.htm&release=252&type=5)

User UI is updated to now have a summary section and an access section: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_customization\_general\_user\_detail.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_customization_general_user_detail.htm&release=252&type=5)

**Critical Updates** - these are things you need to take care of whether you want to or not.

- Update domain list: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_general\_allow\_setup\_domain.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_general_allow_setup_domain.htm&release=252&type=5)

- Verify your no-reply email: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_general\_verify\_return\_email\_address.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_general_verify_return_email_address.htm&release=252&type=5)

- Verify your return address email: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_general\_verify\_your\_return\_email\_address\_for\_senders.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_general_verify_your_return_email_address_for_senders.htm&release=252&type=5)

**Lightning Updates** - just a couple other things I found useful

Fields on a record page can now have conditional formatting, including icons (please don't go overboard with emojis): [https://help.salesforce.com/s/articleView?id=release-notes.rn\_lab\_conditional\_field\_formatting.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_lab_conditional_field_formatting.htm&release=252&type=5)

The highlights panel at the top is now also dynamic: [https://help.salesforce.com/s/articleView?id=release-notes.rn\_lab\_dynamic\_highlights\_panel.htm&release=252&type=5](https://help.salesforce.com/s/articleView?id=release-notes.rn_lab_dynamic_highlights_panel.htm&release=252&type=5)
