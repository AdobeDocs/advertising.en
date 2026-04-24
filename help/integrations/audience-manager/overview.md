---
title: Adobe Advertising integrations with Adobe Audience Manager
description: Learn about the different ways in which Adobe Advertising can exchange data with Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
TQID: https://experienceleague.adobe.com/4O4O-DmHhClvSiOSxM9blAEvVslzYzRobEyU6RGeMEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
    internal-label: Audience Manager integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Adobe Advertising integrations with Adobe Audience Manager

You can integrate Adobe Advertising with Audience Manager in the following ways.

## Synchronize Audience Manager and other [!DNL Adobe] segments for ad targeting

[!DNL Search, Social, & Commerce] and DSP can pull in metadata, hierarchy data, and unique audience data for all of an advertiser's or agency's Audience Manager and other [!DNL Adobe] audiences. This unique connection is available only to marketers using Adobe Advertising. See "[Import Adobe Audience Manager segments for ad targeting](/help/integrations/audience-manager/import-audiences.md)."

### Use Audience Manager and other [!DNL Adobe] segments to create [!DNL Google Ads] audiences {#audience-manager-google-audiences}

*Opted-in advertisers with [!DNL Advertising Search, Social, & Commerce] only*

Within [!DNL Search, Social, & Commerce], you can create [!DNL Google Ads] customer match audiences from user IDs using your existing Audience Manager segments that have [!UICONTROL Adobe Media Optimizer (HTTP)] and [!UICONTROL Adobe Media Optimizer Batch Destination] as destinations. ([!DNL Media Optimizer] is a former name for [!DNL Search, Social, & Commerce].) This includes Adobe Analytics segments that are published to Adobe CX Enterprise and segments that are created using the Adobe CX Enterprise [!DNL Audience Library]. For more information, see "[Create [!DNL Google Ads] customer match audiences from [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)."

[Customer match audiences from user IDs](https://support.google.com/google-ads/answer/9199250) work like website tag-based audiences, but a non-PII ID is assigned to unique audience members for distinct benefits over standard customer match and website tag-based audiences.

To create the necessary user IDs, you must use an Adobe Advertising JavaScript tag <!-- with a user ID parameter -->on your websites. Contact your Adobe Account Team for more information. 

![segment creation process](/help/integrations/assets/ad_search_user_id_pic.png)

Once you create the audiences, you can use them in [!DNL Google Ads] campaigns as [campaign-level or ad group-level targets or exclusions](#audience-manager-targets).

### Use Audience Manager and other [!DNL Adobe] segments to target or exclude ads {#audience-manager-targets}

* (Opted-in advertisers with [!DNL Search, Social, & Commerce]) You can use any [!DNL Google Ads] audiences that were [created using [!DNL Adobe] segments](#audience-manager-google-audiences) as campaign-level or ad group-level targets or exclusions in your [!DNL Google Ads] campaigns.

* (Advertisers with DSP) You can use your existing [!DNL Adobe] segments as targets for your ad placements. You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Adobe] segments as targets for specific creatives in your ad experiences.

>[!NOTE]
>
>For more information about how to create audiences in the Audience Manager and Adobe CX Enterprise [!DNL Audience Library] interfaces, and common use cases for different audience types, see "[Audience creation options](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)."

## Send DSP media exposure data to Audience Manager

*Advertisers with DSP only*

DSP customers with Adobe Audience Manager can capture data from ad campaigns using pixel calls to Audience Manager. You can then use the campaign data to build rule-based traits, which you can use to define new segments to enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

See "[Overview of sending DSP media exposure data to Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)" for more information.

## Get richer insights into site activity with Audience Analytics

Adobe Advertising customers with [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) can send both Adobe Advertising-tracked data and Audience Manager segments to [!DNL Analytics] for enriched insights about site activity.

For more information, see "[[!DNL Adobe Audience Analytics] for Adobe Advertising customers](/help/integrations/audience-manager/audience-analytics.md)."
