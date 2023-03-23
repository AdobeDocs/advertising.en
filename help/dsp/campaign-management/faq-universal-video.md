---
title: FAQs About Universal Video
description: Learn more about universal video ads.
feature: DSP Placements, DSP Ads
---
# FAQs About Universal Video

[Universal video ads](/help/dsp/campaign-management/ads/ad-about.md) allow you to target video inventory from desktop, mobile, and connected TV environments for VPAID and VAST inventory using a single video placement.

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

   See "[Universal Video Ad Settings](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)" for more information.

1. [Attach the new universal video ads](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) to the universal video placement.

## Why are some optimization goals and packages unavailable when the Connected TV environment is selected for a universal video placement?

Goals that are incompatible with standard connected TV placements, such as Lowest Cost per Click, aren't supported for the connected TV environment in universal video placements. Similarly, packages with incompatible optimization goals are also unavailable for selection. 

## When should the **[!UICONTROL VAST]** video format be used for universal video ads? 

Use **[!UICONTROL VAST]** in either of the following scenarios:

* The placement targets connected TV inventory.
* The placement targets video inventory from Google Ad Manager, Appnexus, SpotX, or Freewheel. These SSPs don't support the VPAID & VAST video format.

## Is it possible to attach multiple universal video ads to the same universal video placement?

Yes.
