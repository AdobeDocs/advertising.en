---
title: Display Ad Settings
description: See descriptions of the available ad settings for display ads.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
---
# Display Ad Settings

The following settings are for standard display ads.

## [!UICONTROL Ad Options]

### Basic

**[!UICONTROL Ad Type]:** (Read-only) The ad type you're creating, which corresponds to the placement type to which the ad can be attached. It defaults to *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** The ad name. The asset title is used by default, but you can change the name.

>[!TIP]
>
> Use a name that will be easy to find when you attach the ad to a placement, in the [!UICONTROL Ads] view, and in reports. For example, describe the unit type and some key attributes (such as Holiday Product Preview: 300x250 Gamer”).

**\[Ad Source\]**: (Read-only) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Third-party ads only) Indicates the ad is an expandable banner ad. The related expansion settings determine which inventory to buy, so make sure they reflect the ad behavior.

**[!UICONTROL Expansion Method]:** (Third-party expandable banner ads only) Whether the banner expands upon *[!UICONTROL Click]* or *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Third-party expandable banner ads only) The direction in which the ad expands: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*, or *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Third-party expandable banner ads only) The certified vendor for which the ad is available: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*, or *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Third-party ads only) The URL of the third-party creative asset. Any [timestamp] and [[timestamp]] parameters will be replaced with actual values.

**[!UICONTROL Final Display Code]:** (Third-party ads only) The URL for the third-party creative asset, with the necessary [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) inserted, if applicable.

**[!UICONTROL Ad Size]:** The width and height of the ad. It must be a [supported standard display ad size](ad-specs.md). You can manually enter the ad size before you upload the ad or enter a [!UICONTROL Display Code]. If you don't enter the ad size, the dimensions of the uploaded ad or ad tag are automatically entered as read-only. Note that the Display ad will not save if the dimensions are not within Standard Display as sizes - e.g. 301x250 instead of 300x250 ad size.

>[!IMPORTANT]
>
> The ad size declared in the width and height fields will be matched with incoming bid requests. You may experience delivery issues if the ad's dimensions don't match the declared ad size.

### [!UICONTROL Pixel]

All existing event tracking pixels for the placement are automatically attached. You can detach existing pixels and create new pixels as needed, based on your tracking needs for the individual ad. **Tip:** To edit the third-party tracking pixels for multiple ads in a placement at once using the [!UICONTROL Ad Tools] view, see "[Attach Third-Party Tracking Pixels to Ads in a Placement](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads)."

The following settings apply to each pixel that you create or edit.

**[!UICONTROL Integration Event]:** The event that triggers the pixel to fire. For this ad type, use pixels that fires on the *[!UICONTROL Impression]* or *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Whether the pixel is an *[!UICONTROL IMG URL]* (1x1 pixel image file), *[!UICONTROL HTML]*, or *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** The URL of the pixel image, in the appropriate format for the specified [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** The pixel name. Use a name that helps you easily identify the pixel.

**[!UICONTROL Pixel Provider]:** The pixel provider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, or *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [List the Placements Associated with an Ad](ad-list-placements.md)
>* [Ad Specifications](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
