---
title: Generate a basic report or advanced report
description: Learn how to generate a customized basic or advanced report.
exl-id: cad5183c-cd21-439a-ab3e-033b2bb187ec
feature: "Search Reports, Search Basic Reports, Search Advanced Reports"
---
# Generate a basic report or advanced report

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]**.

1. In the toolbar above the data table, click **[!UICONTROL Create Report]**, hold the cursor over **[!UICONTROL Basic Reports]** or **[!UICONTROL Advanced Reports]**, and then click the [report type](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md).

1. (Optional) In the [!UICONTROL Report Settings] window, change the default [report settings](basic-advanced-report-settings.md):

   1. (Optional) Enter a custom name for the report and for the template (if you save the report as a template).

   1. (Optional) To save the report settings as a template, select the check box next to **[!UICONTROL Save as template]**.

   1. (Optional) On the **[!UICONTROL Basic Settings]** tab, select an existing report template to use or change the default basic settings for the report.

   1. (Optional) Click the **[!UICONTROL Columns tab]**, and change the default columns in the report.
   
      By default, all monetary data in reports is shown in the format for US dollars (such as 1,000.00). To display the value in the correct currency format (but without any currency symbols in CSV and TSV formats), add the "[!UICONTROL Currency]" column to the report. If the report includes data for accounts with different currencies, then any "[!UICONTROL Total]" monetary values are the sum of all numbers in the column, regardless of currency.

   1. (Optional; [!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], and [!UICONTROL Label Classification Report] only) Click the **[!UICONTROL Classifications]** tab, and limit the report results to include only specific label classifications.
   
   1. (Optional) Click the **[!UICONTROL Advanced Filters]** tab, and change the default advanced options.

   1. (Optional) Click the **[!UICONTROL Attribution]** tab, and change the default attribution rule.

   1. (Optional) Click the **[!UICONTROL Scheduling and Delivery]** tab, and change the default scheduling and delivery options.

1. (Optional when available) To preview the first 50 lines of the report, click **[!UICONTROL Preview]**. When you're finished, click **[!UICONTROL Back]** to return to the report settings page.

   >[!NOTE]
   >
   >The Preview button is available for all basic and advanced reports except for the [!UICONTROL Campaign Hourly Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report], [!UICONTROL Domain Referral Report], and [!UICONTROL Transaction Report].

1. Click **[!UICONTROL Create]**.

If you didn't specify a report schedule, then the report is run immediately; otherwise, it's run according to the specified schedule. The report name is added to the [[!UICONTROL Latest Reports] view](/help/search-social-commerce/reports/report-about.md). If you saved the report as a template, then it's also added to the [[!UICONTROL Templates] view](/help/search-social-commerce/reports/report-about.md). When the report is completed, the file is available to open or save; templates are available immediately.

If you entered any email addresses for notification, each recipient receives a notification when the report job is completed or fails, based on the user's [configured notification settings](/help/search-social-commerce/notifications/notification-edit.md) for reports.

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [Delete reports](/help/search-social-commerce/reports/management/report-delete.md)
