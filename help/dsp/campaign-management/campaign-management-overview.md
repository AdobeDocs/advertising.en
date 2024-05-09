---
title: Overview of Campaign Management in Advertising DSP
description: Learn about the campaign management hierarchy and components.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
---
# Overview of Campaign Management in Advertising DSP

DSP campaigns have the following hierarchy:

* Campaign
  * Package(s)
    * Placement(s)
      * Ad(s)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
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
>* [About Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [About Package Management](/help/dsp/campaign-management/packages/package-about.md)
>* [About Placement Management](/help/dsp/campaign-management/placements/placement-about.md)
>* [About Ad Management](/help/dsp/campaign-management/ads/ad-about.md)
>* [Campaign Launch Checklist](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best Practices for Setting up Performance Campaigns](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Types of Performance Reports in Campaign Management Views](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Manage Your Campaign Data Views](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP Account Structure and User Interface](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
