---
title: "Winter '24 Release- All my thoughts"
date: 2023-11-01
categories: 
  - "admin-life"
---

This release, my post may look different. I had a lot of thoughts, and there was a lot of content. It is sporadic, but I covered each item as its own block.

This is a strange addition, given we are now getting warnings about profiles being deprecated, but they have improved the configuration of [searchable objects based on user profiles](https://help.salesforce.com/s/articleView?id=release-notes.rn_search_manager_configuration.htm&release=246&type=5). This is currently in beta.

For anyone with some setup pages bookmarked, be weary as they may not continue to work as Salesforce is rolling out a [new domain for setup](https://help.salesforce.com/s/articleView?id=release-notes.rn_general_setup_domain_prepare.htm&release=246&type=5): .salesforce-setup.com. Also, make to allowlist if you think this might cause an issue for anyone.

Pretty sure I covered this before, but just a reminder: [News, Automated account fields, and Logos](https://help.salesforce.com/s/articleView?id=release-notes.rn_account_features_news_retirement.htm&release=246&type=5) are going away, and so is the connection to Twitter. Besides Twitter, this will not affect many.

Ok, so permissions are a big one in this round-up, and I will include everything I could find in the release notes because I think it's that important. Reminder: Spring '26 right now is the drop dead date for profiles, and while that seems far off, we will be dealing with it quickly, so get ready.

1. We can now [report on custom permission sets](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_perm_set_crt.htm&release=246&type=5), including which users are attached to which permission set. This is a custom report type, so you will need to do some build to run the report.

3. This one is a godsend, as I cannot think of the number of times I have been asked what permissions are turned on in a permission set. Welcome the ability to [see what is enabled in your permission set](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_summary_beta.htm&release=246&type=5) - currently in beta, but who cares! I have already tested this out in a sandbox, and man, does this save time.

5. I'll be honest I am not sure I understand the purpose behind this one, but maybe with time, it will make sense. They have added a [recalculate button to the permission set groups](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_group_troubleshoot.htm&release=246&type=5) to help with failures.

7. What feels like 400 years later and probably several different Chrome plugins, Salesforce finally allows us to see the [API names of fields in the permission set](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_api_name.htm&release=246&type=5). I wish this was also coming to profiles so we could better understand as we migrate, but I will still take it.

9. Assuming you have permission set groups with a whole bunch of permission sets attached to them, this will be helpful to you. You can now see the [count of permission sets included in a group](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_group_count.htm&release=246&type=5).

11. Count limitations have been increased on the number of things you can filter a user by when assigning through the [User Access Policies](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_user_access_policy_filters.htm&release=246&type=5) that Salesforce previously introduced. This is still in beta, but I think it is now public.

Dynamic forms got another update in this release. Any object that is LWC enabled can now be [converted to a dynamic form](https://help.salesforce.com/s/articleView?id=release-notes.rn_dynamic_forms_standard_objects.htm&release=246&type=5). This includes standard objects. There are only a handful of objects left that do not meet this. Also included are [mobile users](https://help.salesforce.com/s/articleView?id=release-notes.rn_dynamic_forms_on_mobile_ga.htm&release=246&type=5), who can now appreciate the wonders dynamic forms offer. Something else that goes well with this is the ability to [add Mass Quick Action buttons to related lists](https://help.salesforce.com/s/articleView?id=release-notes.rn_customization_general_related_list_quick_actions_ga.htm&release=246&type=5), allowing a user to update multiple records at once.

I doubt some people get excited about sharing updates, but we got two goodies in this update. We got the ability to finally [report on who has access to an account](https://help.salesforce.com/s/articleView?id=release-notes.rn_sharing_crt_accountshare.htm&release=246&type=5) through a new custom report type and be able to [run reports on public groups](https://help.salesforce.com/s/articleView?id=release-notes.rn_sharing_crt_group_membership.htm&release=246&type=5) (this one will be essential for a later post).

Another who did what where update that I am very interested in is [Audit History on Opportunities](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_opportunity_audit_history.htm&release=246&type=5). This allows you to see changes in Opportunity Splits and Opportunity Team members. I am hoping this will save some people headaches in the future.

A somewhat confusing update, based on the title vs. what it says in the subscription combined with little information provided, is that [Web Quote Line functionality and Web Quote document functionality are being deprecated](https://help.salesforce.com/s/articleView?id=release-notes.rn_revenue_cpq_edit_generate_web_quote_retirement.htm&release=246&type=5). I did some additional digging on this and found a trailhead [community post](https://trailhead.salesforce.com/trailblazer-community/feed/0D54S00000A8eOMSAZ) where Salesforce says that Web Quotes no longer serve the value they used to. It might be time to move away if you are still using it.

In other sorts of CPQ news, there is a [new behavior on Order](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_new_order_save_behavior.htm&release=246&type=5) when saved. This new behavior checks to ensure that if a child record (order product) is updated and impact should happen on the parent record, the behavior goes through.

A nifty sales tool coming out in this release called Intelligence View applies to both [Contacts](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_contacts_intelligence_view.htm&release=246&type=5) and [Leads](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_leads_intelligence_view.htm&release=246&type=5). It provides a home base for each object and allows reps to see everything in a dashboard-like form, leveraging the activities as the baseline. I have yet to learn about the customization options, but it looks interesting from the high level.

There have been several updates in the forecasting world, including a [refreshed UI for the home page](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_ui_enhancements.htm&release=246&type=5). There is also an update directed to [managers](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_manager_judgments.htm&release=246&type=5), allowing them to decide on an opportunity-by-opportunity basis whether it should be in or out. General forecast users also get an update, where now, in the r[ollup view, more details](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_forecasts_opportunity_list.htm&release=246&type=5) are available on hover - allowing you to see what you need to quicker.

I swear, every time I write one of these posts now, Flow is the winner of the most updates, which is not any less accurate with this release.

1. [Reactive screen flows](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_build_screen_flows_with_reactive_components_generally_available.htm&release=246&type=5) - there are too many updates here to go through them all (this post is already long). Conceptually, though, this concept is fantastic.

3. No [more ugly error messages](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_create_custom_error_messages_in_record_triggered_flows.htm&release=246&type=5) that users do not know what to do with. Now, you can create custom error messages!

5. You can now do [HTTP callouts directly from a flow](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_http_callout_post.htm&release=246&type=5). No code is needed, how about that for click-not-code.

7. [Transform your data from one object to another](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_transform.htm&release=246&type=5) - while they don't say this, I feel like this is the type of mapping we get when converting a lead, and now we can have it anywhere.

9. One step closer to the concept of [Draft in Flow](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_save_a_flow_without_configuring_some_elements.htm&release=246&type=5), so we can save and come back later like most humans have to.

11. Flow Trigger Explorer gets some nifty [search filter](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_trigger_explorer_quickly_find_record_triggered_flows_using_filters.htm&release=246&type=5) options.
