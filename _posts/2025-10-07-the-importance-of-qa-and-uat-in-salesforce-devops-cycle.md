---
title: "The importance of QA and UAT in Salesforce DevOps cycle"
date: 2025-10-07
categories: 
  - "admin-life"
---

The DevOps process should include two types of testing: QA (Quality Assurance) and UAT (User Acceptance Testing). Both types of testing are crucial for ensuring successful rollouts of Salesforce implementations. This is particularly important as we increasingly see growing complexity inflows and their effects on other components, such as validation rules or APEX. Testing is a critical step to ensure process breakdown is caught before rollout.

### So, what's the difference between QA and UAT? Let's review.

1. QA (Quality Assurance) should focus on catching issues early in the development cycle. The internal dev team reviews the technical requirements and performs tests checking functionality, data integrity, and edge cases. QA ensures that the system works as designed without introducing errors, bugs, or unintended outcomes. Testing conditions should include branching logic, record updates, and error handling. Regression tests should also be run to confirm there is no conflict with other automation in place. It is also critical to ensure that the person testing the build differs from the person building it. This tends to be forgotten and can result in a biased result.

3. UAT (User Acceptance Testing) is where the business units get involved, testing the system from an end-user perspective. Business users ensure the solution meets their requirements and aligns with business processes. UAT should be tested through real business scenarios to identify usability concerns or unexpected behavior. UAT is essential in testing flows that involve multiple users or departments, where roles, permissions, and cross-object interactions can lead to discrepancies if not thoroughly validated.

As Salesforce continues to evolve, the number of admins and developers turning to declarative automation like Flows has increased. Unfortunately, many creating or updating Flows do not fully understand all of the nuances that come with them, and using QA and UAT as a stop-gap can be beneficial in the long term. Proper testing ensures that edge cases, role-specific scenarios, and complex business logic are accounted for.

### Sample QA & UAT Punchlist

The best way to institute QA and UAT is through a punchlist (your team might call it something else), but it is essentially a table where all the feedback can be tracked. While you may have a ticketing system, business users often don't have access to it, so this is an easy way to mitigate it. Below is an example table that helps track who is responsible for each test, what was tested, and whether the outcome matches expectations.

| **Test Name/ID** | **Test Type (QA/UAT)** | **Steps Taken** | **Expected Results** | **Actual Results** | **Relevant URLs** | **Tested By** |
| --- | --- | --- | --- | --- | --- | --- |
| Name of the Tested Item or Ticket Number | Opportunity is closed, as Won.   Related Contact’s status updated | Steps to be taken by the User | Results expected by the User | Results populated by the User testing | Link to the record used for testing | Person who tested |
| Example:   Opportunity Close | UAT | 1\. Close Opportunity as Won   2\. Update related Contact record   3\. Confirm Opportunity stage | Opportunity is closed, as Won.   Related Contact’s status updated. | Opportunity closed successfully   Contact record not updated | Sample Link | Sales Rep |

This punchlist is a structured way to track issues, fixes, and who is responsible for validating them. The table links relevant items to streamline team collaboration and track bugs or errors more effectively.

As implementations grow in complexity with the increased use of flows and other automation tools, it becomes essential to implement a thorough DevOps process that includes both QA and UAT. Both testing phases serve unique purposes to ensure functionality, business processes, and user experience align. The goal is to check for bugs and ensure the system works holistically for the business, with minimal surprises post-deployment. Proper testing leads to more efficient, reliable, and scalable Salesforce solutions.
