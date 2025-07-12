---
title: Export and implement an ad experience tag for a live experience
description: Learn how to export an ad experience tag and optionally upload it to an Advertising DSP campaign.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
---
# Export and implement an ad experience tag for a live experience

*Closed beta*

Once an ad tag for a specific creative size is available for a [live](experience-about.md#experience-statuses) experience, you can generate and copy the tag in JavaScript and iframe formats for implementation on Advertising DSP or other DSPs. The tags for DSP include all macros required for DSP.

Advertisers with Advertising DSP can optionally upload tags directly to an Advertising DSP campaign as ads with the ad type "standard display" or "universal video."

>[!NOTE]
>
>* When you create an experience with decision tree targeting, [!DNL Creative] automatically creates an ad tag for each applicable creative size.
>* When you create an experience without decision tree targeting, you must [manually create an ad tag](experience-tag-create-manually.md) for each applicable creative size.
>* Experience tags are dynamic. You don't need to update the tags if you edit an experience.
>* Make sure that the campaigns in which you'll implement an ad experience include targeting that's compatible with the experience. Hierarchical targeting behavior may vary by DSP. In Advertising DSP, ad-level targeting is applied on top of (not instead of) placement-level targeting.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Do one of the following:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Tag Manager]**.
     
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Tag Manager]**.

1. Hold the cursor over the row for the applicable ad tag and click either ![Export ad tags](/help/creative/assets/export.png "Export ad tags") **[!UICONTROL Export ad tags]** or **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

>[!NOTE]
>
>For standard video ad experiences, wait until the [!UICONTROL Tag Status] column shows "[!UICONTROL Ready]," which indicates that all videos in the experience have been transcoded. All video creatives are automatically transcoded by DSP, but you can optionally [apply publisher-specific transcoding](experience-tag-video-transcoding.md) to any video ad experience tag.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Optional) On the [!UICONTROL Macros] tab, specify up to five custom macros to include in the tag. For each macro to include:

   1. Select a check box.<!-- Explain more -->

   1. Enter the custom macro.<!-- Explain more -->

1. Click **[!UICONTROL Next]** in the upper right or click **[!UICONTROL Generate ad tags]** in the left menu.

1. Select the tag type: ** *JavaScript<!-- sic -->*  ** or ** *IFRAME* ** <!-- sic -->.

1. In the [!UICONTROL Destinations] list, select where you'll create ads for the experience.

   * *Generic:* For ads you'll create in other DSPs. **Note:** You may need to manually include [additional macros](/help/creative/creative-macros.md) as necessary.

   * *Adobe AdCloud:* For ads you'll create in Advertising DSP.

   * *Google CM360:* For ads you'll create in [!DNL Google Campaign Manager 360]. **Note:** You may need to manually include [additional macros](/help/creative/creative-macros.md) as necessary.

1. Click **[!UICONTROL Generate tags]**.

1. Copy or download the tags:

   * To copy a tag for a single ad size, expand the tag row, hold the cursor over the row, and then click ![Copy](/help/creative/assets/copy.png "Copy") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->
   
   * To download all generated tags as a file to your browser's default download location, click ![Download tags](/help/creative/assets/download.png "Download tags").
   
   You can open the file in a text editor to copy each tag. For JavaScript tags, the tag is enclosed in `<script></script>` and `<noscript></noscript>`tags. For iframe tags, the tag is enclosed in `<iframe></iframe>` tags.

1. Implement the tags for the relevant DSP:

   * For DSPs other than Advertising DSP, provide the tags to whomever will create the ads within the DSP.

   * For Advertising DSP:

      1. Click **[!UICONTROL Next]** in the upper right or click **[!UICONTROL DSP link]** in the left menu.

      1. Select the campaign to which you want to upload the ad tag.

      1. Click **[!UICONTROL Assign Tags]**.

         DSP opens to the [!UICONTROL Ads] view for the selected campaign.

      1. In the [!UICONTROL Create ads] view, review the ad tags, select each tag for which you want to create an ad, and then click **[!UICONTROL Create]**.
      
<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Manually create an ad tag for an applicable creative size](experience-tag-create-manually.md)
>* [Assign creatives to an ad tag for experiences without targeting](experience-tag-assign-creatives.md)
>* [Rename an ad tag](experience-tag-rename.md)
>* [Customize transcoding options for a video ad experience tag](experience-tag-video-transcoding.md)
