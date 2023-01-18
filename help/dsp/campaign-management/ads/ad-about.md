---
title: About Ad Management in Advertising DSP
description: Learn about ad management.
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
---
# About Ad Management in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP supports ad delivery via third-party ad serving tags (such as Google, Flashtalking, or Sizmek) for various ad types and the direct asset upload for native display ads. You can upload third-party tags individually or in bulk. Bulk uploads use partner tag sheets or a bulk tag template. 

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Once your ads are set up, you'll need to attach each ad to a placement, which includes the targeting parameters (such as geo, audience, device, and inventory targeting) that will control how your campaign will deliver. You can attach a single ad to one or multiple placements.

## Available Ad Types {#ad-types}

All of the following ad types are available in DSP. For full specifications for each ad type, see the [Ad Specifications](ad-specs.md).

* **Audio Ads (third-party only)**: Audio ads play between content on digital publisher sites and can be run standalone as audio files or along with companion banners. Audio is best used to drive brand awareness and engage with on-the-go audiences. Key performance indicators for audio include [!UICONTROL Completion Rate] and [!UICONTROL Cost per Completion].

* **Display Ads (third-party only)**: Display ads are animated or static images displayed in web browsers or in apps. Clicking on the ad unit takes the user to a branded site or microsite. Display is best used to drive efficient CPMs, increase message association, add additional brand or product touchpoints, and drive users down the purchase funnel. Key performance indicators for display include [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions], and [!UICONTROL Cost per Conversion]. DSP supports a wide variety of display banner ad sizes.

* **Mobile Ads (third-party only)**: Mobile ads can be in pre-roll video (VAST, MRAID) or standard display format. Mobile pre-roll video can be auto-play or click-to-play and is best used for reaching viewers across screens. Mobile standard display is a static image displayed on mobile web browsers or in apps and is best used to complement digital video buys, drive message association, and add additional branding or product touchpoints. Mobile ads can also function as full-screen takeovers or as mobile interstitials, which are full-screen, high-impact mobile ads that are best used to develop brand awareness for mobile audiences and drive conversions.

* **Native Display Ads (first-party only)**: Native ads are supported in standard display format. Native ads include a headline and/or title, description, logo, and image. The ad elements are combined and rendered to match the publisher's page style so that the ad blends in with the publisher's organic content and drives higher engagement. Native is best used for brand awareness and for driving audience view and engagement rates with viewer-friendly advertising. Key performance indicators include [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions], and [!UICONTROL Cost Per Conversion].

* **Pre-roll Ads (third-party only)**: Pre-roll ads (VAST and VPAID) are shown before premium video content and provide an immersive, engaging viewer experience. Pre-roll video can be interactive, contain rich media features, and include overlays, rollovers, and calls-to-action. Key performance indicators for pre-roll video ads include [!UICONTROL Video Completion Rate] and [!UICONTROL Viewability Rate].

* **Connected TV Ads (third-party only)**: Connected TV ads are shown before and during premium TV video content. All connected TV inventory runs on TV devices, meaning that video plays automatically in a lean-back, full-screen environment that viewers can't skip. Connected TV is the closest digital video format to TV commercials. Key performance indicators for Connected TV include [!UICONTROL Completion Rate].

* **Universal Video Ads (third-party only)**: Universal Video ads combine all the capabilities of Connected TV, Pre-roll and Mobile Pre-roll Ads (VAST and VPAID) into one and are shown before and during video content. Universal Video ad can be used when targeting video inventory from Desktop, Mobile and Connected TV environments and thus avoids the need to create multiple video ads. Key performance indicators for Universal Video include [!UICONTROL Completion Rate] and [!UICONTROL Viewability Rate].

## DSP Ad Approvals

When you create an ad, DSP reviews it for sensitive categories, click URL functionality, and preview rendering.

Initially, you'll see a red dot in the [!UICONTROL Status] column. The review process normally takes 24-48 hours. A broken ad, however, may have a pending status for longer than 48 hours so you have time to fix errors before the ad is rejected. Rejected ads include a reason for the rejection.

When DSP approves an ad, you'll see a green dot in the Status column.

![approval indicator in [!UICONTROL Status] column](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Your ad will only be served if both DSP and the SSP have approved the creative. Each SSP has its own approval requirements and process.

>[!MORELIKETHIS]
>
>* [Create a Single Ad](ad-create.md)
>* [Create Multiple Third-party Ads](ad-create-multiple.md)
>* [Ad Specifications](ad-specs.md)
