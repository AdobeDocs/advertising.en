---
title: (New UI) The initial setup tasks for reports
description: Learn how to make metrics available in reports and how to automate reports.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
    internal-label: Reports
---
# (New UI) The initial setup tasks for reports

New users should perform the following initial setup tasks:

* Make the conversion metrics that Adobe Advertising is tracking for an advertiser available for reports and other views, and optionally rename any of the conversion metrics that are displayed in column headings for readability. See "[Manage an advertiser's conversion metrics](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)."
  
  Transactions properties aren't available for reports unless you specifically make them available.
  
  If you later begin to track a new conversion metric, then you must repeat this task.

* (Optional) Automate report generation:
   
   * If you want to regularly generate report data for a specific time increment, such as a [!UICONTROL Campaign Report] for the last week or last 30 days, then you can set up [report templates](report-templates-manage.md) and schedule them to be run daily or on a specific day of the week or month. Each time the report is scheduled to run, a new report is generated. You have the option to notify the email addresses of specific Search, Social, & Commerce users when the report is completed, based on the [notification settings configured in [!UICONTROL Notification Center]][Manage custom alerts](/help/search-social-commerce/new-ui/notifications-manage.md).
   
   * If you want to view up-to-date, daily report data in a custom-formatted spreadsheet, with or without pivot tables and any additional columns you need to perform further calculations, then you can set up a daily [spreadsheet feed](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md). Spreadsheet feeds are refreshed daily with the latest performance data and continue to retain data for the previous dates. To configure spreadsheet feeds, you must first create a customized spreadsheet template in [!DNL Microsoft Excel]. You have the option to notify the email addresses of specific Search, Social, & Commerce users when a feed file is available, based on the [notification settings configured in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md).
   
   * If you want to receive basic and advanced reports at an FTP location, then you can set up [FTP access to basic and advanced reports](/help/search-social-commerce/new-ui/reports/ftp-reports.md) by requesting an FTP account and setting up report templates using a specific naming convention.

>[!MORELIKETHIS]
>
>* [About reports](report-about.md)
>* [Data used for reports](data-used-for-reports.md)
