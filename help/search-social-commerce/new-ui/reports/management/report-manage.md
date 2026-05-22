---
title: Manage scheduled reports
description: Learn how to manage scheduled reports.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
---
# Manage scheduled reports

Performance reports allow you to track and manage the performance of your portfolios, ad networks, and ad network account entities at as granular a level as you want. Most reports provide complete visibility into how the ads in each marketing channel contribute to the overall conversion rate.

The data for a report is compiled dynamically each time you run the report. You can optionally generate a new report from an existing report. The available report parameters vary by report type. For most reports, you have the option to preview the first 50 lines instead of generating the entire report. When you generate a report, you can send a notification with download links to one or more email addresses when a report is completed, and the recipients can [manage the notifications in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

All completed reports are available in the [!UICONTROL Latest Reports] section of the [!UICONTROL Reports] view, and you can either view them in table format in the browser window or open or download them as files.

## Available report categories

The following report categories are available from the [!UICONTROL Reports] view. You may not have access to all of them; the available reports and the data they generate are determined by your role and how your customer account is configured.

| Report Category | Description |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Basic reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md), which are available to all users, show the actual cost and click data for portfolios, ad network accounts, specific ad network accounts, campaigns, ad groups, ads, keywords, product groups, label classifications and label values, bid unit constraints, and network constraints. They are based on clicks billed by the applicable ad networks, and they optionally can include conversion data or any other metrics you create. |
| [!UICONTROL Advanced Reports] | [Advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) provide additional insight into your advertising configuration, helping you to identify where you would benefit by changing your geographical targeting or network settings. They also can help you validate conversion data in the campaign and portfolio management views and reports against the advertiser's internal conversion tracking data. |
| [!UICONTROL Assist Reports] | [Assist reports](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) provide insights into the conversion paths for all of an advertiser's keywords and ads. They use data captured through the Adobe Advertising conversion tracking service and can be generated only for advertisers with the service. |
| [!UICONTROL Specialty Reports] | [Specialty reports](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) consist of data collected by the ad networks (rather than by Adobe Advertising tracking). |
| [!UICONTROL Model Accuracy Reports] | [Model accuracy reports](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) indicate the accuracy of the cost and revenue models that are used to optimize bids, campaign budgets, and bid strategy targets for a portfolio. |

## Report automation

Schedule customized reports to be automatically generated in either or both of the following ways:

* Automatically generate reports each day, or on a specific day of the week or month, using [report templates](/help/search-social-commerce/reports/automation/templates/template-about.md).
  
  You can optionally set up [FTP delivery of basic and advanced reports](/help/search-social-commerce/new-ui/reports/ftp-reports.md) that use a template.

* Keep refreshing your customized spreadsheet templates with daily performance data using [spreadsheet feeds](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## The [!UICONTROL Scheduled Reports] views

The [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] views allows you to create and manage reports and report templates:

* The **[!UICONTROL Latest Reports]** tab lists all reports available to you<!-- Doesn't seem to be true: that were requested in the last seven days -->, except those that were manually deleted, with the most recent report at the top by default. Information shown for each report includes the schedule by which it is run (when applicable), the start and end dates for which data was or will be generated, who created the report, and the report status (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]*, or *[!UICONTROL Error]*).
  
  Links next to each report allow you to open or save the report as a [!DNL Microsoft Excel] workbook (XLS), a tab-separated values (TSV) file, or a comma-separated values (CSV) file. Some report types can also be saved as [!UICONTROL Excel] workbooks with a separate worksheet for each applicable campaign.
  
  From this tab, you also can create a new report (which optionally may be used as a template), create a new report based on the settings for an existing report or using a report template, cancel in-progress reports available to you by deleting them, and delete any completed report available to you.

* The **[!UICONTROL Templates]** tab lists all saved basic and advanced report templates available to you, including information about any schedules associated with them. The most recent template is at the top by default.
  
  From this tab, you create a new template, edit any template you created (including adding, changing, or removing its schedule), generate a report from a template; and delete any template available to you.

## How to use reports

| Purpose | Report |
| ---- | ---- |
| Performance Monitoring | <ul><li>[The [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[The [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[The [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[The [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[The [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[The [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Performance Troubleshooting & Trend Analysis | <ul><li>[The [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[The [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[The [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[The [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[The [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) and [The [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Any basic report that compares two time windows using the "[!UICONTROL Compare with]" feature</li></ul> |
| Identifying Business Growth Opportunities | <ul><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Advertisers with [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Customized reports within Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Advertisers with Adobe Advertising conversion tracking only) [The [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Advertisers with [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Customized reports within Adobe Analytics Analysis Workspace</li></ul> |

## Generate reports

### Generate a new report

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**.

1. Click **[!UICONTROL Create Report]**, click the report category in the left panel, and then select the report type.<!-- Add link to list of report categories and report types --> Click **[!UICONTROL Proceed]**.

1. (Optional) In the [!UICONTROL Create Report] window, change the default report settings for [basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [assist reports](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [model accuracy reports](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md), and [specialty reports](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md):

   1. (Optional) Enter a custom name for the report and for the template (if you save the report as a template).

   1. (Optional) To save the report settings as a template, enable the **[!UICONTROL Save as template]** setting.

   1. (Optional) Select a different report **[!UICONTROL Type]** within the same report category.

   1. (Optional) On the **[!UICONTROL Basic Settings]** tab, select an existing report template to use or change the default basic settings for the report.

   1. (Optional) Click the **[!UICONTROL Columns]** tab, and change the default columns in the report, including the column order.
   
      By default, all monetary data in reports is shown in the format for US dollars (such as 1,000.00). To display the value in the correct currency format (but without any currency symbols in CSV and TSV formats), add the "[!UICONTROL Currency]" column to the report. If the report includes data for accounts with different currencies, then any "[!UICONTROL Total]" monetary values are the sum of all numbers in the column, regardless of currency.
   
   1. (Some report types, optional) Click the **[!UICONTROL Filters & Attribution]** or **[!UICONTROL Filters]** tab, and add data filters, (some report types) limit the report results to include only specific label classifications, and change the default attribution rule and conversion attribution settings.

   1. (Optional) Click the **[!UICONTROL Scheduling]** tab, and change the default scheduling and delivery options.

1. Click **[!UICONTROL Create]**.

If you didn't specify a report schedule, then the report is run immediately; otherwise, it's run according to the specified schedule. The report name is added to the [[!UICONTROL Latest Reports] view](/help/search-social-commerce/reports/report-about.md). If you saved the report as a template, then it's also added to the [[!UICONTROL Templates] view](/help/search-social-commerce/reports/report-about.md). When the report is completed, the file is available to open or save; templates are available immediately.

If you entered any email addresses for notification, each recipient receives a notification when the report job is completed or fails, based on the user's [configured notification settings](/help/search-social-commerce/notifications/notification-edit.md) for reports.

### Generate a report from an existing report

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**, which opens to the **[!UICONTROL Latest Reports]** tab.

1. Do either of the following:

   * Hold the cursor over the report row, and click **...** > **[!UICONTROL Duplicate]**.
   
   * Select the check box next to the report. In the bulk actions toolbar, click [Duplicate](/help/search-social-commerce/assets/duplicate.png "Duplicate").

1. Edit the report settings if necessary.

1. Click **[!UICONTROL Create]**.

### Generate a report from an existing template

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**.

1. Click the **[!UICONTROL Templates]** tab.

  1. Do either of the following:
  
     * Hold the cursor over the template row, and click **...** > **[!UICONTROL Duplicate]**.
     
     * Select the check box next to the existing template. In the bulk actions toolbar, click [Duplicate](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.
  
  1. (Optional) Rename the template, and edit the report settings if necessary.

     Click **[!UICONTROL Next]** to move between the setting sections.
  
  1. Enable the **[!UICONTROL Save as Template]** setting.
  
  1. Click **[!UICONTROL Create]**.

## Preview or save a report

You can preview a report in the web browser, or open or save the report data as a [!DNL Microsoft Excel] workbook, a tab-separated values (TSV) file, a comma-separated values (CSV) file, or (some report types) a [!DNL Microsoft Excel] tabbed workbook.

>[!NOTE]
>
>Adobe Account Team members and some administrator users can view reports created by advertiser and agency users.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**, which opens to the **[!UICONTROL Latest Reports]** tab.

1. Do either of the following:

   * (To view a report in the web browser) Do either of the following:
  
     * Hold the cursor over the template row, and click **...** > **[!UICONTROL Preview]**.
     
     * Select the check box next to the existing template. In the bulk actions toolbar, click **[!UICONTROL Preview]**.
   
   * (To open or save the report data in a file) In the [!UICONTROL Export] column next to the report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

     * **[!UICONTROL XLS]:**   For an [!DNL Excel] workbook with a single worksheet (XLSX format). The report includes one worksheet that's labeled at the top with the parameters, with one row for each component reported when data for the component is available. Rows with no data are omitted.
     
       Basic reports include a total for each numeric column.
       
     * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each component reported.
     
     * **[!UICONTROL CSV]:**   For a CSV file. The report includes the parameters and one row for each component reported.

## Delete reports

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**, which opens to the **[!UICONTROL Latest Reports]** tab.

1. Do either of the following:

   * (To delete a single report):

     1. Hold the cursor over the report row, and click **...** > **[!UICONTROL Run]**.

     1. In the confirmation message, click **[!UICONTROL Confirm]**.
   
   * (To delete one or more reports):

     1. Select the check box next to each report that you want to delete.

     1. In the bulk actions toolbar, click [Delete](/help/search-social-commerce/assets/delete-new.png "Delete") **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
