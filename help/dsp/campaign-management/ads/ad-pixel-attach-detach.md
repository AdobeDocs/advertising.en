---
title: Attach and Remove Pixels from Ads
description: Learn how to attach and remove third-party tracking pixels from ads.
feature: DSP Ads
exl-id: 7b386a58-5300-49cf-9de8-4ce982a5181d
---
# Attach and Remove Pixels from Ads

You can attach and detach third-party tracking pixels from ads.

## Open the [!UICONTROL Ad Tools] View {#ad-tools-open}

1. In the main menu, click **[!UICONTROL Campaigns]**.
     
1. Click the name of the campaign.

1. Open the [!UICONTROL Ad Tools] view in any of the following ways:

   * (From the [!UICONTROL Campaigns] view) Next to the campaign name, click **[!UICONTROL ...]** > **[!UICONTROL Ad Tools].**

   * (From the [!UICONTROL Packages] , [!UICONTROL Placements], or [!UICONTROL Ads] view) In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

## Attach Third-Party Tracking Pixels to Ads in a Placement {#attach-pixels-ads}
     
1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

   The **[!UICONTROL Attach Pixels]** tab opens.

1. In the [!UICONTROL Edit] subview:

   1. (Optional) Locate ads and third-party pixels in any of the following ways:

      * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by ad status, ad type, pixel integration event, or pixel type.
   
      * Above the right and left tables, search for specific text strings in the ad names and pixel names.
   
   1. (If no third-party tracking pixels exist for the campaign) Create a pixel:

      1. In the right table, click **[!UICONTROL Create pixel]**.

      1. Specify the settings:

         **[!UICONTROL Integration Event]:** The event that triggers the pixel to fire, such as *[!UICONTROL Impression]* or *[!UICONTROL Click-through]*.
         
         **[!UICONTROL Pixel Type]:** Whether the pixel is an *[!UICONTROL IMG URL]* (1x1 pixel image file), *[!UICONTROL HTML]*, or *[!UICONTROL JavaScript URL]*.
         
         **[!UICONTROL Pixel URL or Code]:** The URL of the pixel image, in the appropriate format for the specified Pixel Type.
         
         **[!UICONTROL Pixel Name]:** The pixel name. Use a name that helps you easily identify the pixel.
         
         **[!UICONTROL Pixel Provider]:** The pixel provider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, or *[!UICONTROL IAS]*.

      1. Click **[!UICONTROL Save]**.

   1. In the left table, select the check box next to each ad for which you want to attach third-party tracking pixels.

   1. In the right table, select the check box next to each third-party tracking pixel you want to attach to the selected ads.

      Only pixels that aren't already attached to the selected ads are selectable.

   1. In the bottom right, click **[!UICONTROL Attach]**.

1. (Optional) To return to the campaign detail views, click ![Return to folder](/help/dsp/assets/breadcrumb-return.png "Return to folder") to the left of [!UICONTROL Ad Tools] and select the campaign name.

## Detach Third-Party Tracking Pixels from Ads in a Placement {#detach-pixels-ads}
     
1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

   The **[!UICONTROL Attach Pixels]** tab opens.

1. In the [!UICONTROL Edit] subview:

   1. (Optional) Locate ads and third-party pixels in any of the following ways:

      * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by ad status, ad type, pixel integration event, or pixel type.
   
      * Above the right and left tables, search for specific text strings in the ad names and pixel names.
   
   1. In the left table, select the check box next to each ad from which you want to detach third-party tracking pixels.

   1. In the right table, select the check box next to each third-party tracking pixel you want to detach from the selected ads.

      Only pixels that are attached to all selected ads are selectable.

   1. In the bottom right, click **[!UICONTROL Detach]**.

1. (Optional) To return to the campaign detail views, click ![Return to folder](/help/dsp/assets/breadcrumb-return.png "Return to folder") to the left of [!UICONTROL Ad Tools] and select the campaign name.

## View Pixels Attached to Ads {#view-pixels-ads}

1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

   The **[!UICONTROL Attach Pixels]** tab opens.

1. Switch to the **[!UICONTROL View]** option in the upper right.

1. (Optional) Locate ads and third-party pixels as needed:

      * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by ad status, ad type, pixel integration event, or pixel type.
   
      * Above the right and left tables, search for specific text strings in the ad names and pixel names.

1. Click any ad row in the left table to see the attached pixels in the right table.

1. (Optional) To attach more pixels to the ads, switch to the **[!UICONTROL Edit]** view in the upper right. See Step 3 in the previous procedure, "[Attach Third-Party Tracking Pixels to Ads in a Placement](#attach-pixels-ads)," for instructions.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Attach Ads to Placements](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [Create a Single Ad](ad-create.md)
>* [Create Multiple Third-party Ads](ad-create-multiple.md)
>* [Edit an Ad](ad-edit.md)
>* [List the Placements Associated with an Ad](ad-list-placements.md)
>* [Edit the Ad Schedules for Placements](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [FAQs About Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
