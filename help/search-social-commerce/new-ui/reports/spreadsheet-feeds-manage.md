---
title: (New UI) Manage spreadsheet report feeds
description: Learn how to create, configure, refresh, view, and delete spreadsheet report feeds that deliver daily performance data in a custom-formatted spreadsheet.
feature: Search Reports
---
# (New UI) Manage spreadsheet report feeds

*For basic reports and model accuracy reports only*

<!-- Update link to notifications once available -->

Spreadsheet feeds provide daily performance data for all basic reports and model accuracy reports in a custom spreadsheet format in [!DNL Microsoft Excel] XLSX. You can set up spreadsheet feeds using specially formatted [!DNL Excel] spreadsheet templates that you create from regular report templates. Each day, the spreadsheet is automatically refreshed at a specified time with new, raw data that is aggregated daily. The raw data populates any columns and graphs that you've included in the spreadsheet template. Once a spreadsheet feed file is available, or if the file generation fails, each email recipient in the report template receives notification, based on the user's configured [notification settings for reports](/help/search-social-commerce/notifications/notification-about.md).

You can configure the feed to refresh up to the last 90 days of data, and all previous existing data remains, continuing to accumulate.

The [!UICONTROL Reports] > [!UICONTROL Spreadsheets Feeds] view lists all spreadsheet feeds that you have created. From this view, you can create spreadsheet feeds, manually refresh a feed, or delete a feed.

## Available actions

* [Create an [!DNL Excel] template for a spreadsheet report feed](#spreadsheet-feed-create-excel-template)

* [Create a spreadsheet report feed](#spreadsheet-feed-create)

* [Edit spreadsheet report feed settings](#spreadsheet-feed-edit)

* [View or save a spreadsheet report feed file](#spreadsheet-feed-view-or-save)

* [Manually refresh spreadsheet report feeds](#spreadsheet-feed-refresh)

* [Delete spreadsheet report feeds](#spreadsheet-feed-delete)

## Create an [!DNL Excel] template for a spreadsheet report feed {#spreadsheet-feed-create-excel-template}

<!-- Add x-refs when available -->

To create spreadsheet feeds, you must first create specially formatted [!DNL Microsoft Excel] spreadsheet templates using regular report templates. You optionally can customize the [!DNL Excel] spreadsheet to include additional columns and graphs.

1. In **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]**, generate the desired report type using a [!UICONTROL Date Aggregation] unit of "[!UICONTROL Daily]" and with all other data parameters you want, saving the report as a template.

   >[!NOTE]
   >
   > * You can create spreadsheet feeds for [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], and [!UICONTROL Forecast Accuracy] reports. If you use the [!UICONTROL Ad Group Report], limit the number of ad groups included for quicker results.
   > * The [!UICONTROL Date Range] unit defined in the template isn't used. You'll define the dates for which to refresh data when you configure the spreadsheet feed later.

1. After the report is generated, go to **[!UICONTROL Reports] > [!UICONTROL Scheduled Reports]** and export a TSV or XLS version of the report output to a file.

1. In [!DNL Excel], create a custom template for the report:

   1. Open the report file in [!DNL Excel].
   
   1. Prepare the workbook:
      
      1. Delete the top rows that show the report parameters. For XLS files, also delete the "[!UICONTROL Total]" row. You can optionally delete some of the data rows, but keep a) the data header row with all columns in the original order and b) at least one data row. Don't manually add any data.
       
         >[!NOTE]
         >
         > The final column must include non-zero values.
       
      1. Sort the data by start date in ascending order (from the oldest to the most recent).
       
      1. Change the worksheet tab name from "[!UICONTROL Sheet1]" to "[!UICONTROL RAW]."
          
          This specific tab name enables the data to be refreshed.
          
      1. (Optional) Add custom columns to the right of the columns from the report template, as necessary.

   1. (Optional) On a separate worksheet, create a pivot table. After you are done, right-click in any cell of the pivot table and select **[!UICONTROL Pivot Table Options]**, click the **[!UICONTROL Data]** tab, and then select **[!UICONTROL Refresh data when opening the file]**.
   
   1. Save the file as an [!DNL Excel] spreadsheet in .XLSX format.

## Create a spreadsheet report feed {#spreadsheet-feed-create}

1. [Create the [!DNL Excel] template to populate with the report data](#spreadsheet-feed-create-excel-template).

1. Create the spreadsheet feed:
   
   1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.
   
   1. In the upper right, click **[!UICONTROL Create Spreadsheet]**.
   
   1. In the **[!UICONTROL Create Spreadsheet Feed]** dialog, specify the [spreadsheet feed settings](#spreadsheet-feed-settings).
   
   1. Click **[!UICONTROL Submit]**.
   
   1. (Optional) Once the feed's [!UICONTROL Update Status] is *[!UICONTROL Finished]*, click **[!UICONTROL XLSX]** next to the feed, and then open or save the file according to your browser's normal procedure.

      >[!NOTE]
      >
      >If the report template associated with the feed is later deleted, then the feed is also deleted.

      The spreadsheet feeds are automatically refreshed each day at the configured [!UICONTROL Schedule Time]. If the report template includes addresses for any email recipients, then those addresses receive notifications when the spreadsheet is refreshed.

## Edit spreadsheet report feed settings {#spreadsheet-feed-edit}

>[!NOTE]
>
> If you edit the columns in the report template or use a new or updated report template, then you must update the [!DNL Excel] template accordingly and upload it again.

1. (Optional) To update the report template or the [!DNL Excel] template used for the spreadsheet feed:

   * (Optional) To use a different or updated report template for the feed, [create a new [!DNL Excel] template for the report template](#spreadsheet-feed-create-excel-template).
     
     You'll upload both the report template and the new [!DNL Excel] file in the next steps.
   
   * (Optional) To simply add custom columns to the [!DNL Excel] template, insert the columns to the right of the columns from the report template, and then save the file as an [!DNL Excel] spreadsheet in .XLSX format. You'll need to upload the new [!DNL Excel] file in the next step.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.

1. Change the spreadsheet feed settings:
   
   1. Select the check box next to the spreadsheet feed name.
   
   1. In the bulk actions toolbar, click **[!UICONTROL Edit]**.
   
   1. In the [!UICONTROL Create Spreadsheet Feed]<!-- sic --> dialog, change the [spreadsheet feed settings](#spreadsheet-feed-settings).
   
   1. Click **[!UICONTROL Submit]**.
   
   1. (Optional) Once the feed's [!UICONTROL Update Status] is *[!UICONTROL Finished]*, click **[!UICONTROL XLSX]** next to the feed, and then open or save the file according to your browser's normal procedure.

     >[!NOTE]
     >
     > If the report template associated with the feed is later deleted, then the feed is also deleted.

      Spreadsheet feeds are automatically refreshed at 08:00 each day in the advertiser's time zone. If the report template includes addresses for any email recipients, then those addresses receive notifications when the spreadsheet is refreshed.

## Spreadsheet report feed settings {#spreadsheet-feed-settings}

| Field | Description |
|---|---|
| [!UICONTROL Feed Name] | A name for the spreadsheet feed. |
| [!UICONTROL Report Template] | The report template that specifies the required report data; select the one you used to create the [!DNL Excel] template. All basic report templates are listed.<br><br><b>Note:</b> If you change the report template used for the report, or you update the columns in the template, then you must create and upload a new [!DNL Excel] template. |
| [!UICONTROL Excel Template] | The specially formatted [!DNL Excel] template that you created in .XLSX format, which is applied to data specified in the report template. Specify the file to upload either by entering the full path and file name or by clicking <b>[!UICONTROL Browse]</b> to locate the file on your device or network. |
| [!UICONTROL Back Fill From] | The beginning date for which existing data on the [!UICONTROL RAW] tab is refreshed, represented by a number of days in the past. Enter a value of up to 90 days; the default is seven (7) days.<br><br>For example, if the value is 7, and today is March 7, then the existing data on the [!UICONTROL RAW] tab beginning with March 1 is refreshed (up until the end date specified by the [!UICONTROL Back Fill Until] parameter). Existing rows of data for dates before March 1 aren't deleted, but they aren't refreshed. |
| [!UICONTROL Back Fill Until] |The end date for which existing data on the [!UICONTROL RAW] tab is refreshed, represented by a number of days in the past. The default value is one (1) day.<br><br>For example, if this value is 1, and today is March 7, then the existing data on the [!UICONTROL RAW] tab is refreshed up to March 6 (and beginning with the start date specified by the [!UICONTROL Back Fill From] parameter). If this value is 1, the [!UICONTROL Back Fill Until] parameter is 7, and today is March 7, then the existing data on the [!UICONTROL RAW] tab is refreshed from March 1 through March 6. In both examples, existing rows of data for dates after March 6 aren't deleted, but they aren't refreshed. |
| [!UICONTROL Email Recipients] | Email addresses at which to send notifications each time the report is refreshed, or each time the report is run when the template includes a schedule. By default, the address for your user account is entered. To specify multiple addresses, separate them with commas, spaces, or new lines. |
| [!UICONTROL Schedule Time] | The time at which spreadsheet feeds are refreshed: either at 08:00 or at any hour between 10:00 and 23:00 in the advertiser's time zone. The default for new spreadsheet feeds is 10:00.<br><br><b>Note:</b> For performance reasons, you can't refresh spreadsheet feeds at 09:00, when other reports are generated. |
| [!UICONTROL Email Notification] | (When Email Recipients are specified) What to include in email notifications to any specified addresses:<ul><li><i>[!UICONTROL Attach feed]</i> &mdash; To send a copy of the completed report in XLSX format. If the file is greater than 10 MB, then the notification doesn't include an attachment.</li><li><i>[!UICONTROL Notification Only]</i> (the default) &mdash; To send only a notification of the report completion or failure, with a link to the report.</li></ul> |

## View or save a spreadsheet report feed file {#spreadsheet-feed-view-or-save}

You can view any generated spreadsheet feed or save it to a file. Spreadsheet feed files are in [!DNL Microsoft Excel] XLSX format.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.

1. Click **[!UICONTROL XLSX]** next to the feed, and then open or save the file according to your browser's normal procedure.

## Manually refresh spreadsheet report feeds {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Spreadsheet feeds are automatically refreshed at 08:00 each day in the local time zone.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.

1. Select the check box next to each feed that you want to refresh.

1. In the bulk actions toolbar, click **[!UICONTROL Run Spreadsheet]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

1. (Optional) Once a feed's [!UICONTROL Update Status] is *[!UICONTROL Finished]*, click **[!UICONTROL XLSX]** next to the feed, and then open or save the file according to your browser's normal procedure.

## Delete spreadsheet report feeds {#spreadsheet-feed-delete}

>[!NOTE]
>
>If the report template associated with a feed is deleted, then the feed is automatically deleted.

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.

1. Select the check box next to each feed that you want to delete.

1. In the bulk actions toolbar, click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.
