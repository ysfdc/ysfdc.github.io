---
title: "The Classic side of Spring '19 Release"
date: 2019-01-15
categories: 
  - "admin-life"
  - "cpq"
  - "development"
  - "lightning"
---

Wow, Spring '19 is already here, although, it does not look like Spring outside my window as I write this. I think this release really comes packing a punch, especially to those still living comfortably in the Classic world. As of 2020, we Classic users are going to be hit with some pretty big changes that will require preparation. So without further ado, let's dive into the Classic side of the Spring '19 release notes.

## Changes coming in 2020

1. [Lightning will be turned on for EVERYONE](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_cruc_lex_turned_on.htm) - I repeat, Lightning will be turned on for Everyone. You will still be able to switch back to Classic, but if your users haven't seen it before, this is the time to start thinking about the shock they may get one morning when it just appears.
2. In 2020 [Customizable Forecasting](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_other_changes_customizable_forecasting_retirement.htm) is being retired and by this I mean, it is going away for good and you will lose the data and access to the functionality. Start your planning now if you are still using this functionality. Recommended by Salesforce is to move over to Collaborative Forecasting.
3. Also going away for good in 2020 is the [Original Territory Management](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_other_changes_territory_management_retirement.htm) setup. If you are still using this functionality, the recommendation is to move to Enterprise Territory Management. Updates are constantly being made to this. Read on for more info on that.

## Updates to [Enterprise Territory Management](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_sharing_territory.htm)

These updates primarily focus on the sharing capabilities within the Territory Management structure

1. Users can now share records across a [single Territory](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_features_core_territory_management_sharing_manual.htm) opening it up beyond the org-wide settings
2. You can [grant access to records, reports, list views](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_features_core_territory_management_sharing_rules.htm), etc. through Territories
3. Add reps to [Groups and Queues](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_features_core_territory_management_groups_queues.htm) using the Territory structure

[Collaborative Forecasting](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_features_core_forecast_range_expanded.htm) has increased its overall month count to up to 15 months of viewing and the ability to create a custom fiscal period.

## Files

1. The ability to [Query all Files](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_files_query_all_files.htm) is finally here! You need View All and the Query All Files permission
2. Anyone with access to an [Event (Activity)](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_productivity_calendar_related_files.htm) can now see the Files related to that event.

## Field Auditing

1. You can now set tracking on more objects and their [retention policy](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_security_fat_supported_objects.htm) for certain objects can now be set up to 10 years
2. [Where is this Field Used](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_fields_where.htm) is now in Beta (moved from Pilot in the last release)
3. [Field Type conversion](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_change_event_field_conversion.htm) where data loss can happen will now be tracked with a change or gap event

## CPQ & Billing

1. You can now [download the PDF directly](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_cpq_other_changes_download_docpdf.htm) from the Preview page
2. Ability to pull in [Amendment items](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_cpq_amend_subs_button.htm) from other Quotes on the Account directly into the Quote Line Editor when making an Amendment
3. [Price Usage with Consumption based schedules](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_cpq_cons_parent_ga.htm) will now be generally available in the Spring '19 release
4. The ability to i[nvoice on Evergreen subscriptions](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_billing_invoice_evergreen.htm) without having an End Date for the Subscription

## Sandbox and Deployment

1. The [email address](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sandboxes_email_management.htm) will be modified to be more simple when a sandbox is refreshed. It will just be modified to have .invalid at the end
2. We can now [Clone Sandboxes](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sandboxes_cloning_ga.htm), yay!!!
3. The number of [clicks to deploy a changeset](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_deployment_change_sets_fewer_clicks.htm) has shrunk. We can now Validate and Deploy from the Inbound changeset page

## Flows

1. You can now [schedule an action to happen immediately](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_flow_actions_in_hour.htm). Meaning you can set the time to zero so it acts as a separate action, but it will happen as soon as the next spot in the queue.
2. [FLOW BUILDER](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_flow_flow_builder.htm) - updated, new and improved, with no Adobe Flash required
3. You can now [act upon Salesforce Errors](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_flow_respond_to_sf_errors.htm) from within a Process or a Flow using the Platform events
4. When there is a NULL value and it triggers a Flow error, the error will actually now say NULL value instead of the sometimes inconspicuous Unhandled error

## Miscellaneous

1. You can create a [Follow-Up event with just one click](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_productivity_activities_tasks_follow_up_event.htm) from the event and the data will pre-populate from the original event
2. Finally, you can create a [report on Topics](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_chatter_feeds_topic_reports.htm) and include the content of the posts themselves
3. The ability to [log an email against someone who isn't on the email](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_sales_outlook_integration_other_who.htm) for both Outlook and Gmail
4. Sharing ability for [Multiple Accounts to Single Contact](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_networks_sharing_sets_contacts_multiple.htm) for Communities/Partner Portal
5. You can now set a [default field value](https://releasenotes.docs.salesforce.com/en-us/spring19/release-notes/rn_forcecom_development_custom_metadata_types_default_vals.htm) of a Custom Metadata field
