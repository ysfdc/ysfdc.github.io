---
title: "Summer '23 Release Review"
date: 2023-06-20
categories: 
  - "admin-life"
---

It is hot up here in the Pacific Northwest so I guess that means it's time for our Summer Release update. This month's list is huge so I broke this into sections so hopefully you can find what interests you.

## All of the Permissions and Security

- Add some [security](https://help.salesforce.com/s/articleView?id=release-notes.rn_experiences_files_publiclinksecurity.htm&release=244&type=5) to your file that you share publicly.

- Adding a new field? Now you can set the [FLS on a permission set](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_field_security_perm_set.htm&release=244&type=5) instead of a profile.

- [Restrict who can select org wide addresses](<http://restrict who can select org wide addresses when sending email from salesforce: https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_productivity_email_owea_permission_sets.htm&release=244&type=5>) when sending emails from Salesforce.

- Time to give those delegated admins some more power. Now they can help [manage permission set groups](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_delegated_psg.htm&release=244&type=5) too.

- We are getting closer to coming to GA on the [User Access Policies](https://help.salesforce.com/s/articleView?id=release-notes.rn_permissions_user_access_policies_beta.htm&release=244&type=5). Now moving into a Beta for all users. Previously, Salesforce enabled user access policies, but now you can enable this beta feature on the User Management Settings Setup page.

- You can now upgrade your [speed for resharing calculation on accounts](<http://faster account resharing calculation, need to contact salesforce:https://help.salesforce.com/s/articleView?id=release-notes.rn_sharing_opportunity_child_sharing.htm&release=244&type=5>). Please contact Salesforce for more details.

## Did Someone say Lightning Speed? Here are some general Lightning and page updates:

- [Keep Working with Tab-Focused Dialogs (Release Update)](https://help.salesforce.com/s/articleView?id=release-notes.rn_console_dialogs.htm&language=en_US&release=244&type=5)  
    This release update has been postponed indefinitely and not enforced in its present form. Don’t enable it.

- Want to [undo those field changes](https://help.salesforce.com/s/articleView?id=release-notes.rn_general_unsaved_changes.htm&release=244&type=5)? Well, now you can!

- Time for f[aster loading related lists](https://help.salesforce.com/s/articleView?id=release-notes.rn_related_list_view_all_lwc.htm&release=244&type=5).

- That [News tab](https://help.salesforce.com/s/articleView?id=release-notes.rn_related_list_view_all_lwc.htm&release=244&type=5) you didn't know what to do with it, well it's taking its final bow - News is being retired and the tab going away.

- For those with alignment OCD, [horizontal field alignment](https://help.salesforce.com/s/articleView?id=release-notes.rn_lab_df_field_section_enhancements.htm&release=244&type=5) is here to help.

## Random things

- Very cool - [Mass Quick Actions](https://help.salesforce.com/s/articleView?id=release-notes.rn_customization_general_related_list_quick_actions.htm&release=244&type=5) directly in the Related Lists tab.

- If you have CPQ+ (my understanding of the documentation), you can now create [Quote Templates in OmniStudio](https://help.salesforce.com/s/articleView?id=release-notes.rn_revenue_cpq_omnistudio_doc_gen.htm&release=244&type=5) Document generation - similar to other Word based templates.

- More configuration of [opportunity splits](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_features_core_split_revenue_by_product.htm&release=244&type=5), you can now split by product.

- If you have a console app you can [easily access calendar](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_productivity_calendar_from_DAC.htm&release=244&type=5) with a single popup.

- [Automated emails](https://help.salesforce.com/s/articleView?id=release-notes.rn_sales_productivity_email_owea_autoproc.htm&release=244&type=5) are now going to require the use of a verified org wide address

- Finally, picklists will be [searchable](https://help.salesforce.com/s/articleView?id=release-notes.rn_search_searchable_picklist.htm&release=244&type=5) (pilot).

## So many flow updates:

- Build [reactivate screen flows](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_reactive_screens_beta.htm&release=244&type=5) and use fewer screens.

- [Recalculate screen flow logic](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_reactive_formulas_beta.htm&release=244&type=5) if a formula on that screen changes.

- Send salesforce [data externally](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_http_callout_post.htm&release=244&type=5) without code.

- Track your [outbound email](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_log_emails_sent_using_the_flow_builder_send_email_action.htm&release=244&type=5) in the activity feed when sent from a flow.

- Directly use [email templates in a flow](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_use_email_templates_in_the_send_email_action.htm&release=244&type=5), so long email alerts!

- See more on the [canvas with higher contrast](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_builder_see_more_elements_on_the_flow_builder_canvas.htm&release=244&type=5).

- See Salesforce shipped flows (ones that were previously hidden) in the [order of flows](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_trigger_explorer_standard_flows.htm&release=244&type=5) to work around them. No, you cannot change their order.

- That's all folks - [Process Builders](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_mgmt_block_process_builder.htm&release=244&type=5) can no longer be created anew.

- Not sure what second generation means, but sounds like we can minimize the flows we need from [managed packages](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_mgmt_2gp_delete.htm&release=244&type=5)/ maybe delete them?

- Flows have their own [permissions section](https://help.salesforce.com/s/articleView?id=release-notes.rn_automate_flow_mgmt_find_flow_user_permissions_more_easily.htm&release=244&type=5) now on the app permissions page.

## Cases:

- Directly link [contacts to an email](https://help.salesforce.com/s/articleView?id=release-notes.rn_service_email_link_contacts.htm&release=244&type=5) from email2case easily.

- Adjust [components of an email](https://help.salesforce.com/s/articleView?id=release-notes.rn_service_email_user_perm.htm&release=244&type=5) like additional email addresses through automation.

- Move to the [new email threading](https://help.salesforce.com/s/articleView?id=release-notes.rn_service_email_disable_refid_release_update.htm&release=244&type=5) (because Salesforce decided we can't have nice things).

- Configure no-reply emails that can be used to [send support emails](https://help.salesforce.com/s/articleView?id=release-notes.rn_case_email_notification_owa.htm&release=244&type=5).
