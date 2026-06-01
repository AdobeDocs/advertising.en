---
title: (New UI) Enable uploading of objectives to ad networks
description: Learn how to upload objectives for your hybrid portfolios to Google Ads and Microsoft Advertising.
feature: Search Objectives, Search Optimization
hide: true
---
# (New UI) Enable uploading of objectives to ad networks

*Beta feature*

*Advertisers with [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts only*

*Advertisers enabled for hybrid optimization only*

Search, Social, & Commerce can upload the objectives for an advertiser account's portfolios to [!DNL Google Ads] and [!DNL Microsoft Advertising] so you can use them for hybrid optimization. Your uploaded objectives are available as conversion actions for account-level and campaign-level custom conversion goals.

Enabling this option automatically triggers an upload for objectives in portfolios that contain campaigns with smart bidding strategies. Search, Social, & Commerce creates a conversion on the ad network for each applicable objective. The conversion represents all weighted conversion metrics in the objective at the EF ID (click ID) level. For [!DNL Google Ads] clicks, the EF ID is the [!DNL Google Ads] `gclid`; for [!DNL Microsoft Advertising] clicks, the EF ID is the [!DNL Microsoft Advertising] `msclkid`. Because of this click ID, conversion data can be mapped to the specific keyword and click time.

Each uploaded conversion has the following name:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

where `<network_ID>` is the numeric ID that Search, Social, & Commerce uses for the ad network, `<objective_ID>` is the numeric objective ID, and `<network_account_ID>` is the numeric ID for the ad network account or manager account.

Uploads to [!DNL Google Ads] and [!DNL Microsoft Advertising] occur throughout the day, usually hourly. For advertisers with large accounts or custom configurations, uploads occur at least three times daily.

>[!IMPORTANT]
>
>Conversions tracked by [!DNL Google Ads] and by the [!DNL Microsoft Advertising] universal event tracking (UET) tag aren't re-uploaded to the ad networks. If you include them within an objective, you must add them to the campaign goals within the ad network's editor.

1. In the main menu, click **[!UICONTROL Goals]** > **[!UICONTROL Objectives]**.

1. In the toolbar, click **[!UICONTROL Upload Objective]**.

1. In the [!UICONTROL Objective Upload Setup] dialog, set the **[!UICONTROL Enable Objective Upload]** toggle to **[!UICONTROL On]**.

1. (Advertisers with [!DNL Google Ads] accounts who do business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you've collected consent from EEA and UK users to upload their data for advertising purposes, select the checkbox to confirm EEA/UK user consents have been collected. This sends consent status as **[!UICONTROL GRANTED]** to [!DNL Google Ads] and [!DNL Microsoft Advertising]. If left unchecked, consent status is sent as **[!UICONTROL UNSPECIFIED]**.

1. (If your conversions are tracked at a manager account level) [Add credentials for your manager account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md) before saving.

1. Click **[!UICONTROL Save]**.

1. Verify that each objective &mdash; named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` &mdash; appears within two days on the ad network.

   In the [!DNL Google Ads] editor, look up your [conversion actions](https://support.google.com/google-ads/answer/11461796){target="_blank"}. In the [!DNL Microsoft Advertising] editor, look up your [conversion goals](https://help.ads.microsoft.com/#apex/ads/en/56709){target="_blank"}.
   
   If necessary, update the date range to include the upload date.

## How the weighted objective is calculated

The weighted objective that's passed to the ad network is the sum of all metric values collected, with the exception of conversions tracked by [!DNL Google Ads] or by the [!DNL Microsoft Advertising] universal event tracking (UET) tag. The value is calculated using the attribution method set up for the advertiser's Search, Social, & Commerce account.

For example, say the objective's goal metric is Cart Additions with a weight of 25, and your assist metrics include GGL_Lead and Revenue with weights of 1 and Downloads with a weight of 0.5.

![Example of a weighted objective](/help/search-social-commerce/assets/objective-example.png "Example of a weighted objective")

Suppose a keyword resulted in the following actions for the portfolio:

* 10 Cart Additions
* $500 in Revenue
* 50 Downloads
* 5 GGL_Lead

GGL_Lead isn't included in the calculation/upload because it's a Google Ads-tracked metric. Therefore the weighted objective value is calculated as ((10 x 25) + (500 x 1) + (50 x 0.5)) = 775.

>[!TIP]
>
>You can view data for Adobe Advertising weighted revenue within the ad network's reports. As a best practice, compare the weighted revenue to the [!DNL Google Ads] "All conv. (by conv. time)" metric or the [!DNL Microsoft Advertising] metric "All conv. revenue," segmented to the O_ACS_OBJ* metric.

## Troubleshooting missing objectives

If the objective &mdash; named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` &mdash; for one of your portfolios doesn't appear on the ad network, then check the following:

* ([!DNL Google Ads]) Check if the conversions should be uploaded to the account or manager level. If they should be uploaded at the manager level:

  * Check if the credentials for the [!DNL Google Ads] manager account are provided. If necessary, [add the credentials for the manager account](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md).

  * Check if the ad network account already includes the same metric name. If it does, rename the metric so that the correct manager-level property can be created.

* Check that the portfolio's "hybrid" option is selected and that the objective has valid revenue.

>[!MORELIKETHIS]
>
>* [About objectives](objective-about.md)
>* [Manage and view performance data for an advertiser's conversion metrics](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)
>* [Manage credentials for [!DNL Google Ads] manager accounts](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
