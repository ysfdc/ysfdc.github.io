---
title: "The Classic Side of Winter '19 release"
date: 2018-09-18
categories: 
  - "admin-life"
---

This has become a bit of a thing that I do when a new release comes out. It seems that most folks focus on the Lightning side of the release notes, which makes sense since the majority of the new features are geared that way. However, there are still so many companies out there that are using Classic that I want to dedicate a post to them to call out the features or relevant updates for those Classic folks.

This round of release notes seems to have brought more to call out than usual, so I hope you find this useful!

### Microsoft

- [Lightning for Outlook](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_outlook_integration_name.htm) in the Microsoft store is now going to be called [Salesforce Lightning for Outlook](https://appsource.microsoft.com/en-us/product/office/WA104379334?tab=Overview) and automatically will include the Inbox features for those who have a license.
- There are no [planned updates](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_sfo_bug_fixes_3.4.3.htm) for the old Salesforce for Outlook plugin. Salesforce is pushing for users to move over to Lightning for Outlook
- It has finally happened! Going forward [new users will NOT](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_sf_eosale.htm) be able to use Salesforce for Outlook.
    - If your users were using the downloadable plugin, but have not been using it regularly, they will NO longer be able to use it and the admin will not be able to create or edit the previous configuration.

### Service

- You will now be able to require a [ReCaptcha](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_cases_web_to_case_recaptcha_enforce.htm) on Web 2 Case. The is a measurement to help fight against spam getting into the system.

### Reporting

- [Dashboards](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_rd_dashboards_filters_more.htm) can now have up to 50 values per filter! This is an increase from the previous 10.

### Pardot

- If you have been dealing with GDPR and trying to update contacts or leads in Salesforce and wanting to [Opt them back in](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_pardot_opt_out_override.htm), then you have run into the mess that is the connection between the 2 systems to be able to achieve this. As a result, Salesforce has made a change that will allow you to update the Opt-In status for up to 100 prospects/ per day. The setting for this is in the Pardot portal.
- [Campaign members](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_features_core_campaigns_member_sync.htm) will now stay synced between Salesforce and Pardot. This process is now handled automatically where the records exist.

### Files

- [Quip](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_files_quip_quipcard_salesforce_classic.htm) can be integrated with Classic! Add Quip documents to most Salesforce standard and custom objects.

### Sales

- I believe the title says it all for these two items: [Filter Opportunity Reports by Territory](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_other_changes_territory_opportunity_report_filter.htm) and [Filter Opportunity List Views by Territory](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_sales_other_changes_territory_opportunity_list_view_filter.htm)

### Misc.

- If you have a Mac you can now Control + Click for [Multi-Page Layout assignment](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_forcecom_general_macos_cmd_click_pagelayout_assign.htm) selection
- [Duplicate Management](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_duplicate_individuals.htm) can be run now on the Individual Object
- In [Process Builder](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_forcecom_flow_design_num_processes.htm), you will now be informed if you have more than one process that is record changing for that object. This is to encourage a move towards a single record changing process per object similar to the [One Trigger per Object](http://www.sfdc99.com/2015/01/19/the-one-trigger-per-object-design-pattern/) methodology.
- While still in Pilot, you should hopefully soon be able to click ["Where is this Used?"](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_forcecom_fields_where.htm) at the field level in order to check the field reference, woohoo!
- You will now be able to reference your [Custom Metadata in Advance formula fields](https://releasenotes.docs.salesforce.com/en-us/winter19/release-notes/rn_forcecom_development_custom_metadata_types_ff.htm)
