---
title: Enable uploading of objectives to ad networks
description: Learn how to upload objectives for your hybrid portfolios to [!DNL Google Ads] and [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
---
# Enable uploading of objectives to ad networks

*Advertisers with [!DNL Google Ads] and [!DNL Microsoft® Advertising] accounts only*

*Advertisers enabled for hybrid optimization only*

Search, Social, & Commerce can upload the objectives for an advertiser account's portfolios to [!DNL Google Ads] and [!DNL Microsoft® Advertising] so you can use them for hybrid optimization. Your uploaded objectives are available as conversion actions for account-level and campaign-level custom conversion goals.

Enabling this option automatically triggers an upload for objectives in portfolios that contain campaigns with smart bidding strategies. Search, Social, & Commerce creates a conversion on the ad network for each applicable objective. The conversion represents all weighted conversion metrics in the objective. Each conversion has one of the following names:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` is the numeric ID that Search, Social, & Commerce uses for the ad network, `<objective_id>` is the numeric objective ID, and `<network_account_ID>` is the numeric ID for the ad network account or manager account.

* (Old format that will be deprecated in the future) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` is the numeric portfolio ID and `<se_acctid/conversion_manager_se_acctid>` is the numeric ID for the ad network account or manager account.

  Your Adobe Account Team will work with you to migrate your existing conversion action names within the ad network before the old format is deprecated. During the migration period, both the old and new format uploads will run in parallel. Modelling and optimization aren't affected because the new conversion actions will appear initially with "secondary" (not optimized) status and with 90 days of backfill data.

Uploads to [!DNL Google Ads] occur daily at 06:00 in the advertiser's time zone. Uploads to [!DNL Microsoft® Advertising] occur daily at 09:00 in the advertiser's time zone.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

[!IMPORTANT] Each campaign in a hybrid portfolio must use the same conversion goals as the portfolio's objective. Using different conversion goals may impact portfolio performance.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Enable Objective Upload]**.

1. (Advertisers with [!DNL Google Ads] accounts who do business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you've collected consent from EEA and UK users to upload their data for advertising purposes, then select the check box next to **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Click **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [About managing an advertiser's conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Upload conversion metrics to [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
