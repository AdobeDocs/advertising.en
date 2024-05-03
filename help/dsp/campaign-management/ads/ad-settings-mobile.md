---
title: Mobile Ad Settings
description: See descriptions of the available ad settings for mobile ads.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
---
# Mobile Ad Settings

## [!UICONTROL Insert Ad Tag]

*New mobile video ads formats only*

**[!UICONTROL URL]** or **[!UICONTROL Ad Tag]**: A third-party VAST ad tag or ad tag that contains creative assets and tracking pixels

**[!UICONTROL Ad Title]** or **[!UICONTROL Title]**: A name for the ad that is used in the [!UICONTROL Ads] view and reports.

>[!TIP]
>
> To check the validity of a VAST tag, paste it into a browser and hit the **[!UICONTROL Enter]** key. If the tag is valid, you will see an XML file that includes `<VAST>` near the top.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Mobile Display Ads

**[!UICONTROL Ad Type]:** (Read-only) The ad type you're creating, which corresponds to the placement type to which the ad can be attached.

**[!UICONTROL Ad Name]:** The ad name. The asset title is used by default, but you can change the name.

>[!TIP]
>
> Use a name that will be easy to find when you attach the ad to a placement, in the Ads view, and in reports. For example, describe the unit type and some key attributes (such as Holiday Product Preview: 300x250 Gamer”).

**\[Ad Source\]**: (Read-only) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** The URL of the third-party creative asset. Any [timestamp] and [[timestamp]] parameters will be replaced with actual values.

**[!UICONTROL Final Display Code]:** The URL for the third-party creative asset, with the necessary [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) inserted, if applicable.

### [!UICONTROL Basic]: Video Ads

**[!UICONTROL Ad Type]:** (Read-only) The ad type you're creating, which corresponds to the placement type to which the ad can be attached.

**[!UICONTROL Ad Name]:** The ad name. The asset title is used by default, but you can change the name.

>[!TIP]
>
> Use a name that will be easy to find when you attach the ad to a placement, in the Ads view, and in reports. For example, describe the unit type and some key attributes (such as Holiday Product Preview: 30sec Phone Preroll”).

**[!UICONTROL Width] | [!UICONTROL Ad Unit Width]:** The width of the entire ad unit. This option may be locked depending on the type of ad unit you selected.

**[!UICONTROL Height] | [!UICONTROL Ad Unit Height]:** The height of the entire ad unit. This option may be locked depending on the type of ad unit you selected.

**[!UICONTROL Player X]:** The X coordinate for the ad unit. Keep the default setting.

**[!UICONTROL Player Y]:** The Y coordinate for the ad unit. Keep the default setting.

**[!UICONTROL Player Width]:** The width of the entire ad unit. This option may be locked depending on the type of ad unit you selected.

This is the same as the **[!UICONTROL Width]** field.

**[!UICONTROL Player Height]:** The height of the entire ad unit. This option may be locked depending on the type of ad unit you selected.

This is the same as the **[!UICONTROL Height]** field.

**[!UICONTROL Show Controls]:** Where to include video controls for the ad: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, or *[!UICONTROL None]* (the default).

**[!UICONTROL Preserve Aspect Ratio]:** Whether to to keep the video's width and height proportions (*[!UICONTROL Yes]*) or to stretch the video to fill available space (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Some ad types) The number of seconds to delay the appearance of the close button.

**[!UICONTROL VAST Tag]:** (Ads using VAST tags only; read-only) The third-party VAST tag you entered as the creative asset.

**[!UICONTROL Final VAST Tag]:** (Ads using VAST tags only; read-only) The third-party VAST tag you entered as the creative asset with the necessary [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) inserted, if applicable.

**[!UICONTROL Wmode]:** (Some ad types) The window mode: *[!UICONTROL window]*, *[!UICONTROL transparent]*, or *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

All existing event tracking pixels for the placement are automatically attached. You can detach existing pixels and create new pixels as needed, based on your tracking needs for the individual ad. **Tip:** To edit the third-party tracking pixels for multiple ads in a placement at once using the [!UICONTROL Ad Tools] view, see "[Attach Third-Party Tracking Pixels to Ads in a Placement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)."

The following settings apply to each pixel that you create or edit.

**[!UICONTROL Integration Event]:** The event that triggers the pixel to fire. For this ad type, use pixels that fires on the *[!UICONTROL Impression]* or *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Whether the pixel is an *[!UICONTROL IMG URL]* (1x1 pixel image file), *[!UICONTROL HTML]*, or *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** The URL of the pixel image, in the appropriate format for the specified [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** The pixel name. Use a name that helps you easily identify the pixel.

**[!UICONTROL Pixel Provider]:** The pixel provider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, or *[!UICONTROL IAS]*.

### [!UICONTROL Sharing]

Deprecated

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [List the Placements Associated with an Ad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Ad Specifications](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
