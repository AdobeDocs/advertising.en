---
title: The AMO ID (s_kwcid) tracking parameter
description: Learn about the tracking parameter used to share Adobe Advertising data with Adobe Analytics.
exl-id: 3f739f1c-3cb7-40d0-86ab-cf66afe6a06f
feature: Search Tracking
---
# The AMO ID (s_kwcid) tracking parameter

*Advertisers with an Adobe Advertising-Adobe Analytics integration only*

<!-- This should go in the Analytics integration chapter > IDs page, under "AMO IDs" once I've finalized content for DSP clients.  -->

Adobe Advertising shares data about your campaigns with Adobe Analytics using the AMO ID append parameter, also called the `s_kwcid` parameter, which consists of ad channel and ad network-specific elements. 

The parameter is added to your tracking URLs in one of the following ways:

* (Recommended) The server-side insertion feature is implemented.

  * DSP customers: The pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user views a display ad with the Adobe Advertising pixel.

  * Search, Social, & Commerce customers:

    * For [!DNL Google Ads] and [!DNL Microsoft® Advertising] accounts with the [!UICONTROL Auto Upload] setting enabled for the account or campaign, the pixel server automatically appends the s_kwcid parameter to your landing page suffixes when an end user clicks an ad with the Adobe Advertising pixel.
    
    * For other ad networks, or [!DNL Google Ads] and [!DNL Microsoft® Advertising] accounts with the [!UICONTROL Auto Upload] setting disabled, manually add the parameter to your account-level append parameters, which append it to your base URLs.

* The server-side insertion feature isn't implemented:

  * DSP customers:

    * For [!DNL Flashtalking] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md)."

    * For [!DNL Google Campaign Manager 360] ad tags, manually insert additional macros per "[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)."

  <!--  * For all other ads, XXXX. -->

  * Search, Social, & Commerce customers:
  
    * For ([!DNL Google Ads] and [!DNL Microsoft® Advertising]) ads, manually add the AMO ID parameter to your landing page suffixes.

    * For ads on all other ad networks, manually add the AMO ID parameter to your account-level append parameters, which append it to your base URLs.

To implement the server-side insertion feature, or to determine the best option for your business, talk to your Adobe Account Team.

For the AMO ID formats for DSP and Search, Social, & Commerce, see "[Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id)."

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md){target="_blank"}
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id){target="_blank"}
>* (Search, Social, & Commerce) [Manage ad network accounts](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)
>* (Search, Social, & Commerce) [Baidu campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* (Search, Social, & Commerce) [Google Ads campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* (Search, Social, & Commerce) [Microsoft® Advertising campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* (Search, Social, & Commerce) [Yahoo! Japan Ads campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* (Search, Social, & Commerce) [Yandex campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
