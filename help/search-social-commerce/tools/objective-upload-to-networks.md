---
title: Enable uploading of objectives to ad networks
description: Learn how to upload objectives for your hybrid portfolios to [!DNL Google Ads] and [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
---
# Enable uploading of objectives to ad networks

*Advertisers with [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

*Advertisers enabled for hybrid optimization only*

Search, Social, & Commerce can upload the objectives for an advertiser account's portfolios to [!DNL Google Ads] and [!DNL Microsoft Advertising] so you can use them for hybrid optimization. Your uploaded objectives are available as conversion actions for account-level and campaign-level custom conversion goals.

Enabling this option automatically triggers an upload for objectives in portfolios that contain campaigns with smart bidding strategies. Search, Social, & Commerce creates a conversion on the ad network for each applicable objective. The conversion represents all weighted conversion metrics in the objective at the EF ID (click ID) level. Each conversion has one of the following names:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` is the numeric ID that Search, Social, & Commerce uses for the ad network, `<objective_id>` is the numeric objective ID, and `<network_account_ID>` is the numeric ID for the ad network account or manager account.

* (Old format that will be deprecated in the future) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  where `<portfolio_id>` is the numeric portfolio ID and `<se_acctid/conversion_manager_se_acctid>` is the numeric ID for the ad network account or manager account.

  Your Adobe Account Team will work with you to migrate your existing conversion action names within the ad network before the old format is deprecated. During the migration period, both the old and new format uploads will run in parallel. Modelling and optimization aren't affected because the new conversion actions initially appear with "secondary" (not optimized) status and with 90 days of backfill data.

Uploads to [!DNL Google Ads] occur daily at 06:00 in the advertiser's time zone. Uploads to [!DNL Microsoft Advertising] occur daily at 09:00 in the advertiser's time zone.

>[!IMPORTANT]
>
>Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. If you include them within an objective, add them to the campaign goals within the ad network's editor.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Tools] > [!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Enable Objective Upload]**.

1. (Advertisers with [!DNL Google Ads] accounts who do business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you've collected consent from EEA and UK users to upload their data for advertising purposes, then select the check box next to **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Click **[!UICONTROL Save]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**.

1. Verify that each objective &mdash; named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` &mdash; appears within two days on the ad network.

   In the [!DNL Google Ads] editor, look up your [conversion actions](https://support.google.com/google-ads/answer/11461796). In the [!DNL Microsoft Advertising] editor, look up your [conversion goals](https://help.ads.microsoft.com/#apex/ads/en/56709).
   
   If necessary, update the date range to include the upload date.

## How the weighted objective is calculated

The weighted objective that's passed to the ad network is the sum of all metric values collected, with the exception of conversions tracked by [!DNL Google Ads] or by the [!DNL Microsoft Advertising] universal event tracking (UET) tag.

For example, say the objective's goal metric is Cart Additions with a weight of 25, and your assist metrics include GGL_Lead and Revenue with weights of 1 and Downloads with a weight of 0.5.

![Example of a weighted objective](/help/search-social-commerce/assets/objective-example.png "Example of a weighted objective")
 
Suppose a keyword resulted in the following actions for the portfolio:

* 10 Cart Additions
* $500 in Revenue
* 50 Downloads
* 5 GGL_Lead

GGL_Lead isn't included in the calculation/upload because it's a Google Ads-tracked metric. Therefore the weighted objective value is calculated as ((10 x 25) + (500 x 1) + (50 x 0.5)) = 775.

## Troubleshooting missing objectives

If the objective &mdash; named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` &mdash; for one of your portfolios doesn't appear on the ad network, then check the following:

* ([!DNL Google Ads]) Check if the conversions should be uploaded to the account or manager level. If they should be uploaded at the manager level:

  * Check if the credentials for the [!DNL Google Ads] manager account is provided at **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**. If necessary, [add the credentials for the manager account](/help/search-social-commerce/admin/manager-accounts.md).
  
  * Check if the ad network account already includes the same metric name. If it does, then rename the metric so that the correct manager-level property can be created.

* Check that the portfolio's "hybrid" option is selected and that the objective has valid revenue.

>[!MORELIKETHIS]
>
>* [About managing an advertiser's conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Upload conversion metrics to [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
