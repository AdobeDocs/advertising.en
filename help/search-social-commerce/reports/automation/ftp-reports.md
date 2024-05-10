---
title: FTP access to reports
description: Learn how to receive reports at a read-only FTP location.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
---
# FTP access to reports

You can optionally receive reports at a read-only FTP location, from which you can retrieve the files for additional automated processes (for example, to parse the data with another program). All basic reports except for [!UICONTROL Search Engine Account Report] and all advanced reports can be delivered to an FTP location as zipped TSV files (the default) or CSV files, with a .ZIP file extension. Any TSV or CSV file headers are included and can't be suppressed.

FTP access to reports requires access to a specified FTP account, and you must set up report templates using a specific naming convention and a schedule.

## Set up an FTP account for access to reports

* Contact your Adobe Account Team to set up an FTP account for report access.
  
  The team provides you with your username and password.

## Set up report templates for FTP delivery

To generate reports in your designated FTP directory, create a [report template](templates/template-create.md) with the following naming conventions and schedule.

>[!NOTE]
>
>All advanced reports and all basic reports except for the [!UICONTROL Search Engine Account Report] can be delivered to an FTP location.

1. In the report template, include the following information anywhere in the template name:
   
   * `FTP` (in uppercase letters).
   
   * (Optional) Any of three systems dates, using the following case-sensitive syntax, including brackets:
     
     * `[TODAY]` &mdash; To include the date, hour, and minute when the report was run. Because this includes the exact time, the same template can be run multiple times a day without overwriting the previous report.
     
     * `[SDATE]` &mdash; To include the start date of the report date range.
     
     * `[EDATE]` &mdash; To include the end date of the report date range.
   
   * (Optional) `[CSV]` (in uppercase letters and enclosed in brackets) to create files in CSV format rather than the default TSV format.
  
   Example: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` would create a file like 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Schedule the report to run at a specific time.

   The reports are delivered to the FTP account within an hour after they're completed. 

>[!NOTE]
>
>* To send completed reports by email, simply enter the addresses of all email recipients when you generate the report or template.
>* Reports are run according to their specified schedules and are delivered to the FTP account within an hour after they're completed.

## Access reports in an FTP repository

To access your reports, connect to one of the following FTP hosts, using the login for your FTP account (`amo<userID>rpt`, such as amo1234rpt) and either a password or a private connection key if one is set up:

* International customers: `ftp3.adobe.net`
* US customers: `ftp5.adobe.net`

>[!NOTE]
>
>The reports repository is read-only and is purged every 15 days.


>[!MORELIKETHIS]
>
>* [Create a report template](/help/search-social-commerce/reports/automation/templates/template-create.md)
