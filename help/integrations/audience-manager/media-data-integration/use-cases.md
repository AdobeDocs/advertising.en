---
title: Use Cases
description: Learn about use cases for sharing your Advertising DSP media data with Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 21d80cf6-f817-495a-bae4-fc9e44f1eda4
---
# Use Cases for Capturing Media Exposure Data in Adobe Audience Manager

*Advertisers with Advertising DSP only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager Integration Only*

Following are some ways in which you can benefit from capturing your Advertising DSP media exposure data <!-- ad impression data? --> in Audience Manager.

## Recency and Frequency Management

Capturing impression data in Audience Manager allows you to enhance your frequency management by creating segments of users who have been exposed to a particular ad or campaign. You can use these segments for ad targeting if you want to increase frequency, or for ad suppression if you want to limit frequency.

Also, with Audience Manager [!DNL Segment Builder], you can apply [recency and frequency controls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) to any [rule-based traits](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) that contain actionable signals. This allows you, for example, to limit the number of times a user is shown a particular creative within a media campaign. Read "[Instant Cross-Device Suppression](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)" to learn how to do this.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sequential Messaging

By capturing impression data, you can create a segment of users who have been exposed to a campaign or ad and use this segment for sequential messaging or suppression. For example, you can retarget users who saw creative `123` but didn’t click or convert by showing them creative `456`.

To execute this example in Audience Manager, you would follow these steps:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Create a trait to capture users who saw the creative.

     For example, to name the trait `Creative Trait 123`, use the following trait rule:

     `d_creative == 123 AND d_event == imp`

1. Create a trait to capture users who click or convert.

     For example, to name this trait `Click and Converter`, use the following trait rule:

     `d_event == click OR d_event=conv`

1. Create a segment called `Retarget Users` to populate with users who saw creative `123` but didn’t click or convert. Use the following trait rule:

     `Creative Trait 123 AND NOT Click and Converter`

1. Map the segment `Retarget Users` to a destination, and target users in the destination with creative `456`.

## [!DNL Adobe Audience Analytics] and Campaign Exposure Data

Once campaign impression and click data is available within Audience Manager, you can create traits and segments of users who were exposed to, or interacted with, a particular campaign or tactic. With an [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), your Audience Manager segments can be synced with [!DNL Analytics] for further analysis. Potential use cases include the following:

* **Interaction analysis between DSP and [!DNL Adobe Advertising Search] ads:** The standard [[!DNL Analytics for Advertising] integration](/help/integrations/analytics/overview.md) doesn't provide insights into the interaction between DSP and [!DNL [!DNL Search]] because both channels use AMO IDs that follow AMO ID attribution rules, for which a search click overrides a display view-through. By creating a DSP exposure segment in Audience Manager, you can use [!DNL Audience Analytics] to analyze the interaction between DSP and [!DNL [!DNL Search]] ads in [!DNL Analytics].

* **Frequency analysis:** You can create segments in Audience Manager based on how many times a user was exposed to a particular ad or campaign. You can then analyze the different exposure segments in Analytics to see how user behavior changes depending on the number of DSP exposures.

## [!DNL Audience Optimization Reports]

You can leverage [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) to identify potential performance opportunities for segments across your campaigns. These reports combine campaign impression, click, and conversion data with segment metrics to inform segment-centric optimizations and an effective channel mix.

### Types of Relevant Audience Optimization Reports

| Report | Description |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html)| Compares mapped and unmapped segments by impressions and conversion rates. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Return data on impressions, click-through rates, and conversions for a broad range of advertising dimensions. |
| [[!UICONTROL Optimal Frequency] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Helps you discover the optimal balance between the number of served impressions and conversions. It allows you to adjust the number of impressions to display before starting to see diminishing returns. |
| [[!UICONTROL Unique User Reach] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | A bubble chart, in which each bubble is sized in direct proportion to the number of unique users for your selected dimension. |

### Considerations

* If [!DNL Audience Optimization Reports] users have role-based access controls (RBAC), then [!DNL Adobe Customer Care] must configure a mapping between the Advertiser ID and the organization's Audience Manager data source integration code. Administrator users can then provide RBAC rights to different users.

* Conversion reporting in [!DNL Audience Optimization Reports] requires some setup by the end user. Users must populate metadata files.

* [!DNL Audience Optimization Reports] doesn't support changes to campaign metadata (such as campaign name or placement name).

* Clicks on search ads are included in [!DNL Audience Optimization Reports] only when they're correlated with impressions. In other words, search clicks are treated as conversions following impressions. As a result, many search clicks may not be included in [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Overview of Sending DSP Media Exposure Data to Adobe Audience Manager](overview.md)
>* [Collect Click and Impression Data from Advertising DSP Campaigns](collect.md)
