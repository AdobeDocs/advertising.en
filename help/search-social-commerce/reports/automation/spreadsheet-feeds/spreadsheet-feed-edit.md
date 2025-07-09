---
title: Edit spreadsheet report feed settings
description: Learn how to edit the settings for spreadsheet feeds.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
---
# Edit spreadsheet report feed settings

*For basic reports and model accuracy reports only*

You can change which report template, [!DNL Microsoft Excel] template, and other parameters  are used for a spreadsheet feed.

>[!NOTE]
>
> If you edit the columns in the report template or use a new or updated report template, then you must update the [!DNL Excel] template accordingly and upload it again.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Insights & Reports] > [!UICONTROL Spreadsheet Feeds]**.

1. (Optional) To update the report template or the [!DNL Excel] template used for the spreadsheet feed:

   * (Optional) To use a different or updated report template for the feed, [create a new [!DNL Excel] template for the report template](spreadsheet-feed-create-excel-template.md).
     
     You'll need to upload both the report template and the new [!DNL Excel] file in the next step.
   
   * (Optional) To simply add custom columns to the [!DNL Excel] template, insert the columns to the right of the columns from the report template, and then save the file as an [!DNL Excel] spreadsheet in .XLSX format. You'll need to upload the new [!DNL Excel] file in the next step.

1. Change the spreadsheet feed settings:
   
   * In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds]**.
   
   * Next to the spreadsheet feed name, click ![View/edit settings button](/help/search-social-commerce/assets/settings.png "View/edit settings button").
   
   * In the [!UICONTROL Edit Spreadsheet Feed] dialog, change the [spreadsheet feed settings](spreadsheet-feed-settings.md).
   
   * Click **[!UICONTROL Submit]**.
   
   * (Optional) Once the feed's [!UICONTROL Update Status] is *[!UICONTROL Finished]*, click **[!UICONTROL XLSX]** next to the feed, and then open or save the file according to your browser's normal procedure.

     >[!NOTE]
     >
     > If the report template associated with the feed is later deleted, then the feed is also deleted.

      Spreadsheet feeds are automatically refreshed at 08:00 each day in the advertiser's time zone. If the report template includes addresses for any email recipients, then those addresses receive notifications when the spreadsheet is refreshed.

>[!MORELIKETHIS]
>
>* [About spreadsheet report feeds](spreadsheet-feed-about.md)
>* [Create a spreadsheet report feed](spreadsheet-feed-create.md)
>* [Create an [!DNL Excel] template for a spreadsheet report feed](spreadsheet-feed-create-excel-template.md)
>* [Edit spreadsheet report feed settings](spreadsheet-feed-edit.md)
>* [Spreadsheet report feed settings](spreadsheet-feed-settings.md)
>* [View or save a spreadsheet report feed file](spreadsheet-feed-view-or-save.md)
>* [Manually refresh spreadsheet report feeds](spreadsheet-feed-refresh.md)
