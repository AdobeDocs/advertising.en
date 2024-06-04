---
title: Edit data generated from feeds
description: Learn how to edit data generated from inventory data feeds.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
---
# Edit data generated from feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

When you propagate feed data without simultaneously posting it to the ad network, you can edit the data in either of the following ways. You later can optionally [post data](propagated-data-post.md) from either location to the relevant ad networks:

* If you used the option to "[!UICONTROL Propagate and Preview]," then you can edit the generated bulksheet file (named "`<feed file name>_<template name>`") by downloading it from the [!UICONTROL Bulksheets] view, editing the file, and uploading it again. No data is included on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs.

* If you used the option to "[!UICONTROL Propagate only]," then you can edit the generated data for components with the [[!UICONTROL New] status](propagated-data-status.md) within a campaign hierarchy view from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs.

  The campaign hierarchy views show only the data generated from the feed file, not the existing account components. After data for a component and all of its subcomponents is posted to the ad network, it's no longer listed in the campaign hierarchy.
  
  1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.
  
  1. (Optional) To show only campaign components created for a specific template:
  
     1. Click the template name.
     
     1. In the [!UICONTROL Accounts] menu in the left navigation pane, expand the ad network node and the ad network account node, and then select the check box next to the template name.

  1. Click the **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, or **[!UICONTROL Ads]** tab, depending on which components that you want to view.
   
     >[!NOTE]
     >
     >* Unless you view data for a specific template, the [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs list all ad groups, keywords, and ads created from all templates and feed files. Product groups used for [!DNL Google Ads] shopping ads are listed on the [!UICONTROL Keywords] tab.
     >* To view only the subcomponents of a specific campaign, start by viewing the [!UICONTROL Campaigns] tab. Similarly, to view only the subcomponents of a specific ad group, start by viewing the [!UICONTROL Ad Groups] tab.

  1. (Optional; to edit ad groups, keywords, or ads only) Filter the list to include only the subcomponents of a specific campaign or ad group:

     * To list all ad groups in a campaign, click the campaign name.
     
     * To list all keywords in an ad group, click the ad group name.

     * To list all as in an ad group, click the ad group name, and then click the [!UICONTROL Ads] tab.

  1. Click [View/edit settings icon](/help/search-social-commerce/assets/settings.png "View/edit settings icon") next to the campaign, ad group, keyword, or ad name.
  
  1. Edit the settings, and then click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [About inventory feeds](inventory-feeds-about.md)
>* [View data generated from feeds](propagated-data-view.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
>* [Statuses of data generated from feeds](propagated-data-status.md)
