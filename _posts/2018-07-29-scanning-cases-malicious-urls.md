---
title: "Scanning Cases for Malicious URLs"
date: 2018-07-29
categories: 
  - "development"
---

One of the biggest cybersecurity threats around today is the existence of phishing, malware or spear phishing URLs. Phishing URLs are URLs that look legitimate but are actually malicious in their intent and designed to steal critical personal information (e.g. login credentials to your corporate account).

Within the Salesforce universe, there is a critical point in which users can be susceptible to this type of threat and that is in the [Email to Case creation](http://sf9to5.wordpress.com/2017/08/02/how-to-setup-email-to-case-gmail/). Cases come into Salesforce from the external world, supposedly from customers, but potentially from folks with malicious intent pretending to be customers. In these cases, the external user can provide a link to something they may indicate as benign but in actuality could contain malware or lead to a phishing site.

Introducing [CaseURLScanner](https://github.com/ysfdc/CaseURLScanner). The goal of this project was to provide a way to protect Salesforce users from accidentally falling for one of these phishing links.  I have chosen to use VirusTotal's Public API, as they are one of the largest databases of known malicious (phishing or otherwise) URLs. However, this project can be expanded to work with other databases out there that provide the same scanning mechanism and API.

## The Setup and Design

In order for this project to work, there was some initial foundational work that had to be done. I wanted to ensure that users are only exposed to cases that had been scanned and deemed clean, while also completely removing from view any case that may contain a malicious URL. To achieve this logic I implemented the following point and click functionality into Salesforce:

1. I created a field on the Case called Bypass Assignment Rule 1. This is a Boolean field, default is off.
2. I created 3 queues to be used throughout this project:
    1. Holding Queue - this is where all cases will go before being seen by the user until processed by the API
    2. General Queue - this is where normal cases will go after being processed and found clean of any malicious URLs
    3. No Man's Queue - this is where cases with potentially malicious URLs go to live (this can be used to determine if the case should be deleted or otherwise handled)
3. I created 2 assignment rules (this way will vary highly based on your org, but the first rule is critical in preventing users access to the Case before it has been scanned)
    1. The first rule has Bypass Assignment Rule 1 set to False and assigns the Case to the Holding Queue
    2. The second rule has Bypass Assignment Rule 1 set to True and assigns the Case to the General Queue - this is just for the purpose of this project. You may have many rules that the Case could go to if it is found clean. The classes for this project have kept that in mind and simply send the case back through the assignment you have at the end if deemed clean.

Once this foundational logic is in place than the following set of classes and trigger will work to allow your users to only see clean cases.

_**Control Flow**_

![ControlDiagram](/images/controldiagram.png)

The above image represents the flow of the following Trigger and Classes. It shows the flow from the start of generating a case through to the end of either going through the Assignment rules again or ending in the No Man's Queue.

A couple items about VirusTotal before jumping into the classes:

- This code has been made to accommodate the Public API and only passes a single URL at a time. If you have the Private API, you can modifications to the scanURLs class to handle this.
- VirusTotal has a number of different APIs, including the ability to scan and report on new URLs in addition to searching for URLs that have already been reported. This project only uses the [reported URL API](https://developers.virustotal.com/v2.0/reference#url-report).
- For more information about the VirusTotal APIs please visit here: [https://developers.virustotal.com/v2.0/reference#getting-started](https://developers.virustotal.com/v2.0/reference#getting-started)

Github Project: [https://github.com/ysfdc/CaseURLScanner](https://github.com/ysfdc/CaseURLScanner)

_**CaseTriggerHandler**_

For each new case that is created (irrelevant of how it is created), it will flow through this class. In this class, there is a call out to the _extractURLs_ class to check to see if there are any URLs in the description field of the case (this also represents the body of the email). If no URLs are found, the case is immediately sent back through to the Assignment Rules. If a URL is found, the _scanURLs_ class is called.

_**extractURLs**_

This class uses a regular expression to parse through the text to see if anything matches the format of a URL. If a URL is found it then passes that information back to the _CaseTriggerHandler_.

_**scanURLs**_

This class contains 3 important sections:

1. The Constants that need to be set ahead of time
2. The _checkURLMalicious_ method
3. The _VTCallout_ method

The constants that need to be set include your **VirusTotal API key**, the **VirusTotal endpoint**\- which is currently set to the URL Report endpoint, and the **Threshold**.

The **Threshold** value is what will be used to determine over what number of positives received from VirusTotal report that you deem the URL to be malicious. The Threshold value can also be passed through from the _caseTriggerHandler_. Currently, the constant value is set to 10.

The _checkURLMalicious_ method handles calling out to the _VTCallout_ method, as well as, what to do based on the results of the callout. If the return value is TRUE, the method calls the _caseReassignmentPostScan_ class to send the case to the No Man's Queue. If the return value is False, it will also call the _caseReassignmentPostScan_ class, but to send it back through the assignment rules. This method was designed to be able to handle more than one scanning API and can be easily fitted to handle as many as one thinks is necessary to have to check a URL.

The _VTCallout_ method is the method that makes the callout to the VT API. In this method, the callout is made and then the JSON is parsed to determine, first, if the URL was found - this is based on the response code being 1 or 0 (1 = found, 0 = not found). Second, if the URL was found, to check if the number of positives for that URL is greater than the set Threshold. If the number is greater, the method will return TRUE; if the value is less or if no URL is found, the method will return FALSE.

_**caseReassignmentPostScan**_

This last class is what handles the logic for reassigning the cases after they have been parsed. There are 2 methods in this class: _casePassAssignmentRule_ and _caseMovetoNoManView_.

_casePassAssignmentRule_ will change the value of the Bypass Assignment Rule 1 to TRUE and then send the case back through the Assignment rules so that it gets to the correct queue per your organization's structure.

_caseMovetoNoManView_ will take the case and send it directly to the No Man's Queue. As the Dev Admin, you can decide who can see that queue and what the best course of action is to do with that case. Alternatively, you can modify this method to delete the case altogether. I chose not to do this for the project as it seemed extreme to me.

Overall the goal of this project is to ensure the security and safety of your internal users from malicious external URLs who are willing to pray on the lack of security and knowledge of your users through the use of phishing or malware URLs. I modularized this and tried to make it as flexible as possible to accommodate the many different Service structures out there.

As always, if you have any questions, or would be interested in working with me on a customized solution for your organization, please reach out to [yelena@sf9to5.com](mailto:yelena@sf9to5.com).

Github Project: [https://github.com/ysfdc/CaseURLScanner](https://github.com/ysfdc/CaseURLScanner)
