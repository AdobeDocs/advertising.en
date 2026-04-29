---
title: File requirements for conversion feed files
description: Reference the requirements for conversion feed files.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
TQID: https://experienceleague.adobe.com/y5kEsTB71WWQE6RGYdsIq0GFuZI037tRbRQTwuOP8aM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# File requirements for conversion feed files

The following are the requirements for the file format, required and optional data fields, file name, and file transfer protocol for feed files.

## File Format

The data file must be in flat text (TXT), comma-separated values (CSV), or tab-separated values (TSV) format. The file may consist of a header row and data rows with values separated by tabs, commas, or another character (but not spaces):

* **Header row:** (Optional) The first line of the file is a header, which specifies the required field names (or column names) in a specific order, separated by tabs or commas. The required column names include the conversion metrics that Adobe Advertising is tracking as conversions.

* **Data rows:** Each subsequent line includes data fields in the same order as the header and separated by tabs or commas. If the first record isn't a header, then each data row must include all possible fields, in a specified order. The values of all IDs and conversion metrics must be alphanumeric.

  When multiple clicks on one or multiple ads lead to one transaction, then you must determine the click ID and the tracking ID to which to attribute the transaction. Because a unique ID is reported for each transaction, you can update individual transactions.

## File-naming convention

The file name must include the date and be consistent. For example, if you use the format YYYYMMDD.txt, then a file sent on May 15, 2011 must be named 20110515.txt.

## File transfer protocol

Send the file via the SFTP transfer protocol, using Port 22. You'll need to provide your public key information.  Your Adobe Account Team or the implementation team provides you the server location along with the credentials required for your system to transfer the files.

>[!TIP]
>
>Conversion data feeds are processed multiple times a day. Upload the daily feed as soon as possible after 12:00 midnight local time so that Adobe Advertising can process your data and make it available in the reporting UI in the early morning.

>[!MORELIKETHIS]
>
>* [Data requirements for data feeds using EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Data requirements for data feeds using a transaction ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
