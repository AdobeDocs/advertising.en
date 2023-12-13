---
title: Spreadsheet report feed settings
description: Learn about the settings for spreadsheet feeds.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
---
# Spreadsheet report feed settings

| Field | Description |
|---|---|
| [!UICONTROL Feed Name] | A name for the spreadsheet feed. |
| [!UICONTROL Report Template] | The report template that specifies the required report data; select the one you used to create the [!DNL Excel] template. All basic report templates are listed.<br><br><b>Note:</b> If you change the report template used for the report, or you update the columns in the template, then you must create and upload a new [!DNL Excel] template. |
| [!UICONTROL Excel Template] | The specially formatted [!DNL Excel] template that you created in .XLSX format, which is applied to data specified in the report template. Specify the file to upload either by entering the full path and file name or by clicking <b>[!UICONTROL Browse]</b> to locate the file on your device or network. |
| [!UICONTROL Back Fill From] | The beginning date for which existing data on the [!UICONTROL RAW] tab is refreshed, represented by a number of days in the past. Enter a value of up to 90 days; the default is seven (7) days.<br><br>For example, if the value is 7, and today is March 7, then the existing data on the [!UICONTROL RAW] tab beginning with March 1 is refreshed (up until the end date specified by the [!UICONTROL Back Fill Until] parameter). Existing rows of data for dates before March 1 aren't deleted, but they aren't refreshed. |
| [!UICONTROL Back Fill Until] |The end date for which existing data on the [!UICONTROL RAW] tab is refreshed, represented by a number of days in the past. The default value is one (1) day.<br><br>For example, if this value is 1, and today is March 7, then the existing data on the [!UICONTROL RAW] tab is refreshed up to March 6 (and beginning with the start date specified by the [!UICONTROL Back Fill From] parameter). If this value is 1, the [!UICONTROL Back Fill Until] parameter is 7, and today is March 7, then the existing data on the [!UICONTROL RAW] tab is refreshed from March 1 through March 6. In both examples, existing rows of data for dates after March 6 aren't deleted, but they aren't refreshed. |
| [!UICONTROL Email Recipients] | Email addresses at which to send notifications each time the report is refreshed, or each time the report is run when the template includes a schedule. By default, the address for your user account is entered. To specify multiple addresses, separate them with commas, spaces, or new lines. |
| [!UICONTROL Schedule Time] | The time at which spreadsheet feeds are refreshed: either at 08:00 or at any hour between 10:00 and 23:00 in the advertiser’s time zone. The default for new spreadsheet feeds is 10:00.<br><br><b>Note:</b> For performance reasons, you can't refresh spreadsheet feeds at 09:00, when other reports are generated. |
| [!UICONTROL Email Notification] | (When Email Recipients are specified) What to include in email notifications to any specified addresses:<ul><li><i>Attach feed</i> &mdash; To send a copy of the completed report in XLSX format. If the file is greater than 10 MB, then the notification doesn't include an attachment.</li><li><i>Notification only</i> (the default) &mdash; To send only a notification of the report completion or failure, with a link to the report.</li></ul> |

>[!MORELIKETHIS]
>
>* [About spreadsheet report feeds](spreadsheet-feed-about.md)
>* [Create a spreadsheet report feed](spreadsheet-feed-create.md)
>* [Create an [!DNL Excel] template for a spreadsheet report feed](spreadsheet-feed-create-excel-template.md)
>* [Edit spreadsheet report feed settings](spreadsheet-feed-edit.md)
>* [View or save a spreadsheet report feed file](spreadsheet-feed-view-or-save.md)
>* [Manually refresh spreadsheet report feeds](spreadsheet-feed-refresh.md)
>* [Delete spreadsheet report feeds](spreadsheet-feed-delete.md)
