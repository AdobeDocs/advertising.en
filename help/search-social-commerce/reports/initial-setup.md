---
title: The initial setup tasks for reports
description: Learn how to make metrics available in reports and how to automate reports.
exl-id: c2e76c63-ddb8-4762-8628-30cf3f54b8fd
feature: Search Reports
---
# The initial setup tasks for reports

New users should perform the following initial setup tasks:

* Make the conversion metrics that Adobe Advertising is tracking for an advertiser [available for reports and other views](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md), and optionally [rename any of the conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md that are displayed in column headings for readability.
  
  Transactions properties aren't available for reports unless you specifically make them available.
  
  If you later begin to track a new conversion metric, then you must repeat this task.

* (Optional) Automate report generation:
   
   * If you want to regularly generate report data for a specific time increment, such as a [!UICONTROL Campaign Report] for the last week or last 30 days, then you can set up [report templates](/help/search-social-commerce/reports/automation/templates/template-about.md) and schedule them to be run daily or on a specific day of the week or month. Each time the report is scheduled to run, a new report is generated. You have the option to notify the email addresses of specific Search, Social, & Commerce users when the report is completed, based on the [notification settings configured in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).
   
   * If you want to view up-to-date, daily report data in a custom-formatted spreadsheet, with or without pivot tables and any additional columns you need to perform further calculations, then you can set up a daily [spreadsheet feed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Spreadsheet feeds are refreshed daily with the latest performance data and continue to retain data for the previous dates. To configure spreadsheet feeds, you must first create a customized spreadsheet template in [!DNL Microsoft Excel]. You have the option to notify the email addresses of specific Search, Social, & Commerce users when a feed file is available, based on the [notification settings configured in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).
   
   * If you want to receive basic and advanced reports at an FTP location, then you can set up [FTP access to basic and advanced reports](/help/search-social-commerce/reports/automation/ftp-reports.md) by requesting an FTP account and setting up report templates using a specific naming convention.

>[!MORELIKETHIS]
>
>* [About reports](report-about.md)
>* [Data used for reports](data-used-for-reports.md)
