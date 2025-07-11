---
title: Update the AMO ID (s_kwcid) tracking code for a [!DNL Google Ads] account
description: Learn how to switch to the latest AMO ID tracking code for a [!DNL Google Ads] account.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
---
# Update the AMO ID (s_kwcid) tracking code for a [!DNL Google Ads] account

*Advertisers with an Adobe Advertising-Adobe Analytics integration only*

*[!DNL Google Ads] accounts only*

The legacy (prior to October 2019) format for the [AMO ID tracking code](/help/integrations/analytics/ids.md#amo-id-formats) for existing [!DNL Google Ads] accounts doesn't support some features in Analytics, such as reporting at the campaign and ad group levels for [!DNL Google Ads] performance max campaigns, drafts and experiments campaigns, and other use cases in which the same ad+keyword+match type combination exists in multiple campaigns.

The current format includes parameters for campaign ID and ad group ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

For an existing account that uses the legacy format, you can change to the current format. If you don't have performance max campaigns or drafts and experiments campaigns, migrating then to the new format is optional.

All new [!DNL Google Ads] accounts automatically use the current AMO ID format.

>[!NOTE]
>
>This option is available only for accounts that don't use the current format.
>
>After you migrate an account, all click, cost, and impression data are reported correctly after the change, but any click-throughs that occurred before the migration are still attributed to conversion data based on the old AMO ID format.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Hold the cursor over the account name, click ![arrow dropdown icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png), and then select **[!UICONTROL Edit]**.

1. Click **[!UICONTROL Set Account Tracking]**.

1. Begin the migration:

   1. Next to **[!UICONTROL S_KWCID FORMAT]** in the  [!UICONTROL Account Tracking] settings, click **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Click **[!UICONTROL Migrate to new s_kwcid format]**.

   1. In the confirmation message, select the check box, and then click **[!UICONTROL Continue]**.

   1. In the account settings, click **[!UICONTROL Post]**.

   Metadata for the campaigns is updated in [!DNL Analytics] within a few days. Tracking continues uninterrupted, so no data is lost, but reporting may not reflect the new tracking codes until [!DNL Analytics] receives all metadata.

   >[!NOTE]
   >
   >All click-throughs that occurred before the migration still report conversion data based on the old format.

1. After you begin the migration, update the Landing Page Suffix settings (called "final URL suffix" in some ad networks) as necessary:

   * When the [!UICONTROL Auto Upload]" feature is enabled in the tracking settings, Search, Social, & Commerce automatically updates the tracking code in the Landing Page Suffix for this account and its campaigns. You don't have to do anything.

   * When the [!UICONTROL Auto Upload]" feature isn't enabled, and you don't use the [server-side AMO ID feature](/help/integrations/analytics/ids.md#amo-id-formats), then you must manually update the AMO ID parameter in the Landing Page Suffix settings. You can change account- and campaign-level suffixes manually in the [account settings](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) and [campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) or by [uploading changes in a bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). To configure a suffix at the ad group level or lower, use the [!DNL Google Ads] editor.
   
   * If you include the AMO ID in the Base URL setting for any campaign component, then move it to the relevant Landing Page Suffix setting.

1. (Recommended) Verify the data for this account in [!DNL Analytics] before you migrate additional accounts.

>[!MORELIKETHIS]
>
>* [Manage ad network accounts](ad-network-account-manage.md)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Overview of [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
