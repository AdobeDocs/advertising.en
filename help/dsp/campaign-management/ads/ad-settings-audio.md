---
title: Audio Ad Settings
description: See descriptions of the available ad settings for audio ads.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
---
# Audio Ad Settings

## [!UICONTROL Insert Ad Tag]

*New ads only*

**[!UICONTROL URL]**: The VAST tag URL.

**[!UICONTROL Title]**: A name for the file, which is used in the [!UICONTROL Ads] view and reports.

>[!TIP]
>
> To check the validity of a VAST tag, paste it into a browser and hit the **[!UICONTROL Enter]** key. If the tag is valid, you will see an XML file that includes `<VAST>` near the top.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Read-only) The ad type you're creating, which corresponds to the placement type to which the ad can be attached. It defaults to *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** The ad name. The asset title is used by default, but you can change the name.

>[!TIP]
>
> Use a name that will be easy to find when you attach the ad to a placement, in the [!UICONTROL Ads] view, and in reports. For example, describe the unit type and some key attributes (such as Holiday Product Preview: 30sec Audio").

**[!UICONTROL Ad Duration]:** The length of the audio file. It's automatically set as either [!UICONTROL 15] or [!UICONTROL 30], depending on the selected ad unit.

This field may or may not be displayed, depending on the account permissions.

**[!UICONTROL VAST Tag]:** (Ads using VAST tags only) An URL for a third-party ad source. Make sure that the VAST tag includes only audio media files.

**[!UICONTROL Final VAST Tag]:** (Ads using VAST tags only) The URL for the third-party ad source with the necessary [Advertising DSP tracking macros](/help/dsp/campaign-management/macros.md) inserted, if applicable.

**[!UICONTROL Select Rate]:** (Users with permission only) A pre-negotiated rate billed through Adobe, or one of the rates that you've negotiated and is billed through the vendor. To add a rate, contact your Adobe Account Team.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [List the Placements Associated with an Ad](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Ad Specifications](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
