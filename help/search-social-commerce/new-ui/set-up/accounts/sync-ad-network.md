---
title: (New UI) Manually synchronize ad network data
description: Learn how to manually trigger synchronization of your campaign structure and campaign entities for supported ad networks from the new UI.
feature: Search Campaign Management
---
# (New UI) Manually synchronize ad network data via API connection 

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL Microsoft Advertising] (formerly [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex], and existing [!DNL Baidu] accounts only*

Synchronization is the process by which Search, Social, & Commerce gathers updated information for each advertiser's connected ad network accounts on [supported ad networks](/help/search-social-commerce/introduction/supported-inventory.md). This data includes the advertiser's campaign structure and campaign entities, including most of their attributes that are managed or reported in Search, Social, & Commerce. It doesn't include click data, nor bids and bid modifiers entered outside Search, Social, & Commerce, which are gathered separately.

Search, Social, & Commerce automatically synchronizes (syncs) with your ad network accounts once a day, and also whenever it detects a new campaign on one of your ad networks. In addition, it immediately sends all changes to campaign data made from within Search, Social, & Commerce to the ad network.

You can manually request synchronization of all active and paused campaigns in specified accounts<!--Not available as of 2/23:  or in specific active and paused campaigns -->. This task gathers entities on the ad network that are new or changed.

For campaigns with the "[!UICONTROL Auto Update]" option, the sync operation also generates and posts tracking codes that are missing or need to be changed in the tracking templates or destination URLs. The URLs are generated according to the parameters in the tracking settings for the account settings or campaign. If tracking URLs exist for the relevant items, they aren't regenerated unless new ones are needed (such as if the keyword match type, the creative text, or the account's tracking parameters have changed).

>[!NOTE]
>
>Anytime you [create a bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), you can optionally sync with the ad network before the bulksheet is created.

## Sync campaigns in an ad network account

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Select the check box next to the account name.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. In the floating toolbar, click **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.

You can follow the status of the sync job in the [!UICONTROL Workspace] view. The job may take
an hour or more to appear.

>[!MORELIKETHIS]
>
>* [Download/Create a bulksheet file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
