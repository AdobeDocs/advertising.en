---
title: Propagate inventory feed data through templates
description: Learn about propagating data from your inventory feeds through ad templates to manage account structure and deliver dynamic ads.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
---
# Propagate inventory feed data through templates

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

After you create an ad network-specific feed template and associate a feed file or a [!DNL Google] or [!DNL Microsoft] merchant center account with it, you can dynamically create ads by propagating the feed data through the template according to the [feed data settings](feed-settings-manage.md). During propagation, the column names in the template are replaced with data values in the feed, and the generated campaigns and their components have the default settings unless the template specifies otherwise. Depending on the template options, Search, Social, & Commerce either creates new account structure (campaigns, ad groups, keywords) for the ads or maps the ads to the existing account structure.

When new feed data contains new data values for an item, or the template has changed, existing ads are deleted and new ones are created. If the only change is the designation of [!DNL Google Ads] Param 1 and Param 2, then only those values are updated. Duplicate ads (the same ad copy and landing page) are never created.

When you propagate data, you can optionally preview the generated data within a campaign hierarchy view, generate a bulksheet file for review, or generate a bulksheet file for immediate posting to the ad network. When each propagation action is completed, a propagation summary is added to the Propagations tab, indicating the number of each entity type that was or would be created, paused, or deleted based on the propagation. If you don't post the data immediately, then you can preview it and post it later.

## Propagate feed files from the [!UICONTROL Templates] tab

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. Select the check box next to the templates to propagate.

1. In the toolbar, click **[!UICONTROL Propagate]**, and then select one of the following options:

   * **[!UICONTROL Propagate Only]:** To show the propagated data on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs. You can still post the data for any component and its subcomponents later from the [!UICONTROL Templates] tab.
   
   * **[!UICONTROL Propagate and Preview]:** To create a bulksheet file (named "`<feed file name>_<template name>`"), which is available in the [!UICONTROL Bulksheets] view for review (but not on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs). You can later post the bulksheet file from the [!UICONTROL Bulksheets] view.

     When the resulting bulksheet file is more than 2 MB, the file is in ZIP format. You don't need to unzip the file to post it.

   * **[!UICONTROL Propagate and Post to SE]:** To create a bulksheet file (named "`<feed file name>_<template name>`") that is immediately queued for posting to the ad network. The bulksheet file is available in the [!UICONTROL Bulksheets] view, but it isn't available on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs.
   
     When the resulting bulksheet file is more than 2 MB, the file is in ZIP format.

   The "Last Prop. Status" column shows the job status for the applicable templates.
   
   When each propagation action is completed, a propagation summary is added to the [!UICONTROL Propagations] tab, indicating the number of each entity type that was or would be created, paused, or deleted based on the propagation. The estimate doesn't include changes made from within the ad network's own ad editor.

## Propagate feed files from the [!UICONTROL Feeds] list

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. In the toolbar above the data table, click **[!UICONTROL Feeds]**.

1. Select the check box next to the feed file.

1. Above the data table, click **[!UICONTROL Propagate/Post Feed Data]**, and then select one of the following options:

   * **[!UICONTROL Propagate Only]:** To show the propagated data on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs. You can still post the data for any component and its subcomponents later from the [!UICONTROL Templates] tab.
   
   * **[!UICONTROL Propagate and Preview]:** To create a bulksheet file (named "`<feed file name>_<template name>`"), which is available in the [!UICONTROL Bulksheets] view for review (but not on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs). You can later post the bulksheet file from the [!UICONTROL Bulksheets] view.

     When the resulting bulksheet file is more than 2 MB, the file is in ZIP format. You don't need to unzip the file to post it.

   * **[!UICONTROL Propagate and Post to SE]:** To create a bulksheet file (named "`<feed file name>_<template name>`") that is immediately queued for posting to the ad network. The bulksheet file is available in the [!UICONTROL Bulksheets] view, but it isn't available on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs.
   
     When the resulting bulksheet file is more than 2 MB, the file is in ZIP format.

1. In the pop-up window, select the check box next to each template through which you want to propagate data from the feed file, and then click **[!UICONTROL Propagate Feed]**.

   All templates associated with the file are listed.

The [!UICONTROL Templates] tab opens, and the "[!UICONTROL Last Prop. Status]" column shows the job status for the applicable templates.

When each propagation action is completed, a propagation summary is added to the [!UICONTROL Propagations] tab, indicating the number of each entity type that was or would be created, paused, or deleted based on the propagation. The estimate doesn't include changes made from within the ad network's own ad editor.

## View a propagation summary

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**.

1. Click the **[!UICONTROL Propagations]** tab.

1. Next to the template name, click ![View/edit settings icon](/help/search-social-commerce/assets/settings.png "View/edit settings icon") .

## Stop a propagation job

You can stop a propagation job for inventory feed data while the job is still queued.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.

1. In the "[!UICONTROL Last Prop. Status]" column next to the template name, click **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [About inventory feeds](inventory-feeds-about.md)
>* [Manage ad templates for inventory feeds](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [View data generated from feeds](propagated-data-view.md)
>* [Edit data generated from feeds](propagated-data-edit.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
>* [Statuses of data generated from feeds](propagated-data-status.md)
