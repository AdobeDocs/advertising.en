---
title: Overview of campaign management in Advertising DSP
description: Learn about the campaign management hierarchy and components.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
    internal-label: DSP placements
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
    internal-label: DSP Campaigns
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: DSP Ads
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
    internal-label: DSP Packages
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Overview of campaign management in Advertising DSP

DSP campaigns have the following hierarchy:

* Campaign
  * Package(s)
    * Placement(s)
      * Ad(s)
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Campaigns](/help/dsp/campaign-management/campaigns/campaign-about.md) are the overarching framework of flight settings. Each campaign is configured with an advertiser, start and end dates, an overall budget, a cross-device targeting option and default frequency cap, and reporting options for viewability, fraud, brand safety, and audience verification. All campaign-level settings automatically apply to each package and placement within the campaign.

## [!UICONTROL Packages]

Each campaign can contain one or more [packages](/help/dsp/campaign-management/packages/package-about.md), each of which includes a set of placements.

Use packages to group placements for delivery to a set budget, performance goal, and custom pacing strategy. DSP optimizes packages by shifting budgets to the best-performing placements in the package. You can organize packages by placement format, inventory type, data provider, persona, or other distinguishable characteristics.

Packages are optional but recommended.

## [!UICONTROL Placements]

A [placement](/help/dsp/campaign-management/placements/placement-about.md) stores targeting parameters for one or more ads of the same ad type. You can create a placement for a single campaign or package, and then assign ads to it.

## [!UICONTROL Ads]

[Ads](/help/dsp/campaign-management/ads/ad-about.md) include creative assets and tracking URLs. You can upload third-party ad serving tags individually or in bulk by using partner tag sheets or the bulk tag template. You can also manually create native display ads for DSP to serve.

Once your ads are set up, you must attach each ad to a placement to begin running the ad. You can attach a single ad to one or more placements.

All active, approved ads in an active placement in an active campaign are eligible to run based on the placement targeting parameters.

>[!MORELIKETHIS]
>
>* [About campaign management in Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [About package management in Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [About placement management in Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [About ad management in Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign launch checklist](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best practices for setting up performance campaigns](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Types of performance reports in campaign management views](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Manage your campaign data views](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP account structure and user interface](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
