---
title: Adobe Advertising Integrations with Adobe Analytics
description: Learn about how Adobe Advertising can exchange data with Adobe Analytics and how you can use the data within Search, Social, & Commerce.
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
---
# Adobe Advertising Integrations with Adobe Analytics

You can integrate Adobe Advertising with Analytics in the following ways.

## Exchange Data Between [!Analytics] and Adobe Advertising

### Pull [!Analytics] Data into Adobe Advertising

With [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] and DSP pull in:

* **[!DNL Analytics] segments:**  Metadata, hierarchy data, and unique audience data for all of an advertiser's or agency's segments created in [!DNL Analytics] and published to Experience Cloud.

* **[!DNL Analytics] site engagement metrics** 

* **[!DNL Analytics] Standard, custom, and reserved metrics**

### Send Adobe Advertising Data to [!Analytics]

* **Traffic metrics from Adobe Advertising**

* **Dimensions from Adobe Advertising**

>[!NOTE]
>
>For [!DNL Search, Social, & Commerce], this feature is supported for most ad networks and campaign types. See "Supported Inventory" in the [!DNL Search, Social, & Commerce] Guide for more information.<!-- add link when that's published in ExL -->

### Use [!DNL Analytics] Segments to Create [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opted-in advertisers with [!DNL Advertising Search, Social, & Commerce] only*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce], you can create [!DNL Google Ads] Google customer match audiences from user IDs using your existing [!DNL Analytics] segments. This includes Adobe Analytics segments that are published to Adobe Experience Cloud and segments that are created using the Adobe Experience Cloud [!DNL Audience Library]. For more information, see the in-product help within [!DNL Search, Social, & Commerce].

[Customer match audiences from user IDs](https://support.google.com/google-ads/answer/9199250) work like website tag-based audiences, but a non-PII ID is assigned to unique audience members for distinct benefits over standard customer match and website tag-based audiences.

To create the necessary user IDs, you must use an Adobe Advertising JavaScript tag <!-- with a user ID parameter -->on your websites. Contact your Adobe Account Team for more information. 

![segment creation process](/help/integrations/assets/ad_search_user_id_pic.png)

Once you create the audiences, you can use them in [!DNL Google Ads] campaigns as [campaign-level or ad group-level targets or exclusions](#audience-manager-targets).

### Use [!DNL Analytics] Segments to Target or Exclude Ads {#analytics-targets}

* (Opted-in advertisers with [!DNL Search, Social, & Commerce]) You can use any [!DNL Google Ads] audiences that were [created using [!DNL Analytics] segments](#audience-manager-google-audiences) as campaign-level or ad group-level targets or exclusions in your [!DNL Google Ads] campaigns.

* (Advertisers with DSP) You can use your existing [!DNL Analytics] segments as targets for your ad placements. You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Analytics] segments as targets for specific creatives in your ad experiences.
