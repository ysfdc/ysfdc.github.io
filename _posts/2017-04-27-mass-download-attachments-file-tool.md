---
title: "Mass Download Attachments (Tool)"
date: 2017-04-27
categories: 
  - "admin-life"
  - "tips-tricks"
---

As many of you are aware, shortly (winter '18) [Salesforce will require](https://releasenotes.docs.salesforce.com/en-us/spring17/release-notes/rn_files_add_related_list_to_page_layouts.htm) all of its users to use Files as they are phasing out Attachments and Notes. While Salesforce is doing a nice job of releasing [a tool](https://releasenotes.docs.salesforce.com/en-us/summer17/release-notes/rn_files_attachments_to_files.htm) in Summer '17 to handle conversion of Attachments to Files, they still have not handled how to mass download all attachments from the system. This may be important to your org before going through the conversion process (or for any other reason). I know it is for mine.

My business case is actually two-fold:

1. I need to get all of the attachments into a safe place before we do the conversion
2. I need to get all of a specific type of attachment downloaded so that it can be uploaded elsewhere

While Salesforce does provide admins with the [Data Export tool](https://help.salesforce.com/articleView?id=admin_exportdata.htm&type=0), the tool itself has a significant number of limitations. First and foremost, you can only run it once a week. Second, it downloads the files without the extensions and without the attachment name, essentially rendering them useless (at least for me). Lastly, you have zero control over which attachments are downloaded. In fact, since it is just a single checkbox option, you will get stuck downloading all attachments, documents, and files and that could lead to more headaches than anyone cares to deal with.

So with all of that said, I wrote up a nice design spec explaining what I was looking for and handed it off to my partner, who translated my design spec into a Python utility, and which is now available for all on GitHub.

The script is relatively straightforward. It goes through all of the attachments and downloads them to your local computer. The tool preserves the original filename and prefixes it with its Attachment ID. For my second business use case, I only needed attachments that were on Accounts, so an extra option exists to download _Accounts Only_ attachments (by default it will download ALL attachments). As a bonus, there's an option to ignore file names that contain certain keywords.

The script also creates a CSV file that maps the Parent ID to the attachment filename, so you could easily tell which file is associated with which account.

How to use the script:

1. Make sure you have Python and [pip](https://pip.pypa.io/en/stable/installing/) installed
2. Install simple-salesforce and requests
    - `$ pip install simple-salesforce`
    - `$ pip install requests`
3. [Download](https://github.com/ysfdc/salesforce_scripts/blob/master/attachments_downloader.py) the tool from GitHub
4. Open your CLI (Terminal/CMD) and run the following line:
    - `$ attachments_downloader.py -u [SFDC username] -p [SFDC password] -t [SFDC token] -s [Path to Store Attachments]`
5. _(Optional)_ If you want to download attachments belonging to Account only:
    - `$ attachments_downloader.py -u [SFDC username] -p [SFDC password] -t [SFDC token] -s [Path to Store Attachments] --account-only`
6. (_Optional_) If you want to skip certain attachments:
    - `$ attachments_downloader.py -u [SFDC username] -p [SFDC password] -t [SFDC token] -s [Path to Store Attachments] --ignore WORD1 WORD2 ...`

Here's a real-world example:

`$ attachments_downloader.py -u sf9to5@example.com -p password -t sf9to5_super_secret_token -s /tmp/ --account-only --ignore photo demo upload`

The command line above will download all attachments that belong to Account only and will skip any files which contain "photo", "demo" or "upload" in their name.

Troubleshooting:

- We tested it on Windows and macOS (Sierra) only (should work on Linux too)
- Ensure your macOS has the most recent OpenSSL library (use brew to upgrade) and that Python uses the most recent OpenSSL library. This is required for the tool to talk TLS with Salesforce
- Works on Production environments only
- Of course, make sure your user has the right permissions :)

Link to Mass Attachments Downloader tool:

[https://github.com/ysfdc/salesforce\_scripts/blob/master/attachments\_downloader.py](https://github.com/ysfdc/salesforce_scripts/blob/master/attachments_downloader.py)

I would love to get your feedback on whether you find this useful and if you have any questions. Thanks!
