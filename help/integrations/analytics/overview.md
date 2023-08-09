---
title: Overview of [!DNL Analytics for Advertising]
description: Overview of [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
---
# Overview of [!DNL Analytics for Advertising]

*Advertisers with Advertising DSP and [!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integrates Adobe Analytics and Adobe Advertising to extend and enhance the capabilities of each product.

The integration allows advertisers to track click-through and view-through site interactions in their [!DNL Analytics] instances, allowing brands to see how their advertising spend leads to site engagement and critical business objectives.

In addition, Adobe Advertising can access the vast first-party data that [!DNL Analytics] collects using [!DNL Analytics] tags already on the site. This allows more robust journey management, first-party remarketing, and paid media site reporting. Adobe Advertising can further use the [!DNL Analytics] data for spend and bid optimization.

When properly employed, [!DNL Analytics for Advertising] blurs the lines between two traditional roles: advertising journey management (the act of sending users to the site through advertisements) and understanding that site engagement through web analytics.

Primary benefits:

* Send [!DNL Analytics] segments directly to Adobe Advertising for first-party site remarketing.
* Use [!DNL Analytics] custom and standard events as conversion signals for optimizing paid media advertising.
* Take advantage of [!DNL Analytics] Analysis Workspace to better understand site entry points and visit behavior.
* Enable closer collaboration between web analysts and paid media teams.
* Use persistent Adobe Advertising view-through and click-through IDs within [!DNL Analytics] to understand site engagement.
* Enhance traditional paid media reports in Analysis Workspace with custom metrics, custom dimensions, and site activity not achievable when exporting data or pixels to ad servers or other DSPs.
* Take advantage of [!DNL Analytics] code already on your website for tracking and optimization within Adobe Advertising.

>[!TIP]
>
> Watch a [video introduction to [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Using Analytics for Paid Media Reporting

[!DNL Analytics for Advertising] improves reporting and insight on how your advertising drives site behavior by allowing you to:

* Use persistent Adobe Advertising view-through and click-through IDs within [!DNL Analytics] to understand site engagement.
* Take advantage of Analysis Workspace to better understand site entry points and visit behavior. You can access paid media dimensional and event data, which include Adobe Advertising campaign entity names (down to placements and ads) and their associated metrics, such as clicks, impressions, and cost.

To use [!DNL Analytics] as your paid media reporting tool, your organization needs an Experience Cloud login with access to Analysis Workspace. Your Adobe Advertising team will help you to map your Adobe Advertising data to individual report suites in Analysis Workspace. You can send Adobe Advertising data to any report suite, but you should be aware of the report suites that have been mapped to Adobe Advertising and those that haven't. Depending on the report suite, this may change the data reported.

[Adobe Advertising IDs within [!DNL Analytics]](ids.md) works like other [!DNL eVars], with a custom, persistent expiration. By default, the attribution lookback window is set to 60 days during the Adobe Advertising implementation. To change this setting, work with your Adobe Account Team.

Adobe Advertising dimensions are appended with the suffix "(AMO ID)" (such as "Ad Type (AMO ID)"). See "[Adobe Advertising Metrics in Analysis Workspace](advertising-metrics-in-analytics.md)" for a list of the available dimensions.

>[!NOTE]
>
> When you view Adobe Advertising data (or any data set) within [!DNL Analytics], be aware that metrics and reports are based on the rules that are set within [!DNL Analytics]. The data could be different than what you see within other reporting systems, such as ad server reports, [!DNL DSP] reports, or search engine reports. To understand the data differences in [!DNL Analytics], you need to know when [!DNL eVar] data expires, what defines a visit, what is considered last touch attribution versus total persisting attribution, and other factors. For more information, see [Expected Data Variances Between [!DNL Analytics] and Adobe Advertising](data-variances.md).

## Using Analytics to Power Adobe Advertising Campaigns and Portfolios

Without requiring any additional pixels, [!DNL Analytics for Advertising] enables better optimization and easier audience segmentation by sending two main signals to Adobe Advertising:

* Conversion metrics to be used as bid signals:
  * standard metrics, such as [!UICONTROL Revenue] and [!UICONTROL Cart Views].
  * site engagement metrics, such as page view and visit metrics.
  * custom revenue metrics.
  * reserved revenue metrics.
* Segments created in [!DNL Analytics] and published to Experience Cloud.

  You can use [!DNL Analytics] segments for first-party site retargeting in [!DNL DSP] and paid search advertisements.

  ([!DNL Search, Social, & Commerce] only) Advertisers with [!DNL Analytics] but not Audience Manager can also create Google website tag-based audiences (remarketing lists) and customer match audiences (customer lists) from [!DNL Analytics] segments that are shared with Experience Cloud.

### Site Conversion Metrics as Bid Signals

You can use your standard events and custom events from [!DNL Analytics] to build weighted objectives in Adobe Advertising. Objectives inform bidding decisions for your [!DNL DSP] packages and Search portfolios.

>[!NOTE]
>
> You can't map calculated metrics from [!DNL Analytics] into Adobe Advertising.

Your Adobe Advertising team will help you to identify and map the events that are applicable to paid media performance into Adobe Advertising, where they will appear in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

See "[Analytics Metrics in Adobe Advertising](analytics-data-in-advertising.md)" for a list of available metrics.

### Analytics Segments for Site Retargeting

Adobe Advertising can ingest [!DNL Analytics] segments for remarketing purposes for Advertising DSP and [!DNL Search, Social, & Commerce] ads using the native Experience Cloud Audiences integration between [!DNL Analytics] and Experience Cloud.

To access the [!DNL Analytics] segments, an advertiser account needs to have the [Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) enabled. When the ID Service is enabled, all Experience Cloud segments (including segments created in [!DNL Analytics] and published to Experience Cloud, segments created in Adobe Audience Manager, segments created in Experience Cloud using the [!DNL People core service], and segments created in Adobe Experience Platform and sent to Adobe Advertising via Audience Manager) become available within Adobe Advertising as soon as they are processed.

[!DNL Analytics] segments are available within 24 hours and are updated daily.

For more information about the Experience Cloud Audiences service, see [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Examples of How to Use the Integration {#integration-examples}

### Using Adobe Advertising Data in Analysis Workspace

To learn how you can use your Adobe Advertising data to create visual reports in Analysis Workspace, see the video "[Introduction to Workspace and Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)."

#### Using Connected TV View-Through Conversions in Reports

*Advertising DSP users only*

You can measure the full-funnel effectiveness of your connected TV (CTV) campaigns by linking ad exposure on CTV devices to on-site conversions. The new [!UICONTROL Landing Type] filter "[!UICONTROL View-through (CTV)]" splits conversions into separate rows for [!UICONTROL Click Through], [!UICONTROL View Through], and [!UICONTROL View Through (CTV)] values.

To view your CTV view-through conversion metrics, use either the Placement view or the Marketing Channel view in Analysis Workspace.

Using the Placement view:

1. Include CTV-spending placements in the reporting view.

1. Include the desired metrics, such as “Impressions”, “Clicks”, and so on.

1. Apply the following filters:

   Ad Platform: `Advertising Cloud DSP`
   
   Landing Page: `View-Through (CTV)`

Using the Marketing Channel view:

1. Include the dimension `Marketing Channel`.

1. Include the desired metrics, such as “Impressions”, “Clicks”, and so on.

1. Apply the following filters:

   Ad Platform: `Advertising Cloud DSP`
   
   Landing Page: `View-Through (CTV)`

### Creating Adobe Advertising Dashboards

To learn how you can track your Adobe Advertising data against your goals in Analysis Workspace, see the video "[Create Adobe Advertising Dashboards with Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)."

### Using the Adobe Advertising ID for Site Entry Analysis

To see how you can create an Adobe Advertising site entry report to monitor day-of-week, time-of-day, browser, and geographical influences, see the video "[Create Adobe Advertising Site Entry Reports](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)."

>[!MORELIKETHIS]
>
>* [Video: Introduction to [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Prerequisites and Key Information for Implementing [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising IDs Used by Analytics](ids.md)
>* [JavaScript Code for Analytics for Advertising](/help/integrations/analytics/javascript.md)
>* [Expected Data Variances Between [!DNL Analytics] and Adobe Advertising](data-variances.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
