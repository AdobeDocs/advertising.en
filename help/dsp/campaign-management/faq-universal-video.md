---
title: FAQs about universal video
description: Learn more about universal video ads.
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
TQID: https://experienceleague.adobe.com/LAzSivup-EVuDgtWN1T58lfRjzgrchIiFF9-lMJAVlw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
    internal-label: DSP placements
  - id: d9510790-d834-436d-8423-8d69cd50464a
    internal-label: DSP Ads
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# FAQs about universal video

[Universal video ads](/help/dsp/campaign-management/ads/ad-about.md#ad-types) allow you to target video inventory from desktop, mobile, and connected TV environments for VPAID and VAST inventory using a single video placement.

## How do you create universal video placements and ads?

Universal video placements can contain only universal video ads, and universal video ads can be attached only to universal video placements.

Create universal video placements and ads similarly to how you create other types of placements and videos:

1. Within the desired campaign, [create a universal video placement](/help/dsp/campaign-management/placements/placement-create.md), selecting the [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   You must specify at least one environment (Desktop, Mobile, Connected TV) to target.

1. In the same campaign as the universal video placement, [create a single universal video ad](/help/dsp/campaign-management/ads/ad-create.md) or [create multiple universal video ads](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   If you create multiple ads, make sure to specify "[!UICONTROL Universal Video]" as the [!UICONTROL Ad Type]:
   
   * For [!DNL Google] or [!DNL Flashtalking] ads: In the "[!UICONTROL Review ad types]" step after you upload the file, click the **[!UICONTROL Ad Type]** field and select **[!UICONTROL Universal Video]**.
   
   * For other types of ad tags: Within the spreadsheet file you upload, specify the Ad Type field for each ad as **[!UICONTROL Universal Video]**.

1. [Open the ad settings](/help/dsp/campaign-management/ads/ad-edit.md) for each new ad and select the applicable video format:

   * **[!UICONTROL VPAID]:** Viewability is always measured.
   * **[!UICONTROL VPAID & VAST (Default)]:** Includes inventory that doesn't allow viewability measurement.
   * **[!UICONTROL VAST]** - Suitable for connected TV inventory.

   See "[Universal video ad settings](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)" for more information.

1. [Attach the new universal video ads](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) to the universal video placement.

## Why are some optimization goals and packages unavailable when the connected TV environment is selected for a universal video placement?

Goals that are incompatible with standard connected TV placements, such as Lowest Cost per Click, aren't supported for the connected TV environment in universal video placements. Similarly, packages with incompatible optimization goals are also unavailable for selection. 

## When should the **[!UICONTROL VAST]** video format be used for universal video ads? 

Use **[!UICONTROL VAST]** in either of the following scenarios:

* The placement targets connected TV inventory.
* The placement targets video inventory from Google Ad Manager, Appnexus, SpotX, or FreeWheel. These SSPs don't support the VPAID & VAST video format.

## Is it possible to attach multiple universal video ads to the same universal video placement?

Yes.
