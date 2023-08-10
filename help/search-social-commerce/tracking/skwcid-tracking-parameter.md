---
title: The s_kwcid tracking parameter
description: Learn about the tracking parameter used to share Adobe Advertising data with Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
---
# The s_kwcid tracking parameter

*Advertisers with an Adobe Advertising-Adobe Analytics integration only*

<!-- Where should this go? It probably belongs in the Analytics integration chapter, but I'll need to fit it in/create context around it/explain more about implementation and how this works.  SPECIFICALLY, I'll need to update the second section that explains when/where to add the code for DSP clients. -->

Adobe Advertising shares data about your campaigns with Adobe Analytics using the `s_kwcid` append parameter, which consists of ad channel and ad network-specific elements. The parameter is added to your tracking URLs in one of the following ways:

* (Recommended<!--; the only option for Advertising DSP-->) The server-side s_kwcid feature is implemented.

  * DSP customers: The pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user views a display ad with the Adobe Advertising pixel.

  * Search, Social, & Commerce customers:

    * For [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting enabled for the account or campaign, the pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user clicks an ad with the Adobe Advertising pixel.
    
    * For other ad networks, or [!DNL Google Ads] and [!DNL Microsoft Advertising] accounts with the [!UICONTROL Auto Upload] setting disabled, manually add the parameter to your account-level append parameters, which append it to your base URLs.

* <!-- (Search, Social, & Commerce only) -->The server-side s_kwcid feature isn't implemented, and you need to manually add the s_kwcid parameter to your ([!DNL Google Ads] and [!DNL Microsoft Advertising]) landing page suffixes or (other ad networks) account-level append parameters.

To implement the server-side s_kwcid feature, or to determine the best option for your business, talk to your Adobe Account Team.

## s_kwcid format for Advertising DSP ads

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

where:

* `AC` indicates the display channel.

* `{TM_AD_ID}` is the alphanumeric ad key.

* `{TM_PLACEMENT_ID}` is the alphanumeric placement key.

## s_kwcid formats for Search, Social, & Commerce ads

The parameters vary by ad network, but the following parameters are common to all:

* `AL` indicates the search channel. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is a unique user ID assigned to the advertiser.

* `{sid}` is replaced by the numeric ID for the advertiser's ad network account: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (deprecated), or *106* for [!DNL Pinterest] (deprecated).

### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

### [!DNL Google Ads]

These including shopping campaigns using [!DNL Google Merchant Center].

* Accounts that use the latest s_kwcid format, which supports campaign- and ad group-level reporting for performance max campaigns and drafts and experiments campaigns:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* All other accounts:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

>[!NOTE]
>
>* For dynamic search ads, {keyword} is populated with the auto target.
>* When you generate tracking for [!DNL Google] shopping ads, a product ID parameter, `{adwords_producttargetid}`, is inserted before the keyword parameter. The product ID parameter doesn't appear in the [!DNL Google Ads] account-level and campaign-level tracking parameters.
>* To use the latest s_kwcid tracking code, see "[Update the s_kwcid tracking code for a [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md)."

<!--

### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

### [!DNL Microsoft Advertising]

* Search campaigns:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Shopping campaigns (using [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Audience network campaigns:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Manage ad network accounts](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* [Baidu campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Japan Ads campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
