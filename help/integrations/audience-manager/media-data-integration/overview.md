---
title: Overview of Sending DSP Media Exposure Data to Adobe Audience Manager
description: Learn how to use Audience Manager event pixels to capture impression-level and click-level data from Advertising DSP campaigns
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
---
# Overview of Sending DSP Media Exposure Data to Adobe Audience Manager

*Advertisers with Advertising DSP only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager Integration Only*

Advertising DSP customers with Adobe Audience Manager can use Audience Manager event pixels to capture impression-level data and click-level data from DSP campaigns. The event pixels send the data as actionable signals to Audience Manager. These signals enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

DSP doesn't charge you to send these signals to Audience Manager. However, you pay standard Audience Manager ingestion costs based on server calls, per your Audience Manager contract. Audience Manager removes duplicate events that are tracked in two different ways, so that each event is charged only once.

>[!NOTE]
>
> Audience Manager also supports capturing data from ad server log files, which provides less flexibility. That process isn't covered in this documentation.

## Primary Benefits

* DSP campaign data flows into Audience Manager in real time, and you can use it to build rule-based traits that you use to define segments.

* Segments are available for targeting immediately after user trait and segment qualification, bolstering real-time targeting efforts.

* You can leverage the campaign data for such use cases as frequency capping across creatives, retargeting users who were exposed to previous campaigns, and analyzing downstream site behavior and entry points.

* The aggregated data provides a unified view of campaign performance, helps identify custom conversion paths, and can be used to improve the sequence of events that lead to conversions through Audience Manager [!DNL Audience Optimization Reports] or through an [[!DNL Audience Analytics] integration with Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## How the Data is Tracked

The Audience Manager impression and click event pixels are cookie-based. The pixels don't capture events that occur in cookie-less environments, such as mobile apps.<!-- Verify if this is still correct. -->

### Impression-Tracking Pixels

Audience Manager tracks impression data for an ad when you attach a 1xl-pixel transparent event tracking pixel to the ad. The event pixel is loaded each time the ad is served to a user and loaded by the web browser. The pixel is loaded from a client-specific subdomain of [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), which is a legacy domain for Audience Manager, and contains parameters as key-value pairs. The event call collects impression and conversion data and sends it to the Audience Manager data collection servers.

### Click-Tracking Pixels

Audience Manager tracks clicks similarly to impressions, except that it doesn't load the transparent event pixel each time the ad is served. Instead, the click data is tracked in the ad's click-through URL. The ad points to a client-specific subdomain of [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), which is a legacy domain for Audience Manager, for processing by the Audience Manager data collection servers. The server then redirects the user to the intended landing page. The URL contains parameters as key-value pairs.

>[!NOTE]
>
>If your organization uses [!DNL Analytics] tracking, then you may not need Audience Manager click tracking. Adobe Analytics captures click signals and can send them to Audience Manager through [server-side forwarding](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Collect Click and Impression Data from Advertising DSP Campaigns](collect.md)
>* [Use Cases](use-cases.md)
