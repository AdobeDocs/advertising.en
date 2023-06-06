---
title: Supported bulksheet file formats
description: Reference the general file requirements for bulksheets. 
---
# Supported bulksheet file formats

## File Formats

You can download, upload, and post bulksheet files for supported ad networks in any of the following formats:

* CSV (comma-separated values)
* TSV (tab-separated values)
* TXT (Unicode text), delimited by either commas or tabs
* ZIP (compressed) containing one file in CSV format, TSV format, or TXT format delimited by either commas or tabs

When you create/download a bulksheet, it's created in the specified file format with all relevant data included in the file. Use the following information to edit data in the file or to create your own bulksheet manually.  

## Basic contents of a bulksheet

The first record (line) of a bulksheet file contains a set of specific column names, collectively known as a <i>header</i>. The column names in the header are in a specified order and correspond to each of the fields in the subsequent data records. The column names required in the header vary by ad network.

Each subsequent record (line) contains data, with fields containing values (or no values) for each column in the header.

## Maximum file size

Bulksheet files can be up to 2.5 GB, which is about 2.5 million rows.

>[!NOTE]
>
>When you generate a bulksheet for multiple campaigns and the combined data consists of over 500,000 rows, the data is split by campaign into two or more files, named `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, and so on.

## Formatting requirements for different file types

Data fields delimited by tabs and by commas require different formatting.

### TSV files and TXT files delimited with tabs

Data fields in TSV files and TXT files delimited with tabs must be formatted as follows:

* The fields in each record are separated by tab characters. To omit a value for a field, use only the tab character.

  Example: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Fields can't contain embedded tab characters.

### CSV files and TXT files delimited with commas

Data fields in CSV files and TXT files delimited with commas must be formatted as follows:

* The fields in a record are separated by commas. To omit a value for a field, use only the comma.

  Example: `Cruises,5000,Caribbean,,,`

* Any field may optionally be enclosed within double-quotes (`""`).

  Example:  `"Cruises","5000","Caribbean",`

* Fields with embedded commas must be enclosed within double quotes (`""`).

  Example: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Fields with embedded double quotes must be enclosed within double quotes (`""`).

  Example: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Fields with leading or trailing spaces must be enclosed within double quotes (`""`).

  Example: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [About managing campaign data using bulksheets](../bulksheet-about.md)
>* [Operations you can perform in bulksheets](bulksheet-operations.md)
>* [Appendix - Bulksheet errors](../bulksheet-errors.md)
>* [Download/Create a bulksheet file](../bulksheet-download.md)
