---
title: Adobe Advertising Metrics in Analysis Workspace
description: Adobe Advertising Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
---
# Adobe Advertising Metrics in Analysis Workspace

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

>[!NOTE]
>
>* Adobe Advertising passes traffic metrics and dimensions to [!DNL Analytics] daily.
>* [!DNL Analytics] captures Adobe Advertising click-throughs and view-throughs in real time.

## Traffic Metrics from Adobe Advertising

>[!NOTE]
>
>All Adobe Advertising traffic metrics in [!DNL Analytics] start with "AMO."

| Traffic Metric | Description |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | The number of Adobe Advertising impressions. |
| [!UICONTROL AMO Clicks] | The number of total Adobe Advertising clicks. |
| [!UICONTROL AMO Cost] | The Adobe Advertising spend in the currency of the report suite. |
| [!UICONTROL AMO ID Instance] | The number of times the Adobe Advertising ID is set. |
| [!UICONTROL AMO Minutes Viewed] | The number of minutes an Adobe Advertising video was viewed. |
| [!UICONTROL AMO Views] | The number of views on an ad. A view is counted when the viewer initiates the Adobe Advertising video. |
| [!UICONTROL AMO Views 25% Complete] | The number of views for which at least 25% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO Views 50% Complete] | The number of views for which at least 50% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO Views 75% Complete] | The number of views for which at least 75% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO Views 100% Complete] | The number of views for which 100% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO Viewable Impressions] | The number of impressions that were measured to be viewable according to the placement configuration. |
| [!UICONTROL AMO Not Viewable Impressions] | The number of impressions that were determined to be not viewable. This value is calculated as ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | The number of impressions that were served for which viewability instrumentation successfully initialized. This value is calculated as (instrumented impressions - the number of unmeasurable impressions). |

## Useful Custom Calculated Metrics for Adobe Advertising

Consider creating the following metrics for your Adobe Advertising data.

* Clicks to Landing Page Instance ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): This is the % of people who clicked the ad and made it to the landing page.
* Measurable Rate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Viewable Impression Rate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Cost Per View ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Cost Per Click ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe Advertising Dimensions

>[!NOTE]
>
>All Adobe Advertising dimensions in [!DNL Analytics] are followed by "(AMO ID)."

| Dimension | Applicable Adobe Advertising Data  | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] and [!DNL Search] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] and [!DNL Search] data | The account name. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] and [!DNL Search] data | RTB ([!DNL DSP]) or the ad network name ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] and [!DNL Search] data | The campaign name. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] and [!DNL Search] data | The package ([!DNL DSP]) or portfolio ([!DNL Search]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | The placement name. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | The ad group name. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | The keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | The search match type. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | The keyword and match type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] and [!DNL Search] data | The ad type, such as `text`, `video`, `display`, or `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] and [!DNL Search] data |The ad type ([!DNL DSP]) or ad title ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] and [!DNL Search] data | The ad description ([!DNL DSP]) or ad body ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | The URL displayed in the ad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | The destination URL for the ad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] and [!DNL Search] data | Whether the landing page entry was a view-through or a click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | The product target for a product listing ad. |

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
