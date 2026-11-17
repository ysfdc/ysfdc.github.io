---
title: "How to Mass Upload and Import Records in Salesforce from CSV, Excel, XML, JSON and NDJSON"
date: 2024-11-06
categories: 
  - "admin-life"
  - "development"
  - "tips-tricks"
---

\*\*_Written by Dorian Sabitov_

## Introduction: Why do You Need To Mass Import/Export a Data

Managing large volumes of data in Salesforce can quickly become overwhelming without the right tools. Accurately getting that data into Salesforce is essential whether you're importing customer information, sales data, or custom records. This process becomes even more challenging when handling complex datasets or working with different file formats like CSV, JSON, or NDJSON. In these situations, efficient [mass update records in Salesforce](https://www.sfapps.info/mass-update-and-upsert-records-in-salesforce/) can save your team hours of manual work and reduce the risk of data errors.

Imagine a mid-sized retail business that just upgraded to Salesforce and needs to migrate all its historical sales data—hundreds of thousands of records—from its old system. Manually uploading each entry would take days, if not weeks, and the risk of incorrect field mapping or validation errors is high. 

## Why Efficient Data Imports Matter

Efficient data imports are not just about saving time; they help ensure accuracy, maintain data integrity, and minimize disruptions to daily operations. For example, when this retail business uses [Sliced Bread ETL](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N4V00000DZClKUAX), it can handle different file formats (CSV, Excel, XML, JSON, and NDJSON) and automatically map data fields, reducing the chance of human error. Additionally, they can set up the tool to run scheduled imports so new data from their eCommerce site flows into Salesforce overnight, keeping everything up to date without manual intervention.

Businesses can handle even the most complex data import scenarios without hassle using the right tools. The following sections will guide you through understanding file formats, preparing data, and selecting the right tools.

## Understanding Data File Formats: CSV, Excel, XML, JSON, and NDJSON

When importing large volumes of data into Salesforce, the format of your data file is crucial. Salesforce supports several formats for importing records, but the most commonly used formats are CSV (Comma-Separated Values), JSON (JavaScript Object Notation), and NDJSON (Newline Delimited JSON). Each of these formats has unique characteristics that make it suitable for different use cases. Let’s explore these formats and their specific applications for Salesforce imports.

### CSV (Comma-Separated Values)

CSV is the standard format for data imports into Salesforce and is supported by Salesforce’s built-in tools, such as the [Data Import Wizard](https://help.salesforce.com/s/articleView?id=sf.data_import_wizard.htm&type=5) and [Data Loader](https://developer.salesforce.com/tools/data-loader). In CSV files, each line represents a record, and each field is separated by a comma, making it a simple and widely recognized format.

**Use Case:** CSV is most effective for importing straightforward, flat data such as contact lists, sales records, or basic inventory. For example, if a company needs to import 100,000 customer records into Salesforce, including fields like names, email addresses, and phone numbers, it would typically use a CSV file.

However, CSV has its limitations when dealing with more complex or nested data structures, such as hierarchical data with relationships between objects, which is where other formats like JSON or NDJSON come into play.

**Limitations of CSV in Salesforce:**

- **Data Import Wizard**: [This cloud-based tool supports up to 50,000 records](https://help.salesforce.com/s/articleView?id=sf.import_with_data_import_wizard.htm&type=5) and is limited to CSV format. It has an intuitive interface for importing standard and custom objects but is less suited for complex data scenarios​.

- **Data Loader**: This tool allows the import of [up to 5 million records](https://help.salesforce.com/s/articleView?id=sf.data_loader_about.htm&type=5), but like the Import Wizard, it only works with CSV files​.

### JSON (JavaScript Object Notation)

JSON is a more flexible data format than CSV. It supports nested structures, making it ideal for complex data relationships where records may have multiple associated objects. JSON is beneficial for importing data with parent-child relationships, such as products with multiple variants or customers with associated orders.

**Use Case:** For instance, if a company needs to import data on products where each product has multiple attributes (like color, size, and stock levels), a JSON file would allow them to structure the data in a way that maintains those relationships. JSON also supports structured data better than CSV, making it preferable for imports that involve more complex relationships.

However, the standard Salesforce import tools (Data Import Wizard and Data Loader) do not support JSON imports. For businesses that need to handle JSON data, third-party tools like Sliced Bread ETL on Salesforce come into play. These tools can process JSON files, making them an excellent choice for organizations with structured or hierarchical data​.

### NDJSON (Newline Delimited JSON)

NDJSON, or Newline Delimited JSON, is a specialized format in which each JSON object is placed on a new line. This makes it particularly suitable for handling large volumes of data in real time, as each record can be processed individually without wrapping all records in a single array.

**Use Case:** Consider a scenario where a streaming platform wants to import daily user activity logs into Salesforce. Each log entry (a single interaction, such as viewing a video or making a purchase) would be its own line in an NDJSON file, making this format ideal for high-volume, real-time data imports.

### Key Takeaways:

- **CSV** is the preferred format for standard Salesforce imports, especially for simple, flat data structures. Salesforce’s built-in tools, such as the Data Import Wizard and Data Loader, work exclusively with CSV files.

- **JSON** offers more flexibility for complex and hierarchical data but requires third-party tools like Sliced Bread ETL for import into Salesforce.

- **NDJSON** is ideal for large-scale, real-time data imports where each record is discrete. Tools like Sliced Bread ETL support this format for advanced import needs.

By using Sliced Bread ETL, you can ensure that your data is imported efficiently, regardless of the format, while minimizing errors and ensuring data integrity.

## Preparing Your Data for Import With Sliced Bread ETL

Before you begin importing data into Salesforce, you must prepare your data thoroughly. Proper preparation helps prevent errors, ensure smooth imports, and maintain data integrity. Importing unclean or disorganized data can lead to mismatches, validation rule failures, and incomplete records, which can cause long-term data issues.

### Insight: 

“One of the visions when creating Sliced Bread was that we believe that data transformation belongs on Salesforce and not in your source file. Keep your sources as is, and use Sliced Bread to do the necessary transformations.”  
\--Martijn Schwärzer, Sliced Bread CEO  

Here’s a step-by-step guide to ensure your data is ready for import:

### 1\. Clean and Organize Your Data

Before importing, ensure the data is free from errors, duplicates, and inconsistencies. Cleaning your data involves:

- Removing duplicates: Salesforce can create issues with duplicated records, so it's essential to remove them beforehand. Use Excel’s de-duplication features or other tools to identify and remove duplicates.

![](/images/AD_4nXfIffl1cusFBBvz8jnzW5FPpmMsEwonBvPwWuLm-XVcV2Vjah7I24ensH31eKmFmD2yKDHvPcBYRHPTihhPjlZZlOZGtLygqnwuf3BnsAY87C7Gs6xyYa7T3neI-3Ou88wL5pUa4JtRhtuX2sOtrxWDca6Zx4WNaHnWSF5MK2Rel9ndkxmcLNI)

- **Correcting inconsistencies**: Ensure uniformity in how data is formatted. For example, check that phone numbers follow the same format and that names are standardized (e.g., using full names or initials).

- **Validating data**: Ensure that the data you’re importing adheres to the field types in Salesforce. For example, if importing into a numeric field, ensure the data doesn't contain text characters.

![](/images/AD_4nXd6B86N2gdVGVVPRA5ANxWE4Xi_h5d_TzIMpv591kX06nSEVUzm7pXOHiTVWO0cAfkI38AqdN9n67a141NDQ_4JHwce63TMnQnFNL3_AyLzEhbv3QY9slPGUjlOicA3iBhgtY68QC2uSd9IV4gNI-DM0L2gPrH_hDTpvkVm_v36-LP7qtptOx4)

- **Handling missing fields**: If required Salesforce fields are missing in your import data, be sure to fill them in. Missing data can cause validation errors or leave records incomplete.

**Example:** Imagine you’re importing 50,000 customer contact records into Salesforce, and some records don’t have valid email addresses. Without fixing this issue, Salesforce could reject many of these records, leaving gaps in your contact database. You can avoid these issues by cleaning and validating this data in advance.

### 2\. Match Your Data Fields to Salesforce Fields

Before importing, ensure your data fields align with the fields in Salesforce. This step is essential to avoid errors or missing information during the import process. It’s crucial to:

- **Review Salesforce’s field structure**: Check your Salesforce instance to see the fields you’ll be importing into, especially if you have custom objects or custom fields. Salesforce provides a field mapping tool that lets you align your source data with Salesforce’s fields.

- **Ensure field consistency**: For example, date fields in your data follow the required Salesforce format (e.g., YYYY-MM-DD). If your data format doesn’t match, your records may be rejected.

![](/images/AD_4nXcdfow2cpqim0802-64aliHyvbL3TMA-1c4-bjTB8CapeQLAon1mla8HOyDEKicckCZNwPf9JTbB3AGbbd77RvdyqYONWeK33tiftBK0x_zjpthvS3gdah9byJ7sOoN7g1cBv2ExLUCx3zT1psVjKxJ5pTW5jUsuiVl6aacXEQM4krMu1UZyA)

**Example:** If importing lead records into Salesforce, ensure that fields like “Lead Source” or “Industry” match Salesforce’s existing field types and picklist values. Customizing or creating new fields in Salesforce might be necessary to accommodate all data.

### 3\. Handling Validation Rules

Validation rules in Salesforce enforce business logic, ensuring that specific criteria are met before a record can be saved. While beneficial, these rules can cause issues during data import if your data doesn’t comply.

- **Review validation rules**: Before importing, check whether any validation rules might prevent the import from succeeding. You may need to temporarily deactivate these rules during the import and then reactivate them afterward.

- **Update workflows**: Similar to validation rules, some workflows or triggers can cause errors during data imports. Temporarily disabling them until after the import can help streamline the process.

### 4\. Choosing the Right File Format

As mentioned, Salesforce’s native tools, like Data Import Wizard and Data Loader, only support CSV files. If you’re working with more complex data structures that require JSON or NDJSON formats, using a tool like Sliced Bread ETL will ensure proper data handling without the risk of file format incompatibility.

![](/images/AD_4nXdmpvb-XJzifzEdOPHsN0k-au_8bItyFwMe515TEzCuHFnoeQSE5K-lPHFXHlCMlN9dKctD93EdopAGmGAMwb6DkUwSFKZhqqRWDaIDP9oC_q7crxlItOHSxH2fy4kpAj58-v-WVUJL6A8pwvR8otGBWetyhPsDMXiuKl5xiYv8zT5Q9Rr8rRA)

### 5\. Run Test Imports

Running a test import with a small sample of your data is one of the most critical steps in preparing for a larger import. By testing with a small dataset, you can:

- **Catch potential errors early**: Test imports help you catch issues with field mappings, formatting errors, and validation rule conflicts before they affect a large dataset.

- **Verify data accuracy**: Ensure the test data is imported correctly and fields are mapped as expected.

**Example:** If importing 200,000 records, start with a sample of 500 records. This will help you see if there are any issues with missing fields or validation rule errors without risking a large-scale import failure.

### 6\. Backup Your Data

Before importing new data, always create a backup of your current Salesforce data. This step is vital because if something goes wrong during the import, you’ll have a snapshot of your data that you can revert to.

- **Export data**: Salesforce allows you to export your data for backup purposes. You can use native tools like Salesforce Data Export or third-party backup solutions​.

Properly preparing your data can avoid many of the common issues that arise during imports. Tools like Sliced Bread ETL help streamline this preparation by providing enhanced field mapping and error detection, making it easier to ensure your data is import-ready.

## Import Methods and Tools

Choosing the right tool ensures a smooth, efficient, and error-free process when importing data into Salesforce. Salesforce offers several built-in tools, like the Data Import Wizard and Data Loader, but these can be limiting when dealing with large or complex datasets. Third-party solutions like Sliced Bread ETL and the Salesforce Bulk API (including Bulk API 2.0) offer powerful capabilities for more advanced requirements. Here, we'll explore the available import tools and methods and provide recommendations based on your needs.

### 1\. Data Import Wizard

![](/images/AD_4nXcXXITO0wVf78If5OgeufabMcd3U0Fv4KrCp3a3JSY4Od0IbmygGs6nP9bpNAEF1_f0v2H2pSC4fMoFRNRh1rwzqL6q6OtnJbTDqgPWy-l5eE5CAIJZ-mNKUVFMzsUnO2Fv0D74zNrLNRYK_68AHl871eBRT_ko8fBoa0Vewepp6XC735rwqPI)

The **Data Import Wizard** is Salesforce’s entry-level import tool, designed for simple, smaller imports. It’s an excellent option for users with no technical background who need to perform straightforward imports for standard or custom objects.

- **Advantages:**
    - Free and available in all Salesforce editions.
    
    - Simple, user-friendly interface.
    
    - Supports deduplication and handles up to 50,000 records​.

- **Limitations:**
    - Limited to CSV format.
    
    - It can only import up to 50,000 records, making it unsuitable for large-scale operations.
    
    - Does not support complex relationships between data objects or automated imports​.

### 2\. Data Loader

![](/images/AD_4nXcXXV6tN7zTBroqe7EATf4B-ZhiQetSByXas_9HZb2V6UciCHpLc8n-N5e2F57fTxroK5xMUorOVK0z5m_r5eMGBuM3TRx6a36dUZJNHHjRbKzO8LP_uaVibtg3GHZ88CO349AkwwsX5ASbFRwa8fpXkVjCflCS6qhI0yl02qx6MH15Rs0NVO8)

The Salesforce Data Loader is a more advanced tool for larger and more complex imports. As a desktop application, it supports up to 5 million records and allows users to insert, update, delete, and export data.

- **Advantages:**
    - Supports bulk imports of up to 5 million records.
    
    - Offers advanced functions like update, delete, and upsert (update and insert).
    
    - Allows scheduling of batch imports.

- **Limitations:**
    - Only supports CSV format, requiring manual conversions for JSON or NDJSON data.
    
    - Requires installation and may not be as intuitive for non-technical users.

### 3\. Sliced Bread ETL 

![](/images/AD_4nXfrPw5yTrYQz20zXnAyVO6lPRQpsBvQU3IvCx8WKXKRI2wN8Epyq7Xvlyfr3qwsyXKtUVhjCby8JQmBDdqgW8kSp82VASWwMw36OQ8qpCNrLp5dsOH8Rh3ha9OHyfZ4K0S91IWYCGKnrzM7I-DX4eV5EdAsQPGz6WaZiv3tB_rs_sfZnTbza-Q)

Sliced Bread ETL is the recommended solution for businesses handling large, complex datasets. It supports multiple file formats (CSV, JSON, and NDJSON), advanced field mapping, and large-scale operations, making it ideal for businesses that need to import structured data or process real-time updates.

- **Advantages:**
    - Supports CSV, JSON, and NDJSON file formats, making it versatile for various import scenarios.
    
    - Handles complex data relationships and hierarchical structures.
    
    - Automates imports and scheduling tasks to reduce manual intervention.
    
    - Provides real-time validation and error handling, making it more robust than native Salesforce tools​.

- **Real-Life Example:** Imagine a healthcare company that needs to import patient records in JSON format. The records contain complex data, including medical history, appointments, and test results. Sliced Bread ETL can handle this import seamlessly, keeping the hierarchical structure intact and ensuring accurate field mapping while offering automation for ongoing data synchronization.

- Limitations: Requires a slight learning curve and may be less intuitive for non-technical users.

### 4\. Salesforce Bulk API

The [Salesforce Bulk API](https://developer.salesforce.com/docs/atlas.en-us.api_asynch.meta/api_asynch/api_asynch_introduction_bulk_api.htm) is designed for large-scale, asynchronous data imports and is optimized for loading millions of records. It processes records in parallel batches, making it significantly faster than the traditional Data Loader. This API is ideal for handling high-volume data operations and can support data loads of up to 150 million records.

- **Advantages:**
    - Processes large datasets more efficiently by dividing them into smaller batches.
    
    - Can import up to 150 million records at once.
    
    - Works well for importing data into both standard and custom objects.

- **Limitations:**
    - It requires technical knowledge to set it up and use it effectively.
    
    - Due to its complexity, it may not be the best choice for smaller imports.

### 5\. Bulk API 2.0

[Bulk API 2.0](https://developer.salesforce.com/docs/atlas.en-us.api_asynch.meta/api_asynch/bulk_api_2_0.htm) enhances the original Bulk API, offering a simpler and more user-friendly interface for large-scale imports. It improves on the original by providing automatic job creation and handling, making the process faster and more efficient for larger datasets.

- **Advantages:**
    - It provides an improved, more intuitive interface than the original Bulk API.
    
    - Automates job creation and completion, reducing manual workload.
    
    - Supports faster processing for extremely large datasets​.

- **Limitations:**

- **Limited to CSV format**: Like the traditional Bulk API, Bulk API 2.0 only supports CSV format for data ingestion, which means that if your data is in JSON or NDJSON, you’ll need to convert it before importing.

- **Requires API permissions**: To use Bulk API 2.0, users must have the “API Enabled” permission on their profiles​.

- **Batch Processing Only**: It’s designed for asynchronous operations, which may not be suitable for smaller, real-time updates.

- **Record Limits**: Although it can handle millions of records, for very large-scale operations, you might need to break the imports into smaller chunks, which may require more complex job handling​.

- **SOQL Limits**: While Bulk API 2.0 supports large data sets, the complexity of the SOQL queries may still be limited by standard Salesforce governor limits, which can affect the efficiency of specific queries​.

**Use Case:** A financial services company needing to import daily transaction data in batches of millions of records can benefit from Bulk API 2.0. The API processes the data asynchronously, ensuring that Salesforce remains responsive even during high-volume data loads. Plus, with the automation features, the team doesn’t need to manually manage each import job.

Overall, Bulk API 2.0 is an excellent solution for organizations with large-scale data management needs but may require additional planning and understanding of its limitations when dealing with complex data structures or formats beyond CSV.

### Insight:

You can find video instructions for common data management operations in Salesforce using Sliced Bread ETL on [YouTube](https://www.youtube.com/@slicedbread-etlonsalesforc3770).

## Handling Common Import Issues

Even with the most well-prepared data and the best import tools, data imports into Salesforce can encounter various issues. Understanding and handling these common problems will help ensure your mass imports go smoothly. Below are some of the most frequent issues you might face and how to overcome them:

### 1\. Validation Rule Failures

Validation rules in Salesforce are designed to enforce business logic and ensure data accuracy. However, they can become an obstacle during data imports if your data doesn’t meet the required criteria.

- **Solution**: Before starting the import, review your active validation rules and determine if any might block the data you're trying to import. You can temporarily disable specific validation rules for the duration of the import and then reactivate them afterward. Alternatively, ensure your import file complies with all validation rules, adjusting data in your CSV, JSON, or NDJSON files as needed.

**Example**: If a rule requires a phone number to be in a specific format (e.g., (XXX) XXX-XXXX), but your import file contains various formats, you will need to standardize all phone numbers before the import.

### 2\. Duplicate Records

One of the most common issues with mass imports is creating duplicate records, mainly when importing data from multiple sources. Salesforce provides built-in deduplication features, which might not catch every scenario, especially for large datasets.

- **Solution**: Tools like Sliced Bread ETL and Dataloader.io offer better deduplication management by allowing you to define more precise matching criteria, such as using emails or Salesforce IDs to prevent duplicate entries. 

**Example**: A healthcare company importing patient data from two systems might have several duplicate entries for the same patient. By configuring Sliced Bread ETL to match records using the email address field, the company can prevent creating duplicate entries for the same individual.

### 3\. Field Mapping Errors

Field mapping is a critical step in any import process. Incorrect mappings can result in data being placed in the wrong fields, causing inconsistencies and inaccuracies.

- **Solution**: Always review and manually adjust your field mappings before importing, especially if importing custom objects or using a tool that supports multiple file formats. If your import tool doesn’t automatically match fields, ensure that the headers in your data file match Salesforce field names as closely as possible​.

**Example**: If you’re importing a CSV file with a field labeled “Cust\_Name,” Salesforce might not automatically recognize this as “Customer Name,” requiring you to manually map it.

### 4\. Data Format Inconsistencies

Inconsistent data formatting—such as date formats, phone numbers, or address fields—can cause data validation errors during imports.

- Solution: Ensure all fields follow the required Salesforce formatting before importing. For instance, date fields should follow the YYYY-MM-DD format, and phone numbers should adhere to a consistent format across all records. Some tools, like Sliced Bread ETL, provide pre-validation checks to flag formatting errors before the import.

**Example**: A retail company importing sales data might have dates in different formats (e.g., “10/01/2023” and “2023-01-10”). Salesforce could reject these records unless the format is standardized before import.

### 5\. Workflow or Trigger Interference

Automated workflows or triggers in Salesforce may cause problems during data imports. For instance, if a workflow triggers emails based on creating new leads, a mass import could send hundreds or thousands of unwanted emails.

- **Solution**: Temporarily disable workflows, triggers, and processes during the import to prevent them from interfering. After the import is complete, you can reactivate them. This is a common practice when importing a large volume of records into Salesforce​.

**Example**: A nonprofit organization is importing volunteer data into Salesforce. If they have a trigger set to send a welcome email to new volunteers, importing thousands of volunteer records at once could unintentionally send thousands of emails. By temporarily disabling this trigger, they can complete the import without issue.

### 6\. CSV File Size Limitations

For large imports, CSV file size can become an issue. Salesforce’s native tools, like the Data Import Wizard, limit the number of records you can upload at one time, and file size limitations may cause upload failures.

- Solution: Break the CSV file into smaller chunks for large datasets or use tools like Sliced Bread ETL or Bulk API 2.0, which can handle much larger file sizes. Bulk API 2.0 is handy for processing large volumes of data, as it can handle millions of records asynchronously.

**Example**: A financial services firm importing customer transaction records would encounter issues with the file size limit if it tried to bulk upload Salesforce everything at once. Using Bulk API 2.0, it can divide its records into batches, ensuring the import is processed efficiently.

## Wrapping Up: On How to Mass Manage Records in Salesforce

When handling large-scale data imports like a Salesforce bulk upload, it's essential to use the right approach. Whether you're trying to mass import contacts into Salesforce, mass create fields in Salesforce, or bulk transfer contacts, having a clear plan and using reliable tools makes a big difference.

For simple imports, Salesforce’s native Data Import Wizard is an option, but it has limitations regarding scale and complexity. For more advanced needs, tools like Sliced Bread ETL and Bulk API 2.0 offer greater flexibility and can handle large volumes of data, multiple file formats, and complex field mappings. These tools make it much easier to load data into Salesforce efficiently without running into errors.

If you're working with large datasets, especially when handling complex tasks like bulk field creation in Salesforce or transferring huge contact lists, it's important to consider tools like Sliced Bread ETL for automation and error management. Bulk API 2.0 is also an excellent option for handling massive uploads, allowing you to process data asynchronously and break it into manageable batches.

Remember, proper preparation is key before performing a Salesforce data load. This includes cleaning up your data, ensuring your field mappings are correct, and running a test import to catch potential issues early. Doing this can avoid common errors, save time, and ensure your data is uploaded accurately.

Whether you're dealing with how to mass import contacts into Salesforce, a simple data load Salesforce process, or more advanced data management, choosing the right tools and following these steps will ensure your Salesforce import is successful.

_"Dorian Sabitov is a 4x Certified Salesforce Administrator and Developer with extensive experience in customizing Salesforce to the client's needs. He started his journey in IT as a CRM admin and kept his focus on the Salesforce ecosystem. He loves exploring new integrations in Salesforce and spotting alternative ways to optimize business processes inside the CRM. He is currently working as a full-time Salesforce developer and contributing content to the [SFApps.info](http://sfapps.info/) educational portal."_
