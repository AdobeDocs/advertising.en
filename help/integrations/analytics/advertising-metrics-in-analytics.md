---
title: Adobe Advertising Metrics in Analysis Workspace
description: Adobe Advertising Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
---
# Adobe Advertising Metrics in Analysis Workspace

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

>[!NOTE]
>
>* Adobe Advertising passes traffic metrics and dimensions to [!DNL Analytics] daily.
>* [!DNL Analytics] captures Adobe Advertising click-throughs and view-throughs in real time.
>* For [!DNL Search, Social, & Commerce], this feature is supported for most ad networks and campaign types. See "[Supported Inventory](/help/search-social-commerce/introduction/supported-inventory.md)" in the [!DNL Search, Social, & Commerce] Guide for more information.

## Traffic Metrics from Adobe Advertising

Adobe Advertising traffic metrics in [!DNL Analytics] usually start with "Adobe Advertising," except for "[!UICONTROL AMO ID Instances]." However, for long-term customers who used a custom event (rather than a reserved event) to originally create metrics for clicks, cost, and impressions, those metrics still begin with "AMO."

| Traffic Metric | Description |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] or (some legacy customers) [!UICONTROL AMO Clicks] | The number of total Adobe Advertising clicks. |
| [!UICONTROL Adobe Advertising Cost] or (some legacy customers) [!UICONTROL AMO Cost] | The Adobe Advertising spend in the currency of the report suite. |
| [!UICONTROL Adobe Advertising Impressions] or (some legacy customers) [!UICONTROL AMO Impressions] | The number of Adobe Advertising impressions. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | The number of impressions that were served for which viewability instrumentation successfully initialized. This value is calculated as (instrumented impressions - the number of unmeasurable impressions). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | The number of minutes an Adobe Advertising video was viewed. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | The number of impressions that were determined to be not viewable. This value is calculated as ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | The number of impressions that were measured to be viewable according to the placement configuration. |
| [!UICONTROL Adobe Advertising Views] | The number of views on an ad. A view is counted when the viewer initiates the Adobe Advertising video. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | The number of views for which at least 25% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | The number of views for which at least 50% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | The number of views for which at least 75% of an Adobe Advertising video was watched. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | The number of views for which 100% of an Adobe Advertising video was watched. |
| [!UICONTROL AMO ID Instances] | The number of times the [!UICONTROL AMO ID] is set. |

## Adobe Advertising Dimensions

>[!NOTE]
>
>All Adobe Advertising dimensions in [!DNL Analytics] are followed by "[!DNL (AMO ID)]."

| Dimension | Applicable Adobe Advertising Data  | Description |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Advertising DSP or the search engine name |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The account name. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) or the ad network name ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The campaign name. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The package ([!DNL DSP]) or portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | The placement name. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | The ad group name. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The search match type. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | The keyword and match type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad type, such as `text`, `video`, `display`, or `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data |The ad type ([!DNL DSP]) or ad title ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | The ad description ([!DNL DSP]) or ad body ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The URL displayed in the ad. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | The destination URL for the ad. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] and [!DNL Search, Social, & Commerce] data | Whether the landing page entry was a view-through or a click-through. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | The product target for a product listing ad. |

## Useful Custom Calculated Metrics for Adobe Advertising

Consider creating the following metrics for your Adobe Advertising data.

* Clicks to Landing Page Instance ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): This is the % of people who clicked the ad and made it to the landing page.
* Measurable Rate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Viewable Impression Rate ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Cost Per View ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Cost Per Click ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
