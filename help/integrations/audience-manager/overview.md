---
title: Adobe Advertising Integrations with Adobe Audience Manager
description: Learn about the different ways in which Adobe Advertising can exchange data with Adobe Audience Manager.
feature: Integration with Adobe Audience Manager
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
---
# Adobe Advertising Integrations with Adobe Audience Manager

You can integrate Adobe Advertising with Audience Manager in the following ways.

## Synchronize Audience Manager and other [!DNL Adobe] Segments for Ad Targeting

[!DNL Search] and DSP can pull in metadata, hierarchy data, and unique audience data for all of an advertiser's or agency's Audience Manager and other [!DNL Adobe] audiences. This unique connection is available only to marketers using Adobe Advertising. See "[Import Adobe Audience Manager Segments for Ad Targeting](/help/integrations/audience-manager/import-audiences.md)."

### Use Audience Manager and Other [!DNL Adobe] Segments to Create [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opted-in advertisers with [!DNL Advertising Search] only*

Within [!DNL Search], you can create [!DNL Google Ads] Google customer match audiences from user IDs using your existing Audience Manager segments that have [!UICONTROL Adobe Media Optimizer (HTTP)] and [!UICONTROL Adobe Media Optimizer Batch Destination] as destinations. ([!DNL Media Optimizer] is a former name for [!DNL Search].) This includes Adobe Analytics segments that are published to Adobe Experience Cloud and segments that are created using the Adobe Experience Cloud [!DNL Audience Library]. For more information, see the in-product help within [!DNL Search].

[Customer match audiences from user IDs](https://support.google.com/google-ads/answer/9199250) work like website tag-based audiences, but a non-PII ID is assigned to unique audience members for distinct benefits over standard customer match and website tag-based audiences.

To create the necessary user IDs, you must use an Adobe Advertising JavaScript tag <!-- with a user ID parameter -->on your websites. Contact your Adobe Account Team for more information. 

![segment creation process](/help/integrations/assets/ad_search_user_id_pic.png)

Once you create the audiences, you can use them in [!DNL Google Ads] campaigns as [campaign-level or ad group-level targets or exclusions](#audience-manager-targets).

### Use Audience Manager and other [!DNL Adobe] Segments to Target or Exclude Ads {#audience-manager-targets}

* (Opted-in advertisers with [!DNL Search]) You can use any [!DNL Google Ads] audiences that were [created using [!DNL Adobe] segments](#audience-manager-google-audiences) as campaign-level or ad group-level targets or exclusions in your [!DNL Google Ads] campaigns.

* (Advertisers with DSP) You can use your existing [!DNL Adobe] segments as targets for your ad placements. You can optionally include the segments in reusable audiences, which you can use as targets or exclusions for multiple placements.

* (Advertisers with Advertising Creative) You can use your existing [!DNL Adobe] segments as targets for specific creatives in your ad experiences.

>[!NOTE]
>
>For more information about how to create audiences in the Audience Manager and Experience Cloud [!DNL Audience Library] interfaces, and common use cases for different audience types, see "[Audience creation options](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)."

## Send DSP Media Exposure Data to Audience Manager

*Advertisers with DSP only*

DSP customers with Adobe Audience Manager can capture data from ad campaigns using pixel calls to Audience Manager. You can then use the campaign data to build rule-based traits, which you can use to define new segments to enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

See "[Overview of Sending DSP Media Exposure Data to Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)" for more information.

## Get Richer Insights into Site Activity with Audience Analytics

Adobe Advertising customers with [[!DNL Adobe Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) can send both Adobe Advertising-tracked data and Audience Manager segments to [!DNL Analytics] for enriched insights about site activity.

For more information, see "[[!DNL Adobe Audience Analytics] for Adobe Advertising Customers](/help/integrations/audience-manager/audience-analytics.md)."
