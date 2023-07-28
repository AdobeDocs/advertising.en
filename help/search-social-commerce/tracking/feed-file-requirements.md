---
title: File requirements for conversion feed files
description: Reference the requirements for conversion feed files.
exl-id: 7d865802-0ab9-4965-9618-6bc0667f4939
feature: Search Tracking
---
# File requirements for conversion feed files

The following are the requirements for the file format, required and optional data fields, file name, and file transfer protocol for feed files.

## File Format

The data file must be in flat text (TXT), comma-separated values (CSV), or tab-separated values (TSV) format. The file may consist of a header row and data rows with values separated by tabs, commas, or another character (but not spaces):

* **Header row:** (Optional) The first line of the file is a header, which specifies the required field names (or column names) in a specific order, separated by tabs or commas. The required column names include the transaction properties that Adobe Advertising is tracking as conversions.

* **Data rows:** Each subsequent line includes data fields in the same order as the header and separated by tabs or commas. If the first record isn't a header, then each data row must include all possible fields, in a specified order. The values of all IDs and transaction properties must be alphanumeric.

  When multiple clicks on one or multiple ads lead to one transaction, then you must determine the click ID and the tracking ID to which to attribute the transaction. Because a unique ID is reported for each transaction, you can update individual transactions.

## File-naming convention

The file name must include the date and be consistent. For example, if you use the format YYYYMMDD.txt, then a file sent on May 15, 2011 must be named 20110515.txt.

## File transfer protocol

Send the file via the SFTP transfer protocol, using Port 22. You'll need to provide your public key information.  Your Adobe Account Team or the implementation team will provide you the server location along with the credentials required for your system to transfer the files.

>[!TIP]
>
>Conversion data feeds are processed multiple times a day. Upload the daily feed as soon as possible after 12:00 midnight local time so that Adobe Advertising can process your data and make it available in the reporting UI in the early morning.

>[!MORELIKETHIS]
>
>* [Data requirements for data feeds using EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Data requirements for data feeds using a transaction ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
