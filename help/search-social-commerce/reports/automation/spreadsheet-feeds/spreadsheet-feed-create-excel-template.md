---
title: Create an [!DNL Excel] template for a spreadsheet report feed
description: Learn how to create specially formatted spreadsheet templates.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
---
# Create an [!DNL Excel] template for a spreadsheet report feed

*For basic reports and model accuracy reports only*

To create spreadsheet feeds, you must first create specially formatted [!DNL Microsoft Excel] spreadsheet templates using regular report templates. You optionally can customize the [!DNL Excel] spreadsheet to include additional columns and graphs.

1. In **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]**, generate the desired report type using a [!UICONTROL Date Aggregation] unit of "[!UICONTROL Daily]" and with all other data parameters you want, saving the report as a template.

   >[!NOTE]
   >
   > * You can create spreadsheet feeds for [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], and [!UICONTROL Forecast Accuracy] reports. If you use the [!UICONTROL Ad Group Report], limit the number of ad groups included for quicker results.
   > * The [!UICONTROL Date Range] unit defined in the template isn't used. You'll define the dates for which to refresh data when you configure the spreadsheet feed later.

1. After the report is generated, go to **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]** and export a TSV or XLS version of the report output to a file.

1. In [!DNL Excel], create a custom template for the report:

   1. Open the report file in [!DNL Excel].
   
   1. Prepare the workbook:
      
      1. Delete the top rows that show the report parameters. For XLS files, also delete the "[!UICONTROL Total]" row. You can optionally delete some of the data rows, but keep a) the data header row with all columns in the original order and b) at least one data row. Don't manually add any data.
       
         >[!NOTE]
         >
         > The final column must include non-zero values.
       
       2. Sort the data by start date in ascending order (from the oldest to the most recent).
       
       3. Change the worksheet tab name from "[!UICONTROL Sheet1]" to "[!UICONTROL RAW]."
          
          This specific tab name enables the data to be refreshed.
          
       4. (Optional) Add custom columns to the right of the columns from the report template, as necessary.

   1. (Optional) On a separate worksheet, create a pivot table. After you are done, right-click in any cell of the pivot table and select **[!UICONTROL Pivot Table Options]**, click the **[!UICONTROL Data]** tab, and then select **[!UICONTROL Refresh data when opening the file]**.
   
   1. Save the file as an [!DNL Excel] spreadsheet in .XLSX format.

>[!MORELIKETHIS]
>
>* [About spreadsheet report feeds](spreadsheet-feed-about.md)
>* [Create a spreadsheet report feed](spreadsheet-feed-create.md)
>* [Edit spreadsheet report feed settings](spreadsheet-feed-edit.md)
>* [Spreadsheet report feed settings](spreadsheet-feed-settings.md)
>* [View or save a spreadsheet report feed file](spreadsheet-feed-view-or-save.md)
>* [Manually refresh spreadsheet report feeds](spreadsheet-feed-refresh.md)
>* [Delete spreadsheet report feeds](spreadsheet-feed-delete.md)
