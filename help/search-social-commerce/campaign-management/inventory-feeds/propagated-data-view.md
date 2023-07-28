---
title: View data generated from feeds
description: Learn how to view data generated from inventory data feeds.
exl-id: 961155ac-a9d3-42e4-904b-b968e9f3383b
feature: Search Inventory Feeds
---
# View data generated from feeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (delete actions only), and [!DNL Yandex] accounts only*

When you propagate feed data without simultaneously posting it to the ad network, you can preview the data in one of the following ways. You later can optionally [post data](propagated-data-post.md) from either location to the relevant ad networks.

* If you used the option to "[!UICONTROL Propagate and Preview]," then view the generated bulksheet (named "`<feed file name>_<template name>`") from the [!UICONTROL Bulksheets] view. No data is included on the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs. This option allows you to [validate the landing pages](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associated with the ads and keywords before you post the data.

* If you used the option to "[!UICONTROL Propagate only]," then view the generated data within a campaign hierarchy view from the [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs.

  The campaign hierarchy views show only the data generated from the feed file, not the existing account components. After data for a component and all of its subcomponents is posted to the ad network, it's no longer listed in the campaign hierarchy vie.

  1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)]**, which opens to the [!UICONTROL Templates] tab.
  
  1. (Optional) To show only campaign components created for a specific template:
  
     1. Click the template name.
     
     1. In the [!UICONTROL Accounts] menu in the left navigation pane, expand the ad network node and the ad network account node, and then select the check box next to the template name.

  1. Click the **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, or **[!UICONTROL Ads]** tab, depending on which components that you want to view.
   
     >[!NOTE]
     >
     >* Unless you view data for a specific template, the [!UICONTROL Ad Groups], [!UICONTROL Keywords], and [!UICONTROL Ads] tabs list all ad groups, keywords, and ads created from all templates and feed files. Product groups used for [!DNL Google Ads] shopping ads are listed on the [!UICONTROL Keywords] tab.
     >* To view only the subcomponents of a specific campaign, start by viewing the [!UICONTROL Campaigns] tab. Similarly, to view only the subcomponents of a specific ad group, start by viewing the [!UICONTROL Ad Groups] tab.

  1. (Optional) To view further information, do either of the following:
   
      * To view the settings for any campaign, ad group, keyword, or ad, click [View/edit settings icon](/help/search-social-commerce/assets/settings.png "View/edit settings icon") next to the name.
      
      * To view the subcomponents of a campaign or ad group, do the following:
      
        * To list all ad groups in a campaign, click the campaign name.
        
        * To list all keywords or product targets in an ad group, click the ad group name.
        
        * To list all ads in an ad group, click the ad group name, and then click the [!UICONTROL Ads] tab.

>[!MORELIKETHIS]
>
>* [About inventory feeds](inventory-feeds-about.md)
>* [Edit data generated from feeds](propagated-data-edit.md)
>* [Post campaign data generated from feeds to ad networks](propagated-data-post.md)
>* [Stop a posting job for inventory feed data](stop-job.md)
>* [Statuses of data generated from feeds](propagated-data-status.md)
