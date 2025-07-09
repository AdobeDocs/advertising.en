---
title: Post campaign data generated from feeds to ad networks
description: Learn how to post data generated from inventory data feeds to ad networks.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
---
# Post campaign data generated from feeds to ad networks

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

You can post campaign data generated from a feed as you propagate the data through the associated templates or as a separate process. Once you post data, any existing propagated data is removed from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] lists.

For a successful posting, all ad groups must be assigned to campaigns, all keywords and ads must be assigned to ad groups, and all required information must be included without any length violations.

* If you used the option to "[!UICONTROL Propagate and Preview]," then [post the generated bulksheet file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (named "`<feed file name>_<template name>`") from the [!UICONTROL Bulksheets] view.

  If you didn't previously [validate your landing pages](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), then you can do so before you post the file.

* If you used the option to "[!UICONTROL Propagate only]," then you can post the generated data for components with the [[!UICONTROL New] status](propagated-data-status.md) within a campaign hierarchy view from the [!UICONTROL Templates] tab.

  >[!NOTE]
  >
  >Active or deleted components may include subcomponents that are new, and the subcomponents can be posted if the data is valid.

  >[!TIP]
  >
  >If you didn't previously validate your landing pages and want to do so, then [propagate data and preview it](feed-data-propagate.md) from the [!UICONTROL Bulksheets] view instead of posting it to the ad network. You can then [validate the URLs](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) before manually posting the file to the ad network.

  1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.
  
  1. Select the check box next to the template.
  
  1. In the toolbar, click **[!UICONTROL Post]**.

  1. In the posting settings, enter or select information in the fields, and then click **[!UICONTROL Post]**.

     * **[!UICONTROL Selection]:** Which account components are posted.
     
     * **[!UICONTROL Scheduling]:** When to post the file:
     
       * *[!UICONTROL Post to search engine now]* (the default): Creates a bulk sheet file from the propagated feed data and begins posting it immediately.
       
       * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Creates a bulksheet file and posts it later. Specify the following:
       
         * **[!UICONTROL Start Time]:** A future date and time on which the bulksheet file should be posted to the ad network. By default, the file is sent at 00:00 (12:00 a.m.) on the next day. **Note:** For large files that require longer processing, the posted data isn't available immediately within the campaign management views or within the network's ad manager.

         * **[!UICONTROL End Time]:** A future date and time at which the posted ads may be paused or deleted based on the [feed data setting](feed-settings-manage.md#feed-data-settings) for "[!UICONTROL When the Scheduled End Date is reached]." By default, the end time is at 00:00 (12:00 a.m.) 30 days from today. Select **[!UICONTROL None]** to keep the data active indefinitely (or until you propagate new data for the template), or specify a date and time.
         
           To specify a date, use the format DD/MM/YYYY or D/M/YYYY or click ![Calendar](/help/search-social-commerce/assets/calendar.png "Calendar") to open the calendar and [select a date](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). To change a time, enter the time in the 24-hour format HH/MM or H/M or select a time (in 30-minute intervals) from the list.

       * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Creates a bulk sheet file that's available from the [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] view. You can optionally post the file from there.
       
         When the resulting bulksheet file is more than 2 MB, the file is in ZIP format. You don't need to unzip the file to post it.

     * **[!UICONTROL Generate Tracking URLs]:** Whether to include tracking URLs for keywords and ad variations in the bulksheet file: *[!UICONTROL Yes]* (the default) or *[!UICONTROL No]*.
     
       If you select *[!UICONTROL Yes]*, then the URLs are generated from the base URLs for the keywords and ads according to the [!UICONTROL Tracking Methods] parameters in the [account settings](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) or, if you're mapping data to existing campaigns, to the [!UICONTROL Tracking Methods] parameters in the existing [campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).
     
       If tracking URLs exist for the relevant items, then they aren't regenerated unless new ones are needed (such as if the keyword match type, the creative text, or the account's tracking parameters have changed).

     * **[!UICONTROL Bulksheet Name]:** The name of the bulksheet file to create from the propagated feed data. By default, the file is named `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. You can rename the file as you like, but it must end with one of the following file extensions: `.tsv` (for tab-separated values), `.txt` (for ASCII text), `.csv` (for comma-separated values), or `.zip` (for a compressed TSV file). For data that includes international characters, use TSV or TXT format.

       The posted file is available in the [!UICONTROL Bulksheets] view for 30 days, whether or not you post it to the ad network.

The "[!UICONTROL Last Prop. Status]" column shows the job status for the applicable templates.

When the bulksheet is created, it's listed in the [!UICONTROL Bulksheets] view. When the file is posted, an email notification is sent with a link to the file. However, if all or some of the data can't be posted, then an error file is listed in the [!UICONTROL Bulksheets] view, and an email notification is sent with a link to the error file.

>[!NOTE]
>
>* Regardless of the scheduling option you selected, the specified data is removed from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] lists.
>* Large amounts of data take longer to be processed. You can follow the progress of the file during the process.
>* All posted data is subject to the network's editorial process.
>* Before a bulksheet file is posted, you can [cancel the posting](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [About inventory feeds](inventory-feeds-about.md)
>* [View data generated from feeds](propagated-data-view.md)
>* [Edit data generated from feeds](propagated-data-edit.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
>* [Statuses of data generated from feeds](propagated-data-status.md)
