---
title: Enable uploading of objectives to ad networks
description: Learn how to upload objectives for your hybrid portfolios to [!DNL Google Ads] and [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
---
# Enable uploading of objectives to ad networks

*Advertisers with [!DNL Google Ads] and [!DNL Microsoft® Advertising] accounts only*

*Advertisers enabled for hybrid optimization only*

If your advertiser account is configured to use hybrid optimization, then Adobe Advertising can optionally upload the objectives for the account's portfolios to [!DNL Google Ads] and [!DNL Microsoft® Advertising] as conversions so you can use them for hybrid optimization.

Enabling this option automatically triggers an upload for portfolios that contain campaigns with smart bidding strategies. Search, Social, & Commerce creates a conversion on the ad network for each applicable portfolio-and-objective combination. Each conversion has the name `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, where `<portfolio_id>` is the numeric portfolio ID and `<se_acctid/conversion_manager_se_acctid>` is the numeric ID for the ad network account or manager account. The conversion represents all weighted conversion metrics in the objective.

Uploads to [!DNL Google Ads] occur daily at 06:00 in the advertiser's time zone. Uploads to [!DNL Microsoft® Advertising] occur daily at 09:00 in the advertiser's time zone.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Enable Objective Upload]**.
   
   This option is available only if your advertiser account is configured to use hybrid optimization. To enable hybrid optimization, contact your Adobe Account Team.

1. Click **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [About managing an advertiser's conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Upload conversion metrics to [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
