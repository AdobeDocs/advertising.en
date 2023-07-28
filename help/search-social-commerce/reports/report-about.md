---
title: About reports
description: Learn about performance reports, including the different report types available and how to automate reports.
exl-id: a945b255-a9b0-42f4-85ea-44416c837fc0
feature: Search Reports
---
# About reports

Performance reports allow you to track and manage the performance of your portfolios, ad networks, and ad network account entities at as granular a level as you want. Most reports provide complete visibility into how the ads in each marketing channel contribute to the overall conversion rate.

The data for a report is compiled dynamically each time you run the report. You can optionally generate a new report from an existing report. The available report parameters vary by report type. For most reports, you have the option to preview the first 50 lines instead of generating the entire report. When you generate a report, you can send a notification with download links to one or more email addresses when a report is completed, and the recipients can [manage the notifications in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

All completed reports are available in the [!UICONTROL Latest Reports] section of the [!UICONTROL Reports] view, and you can either view them in table format in the browser window or open or download them as files.

## Available report categories

The following report categories are available from the [!UICONTROL Reports] view. You may not have access to all of them; the available reports and the data they generate are determined by your role and how your customer account is configured.

| Report Category | Description |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Basic reports](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), which are available to all users, show the actual cost and click data for portfolios, ad network accounts, specific ad network accounts, campaigns, ad groups, ads, keywords, product groups, label classifications and label values, bid unit constraints, and network constraints. They are based on clicks billed by the applicable ad networks, and they optionally can include conversion data or any other metrics you create. |
| [!UICONTROL Advanced Reports] | [Advanced reports](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) provide additional insight into your advertising configuration, helping you to identify where you would benefit by changing your geographical targeting or network settings. They also can help you validate conversion data in the campaign and portfolio management views and reports against the advertiser's internal conversion tracking data. |
| [!UICONTROL Assist Reports] | [Assist reports](/help/search-social-commerce/reports/management/assist/assist-report-about.md) provide insights into the conversion paths for all of an advertiser's keywords and ads. They use data captured through the Adobe Advertising conversion tracking service and can be generated only for advertisers with the service. |
| [!UICONTROL Specialty Reports] | [Specialty reports](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) consist of data collected by the ad networks (rather than by Adobe Advertising tracking). |
| [!UICONTROL Model Accuracy Reports] | [Model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) indicate the accuracy of the cost and revenue models that are used to optimize bids. |

## Report automation

Schedule customized reports to be automatically generated in either or both of the following ways:

* Automatically generate reports each day, or on a specific day of the week or month, using [report templates](/help/search-social-commerce/reports/automation/templates/template-about.md).
  
  You can optionally set up [FTP delivery of basic and advanced reports](/help/search-social-commerce/reports/automation/ftp-reports.md) that use a template.

* Keep refreshing your customized spreadsheet templates with daily performance data using [spreadsheet feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## The Reports views

The [!UICONTROL Reports] views at [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] allows you to create and manage reports, templates, and spreadsheet feeds. The view includes two tabs:

* The **[!UICONTROL Latest Reports]** tab lists all reports available to you that were requested in the last seven days, except those that were manually deleted, with the most recent report at the top by default. Information shown for each report includes the schedule by which it is run (when applicable), the start and end dates for which data was or will be generated, and the report status (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]*, or *[!UICONTROL Error]*).
  
  Links next to each report allow you to view the report in the web browser or open or save it as a [!DNL Microsoft Excel] workbook (XLS) or tab-separated values (TSV) file; some report types can also be saved as [!UICONTROL Excel] workbooks with a separate worksheet for each applicable campaign.
  
  From this tab, you also can create a new report (which optionally may be used as a template), create a new report based on the settings for an existing report, cancel in-progress reports available to you by deleting them, and delete any completed report available to you. Reports older than seven days are automatically deleted.

* The **[!UICONTROL Templates]** tab lists all saved basic and advanced report templates available to you, including information about any schedules associated with them. The most recent template is at the top by default.
  
  From this tab, you create a new template, edit any template you created (including adding, changing, or removing its schedule), generate a report from a template; and delete any template available to you.

## How to use reports

| Purpose | Report |
| ---- | ---- |
| Performance Monitoring | <ul><li>[The [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[The [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[The [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[The [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[The [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[The [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Performance Troubleshooting & Trend Analysis | <ul><li>[The [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[The [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[The [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[The [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[The [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) and [The [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Any basic report that compares two time windows using the "[!UICONTROL Compare with]" feature</li></ul> |
| Identifying Business Growth Opportunities | <ul><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Advertisers with [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Customized reports within Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Advertisers with [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Customized reports within Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Data used for reports](data-used-for-reports.md)
>* [Initial setup tasks for reports](initial-setup.md)
>* [Generate a basic or advanced report](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Generate a model accuracy report](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Generate a specialty report](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Generate an assist report](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
