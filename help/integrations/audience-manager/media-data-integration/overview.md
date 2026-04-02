---
title: Overview of sending DSP media exposure data to Adobe Audience Manager
description: Learn how to use Audience Manager event pixels to capture impression-level and click-level data from Advertising DSP campaigns
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
TQID: https://experienceleague.adobe.com/MqAVZH8WKVulxVDOD3SDbROYnkRG0tlm028WGBL9wOM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
    internal-label: DSP Campaigns
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Overview of sending DSP media exposure data to Adobe Audience Manager

*Advertisers with Advertising DSP only*

*Advertisers with an Adobe Advertising-Adobe Audience Manager Integration Only*

Advertising DSP customers with Adobe Audience Manager can use Audience Manager event pixels to capture impression-level data and click-level data from DSP campaigns. The event pixels send the data as actionable signals to Audience Manager. These signals enable various DSP use cases, such as more advanced segmentation, frequency management, marketing analytics, and reporting insights.

DSP doesn't charge you to send these signals to Audience Manager. However, you pay standard Audience Manager ingestion costs based on server calls, per your Audience Manager contract. Audience Manager removes duplicate events that are tracked in two different ways, so that each event is charged only once.

>[!NOTE]
>
> Audience Manager also supports capturing data from ad server log files, which provides less flexibility. That process isn't covered in this documentation.

## Primary benefits

* DSP campaign data flows into Audience Manager in real time, and you can use it to build rule-based traits that you use to define segments.

* Segments are available for targeting immediately after user trait and segment qualification, bolstering real-time targeting efforts.

* You can leverage the campaign data for such use cases as frequency capping across creatives, retargeting users who were exposed to previous campaigns, and analyzing downstream site behavior and entry points.

* The aggregated data provides a unified view of campaign performance, helps identify custom conversion paths, and can be used to improve the sequence of events that lead to conversions through Audience Manager [!DNL Audience Optimization Reports] or through an [[!DNL Audience Analytics] integration with Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## How the data is tracked

The Audience Manager impression and click event pixels are cookie-based. The pixels don't capture events that occur in environments without cookies, such as mobile apps and connected TV (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Impression-tracking pixels

Audience Manager tracks impression data for an ad when you attach a 1xl-pixel transparent event tracking pixel to the ad. The event pixel is loaded each time the ad is served to a user and loaded by the web browser. The pixel is loaded from a client-specific subdomain of [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), which is a legacy domain for Audience Manager, and contains parameters as key-value pairs. The event call collects impression and conversion data and sends it to the Audience Manager data collection servers.

### Click-tracking pixels

Audience Manager tracks clicks similarly to impressions, except that it doesn't load the transparent event pixel each time the ad is served. Instead, the click data is tracked in the ad's click-through URL. The ad points to a client-specific subdomain of [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), which is a legacy domain for Audience Manager, for processing by the Audience Manager data collection servers. The server then redirects the user to the intended landing page. The URL contains parameters as key-value pairs.

>[!NOTE]
>
>If your organization uses [!DNL Analytics] tracking, then you may not need Audience Manager click tracking. Adobe Analytics captures click signals and can send them to Audience Manager through [server-side forwarding](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Collect click and impression data from Advertising DSP campaigns](collect.md)
>* [Use cases](use-cases.md)
