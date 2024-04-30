---
title: Attach Ads to Placements
description: Learn how to attach ads to placements.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
---
# Attach Ads to Placements

Use the [!UICONTROL Ad Tools] view to attach ads to placements, attach third-party tracking pixels to the ads, and detach existing third-party tracking pixels from the ads.

>[!NOTE]
>
>Universal video ads can be attached only to universal video placements.

## Open the [!UICONTROL Ad Tools] View {#ad-tools-open}

1. In the main menu, click **[!UICONTROL Campaigns]**.
     
1. Click the name of the campaign.

1. Open the [!UICONTROL Ad Tools] view in any of the following ways:

   * (From the [!UICONTROL Packages] , [!UICONTROL Placements], or [!UICONTROL Ads] view) In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**.

   * (From the [!UICONTROL Placements] view) Next to the placement name, click **[!UICONTROL ...]** > **[!UICONTROL Attach Ads].**

   * (From the [!UICONTROL Ads] view) Next to the ad name, click  **[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**.

   The [!UICONTROL Attach Ads] tab is selected by default.

## Attach Ads to Placements {#attach-ads-campaign}

1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

1. In the [!UICONTROL Edit] subview, do the following for each group of ads you want to attach to placements:

   1. (Optional) Locate specific placements and ads in any of the following ways:

      * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by package, placement type, placement status, ad type, or ad status.
   
      * Above the right and left tables, search for specific text strings in the placement and ad names.
   
   1. In the left table, select the check box next to each placement to which to attach the ads.

   1. In the right table, select the check box next to each ad you want to attach to the selected placements.

      Only ads that are applicable for the placement type and that aren't already attached to the selected placements are selectable.

   1. In the bottom right, click **[!UICONTROL Attach]**.

1. (Optional) To return to the campaign detail views, click ![Return to folder](/help/dsp/assets/breadcrumb-return.png "Return to folder") to the left of [!UICONTROL Ad Tools] and select the campaign name.

## View Ads Attached to Placements {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

1. Switch to the **[!UICONTROL View]** option in the upper right.

1. (Optional) Locate specific placements and ads as needed:

   * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by package, placement type, placement status, ad type, or ad status.
   
   * In the right and left tables, search for specific text strings in the placement or ad name.

1. Click any placement row in the left table to see the attached ads in the right table.

1. (Optional) To attach more ads to the campaign's placements, switch to the **[!UICONTROL Edit]** view in the upper right. See Step 2 in the previous procedure, "[Attach Ads to Placements](#attach-ads-campaign)," for instructions.

## Attach Third-Party Tracking Pixels to Ads in a Placement {#attach-pixels-ads}
     
1. [Open the [!UICONTROL Ad Tools] view](#ad-tools-open).

1. Click the **[!UICONTROL Attach Pixels]** tab.

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

1. Click the **[!UICONTROL Attach Pixels]** tab.

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

1. Click the **[!UICONTROL Attach Pixels]** tab.

1. Switch to the **[!UICONTROL View]** option in the upper right.

1. (Optional) Locate ads and third-party pixels as needed:

      * Above the left table, click ![Filter](/help/dsp/assets/filter.png) and filter the lists by ad status, ad type, pixel integration event, or pixel type.
   
      * Above the right and left tables, search for specific text strings in the ad names and pixel names.

1. Click any ad row in the left table to see the attached pixels in the right table.

1. (Optional) To attach more pixels to the ads, switch to the **[!UICONTROL Edit]** view in the upper right. See Step 3 in the previous procedure, "[Attach Third-Party Tracking Pixels to Ads in a Placement](#attach-pixels-ads)," for instructions.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [Create Multiple Third-party Ads](ad-create-multiple.md)
>* [Edit an Ad](ad-edit.md)
>* [List the Placements Associated with an Ad](ad-list-placements.md)
>* [Edit the Ad Schedules for Placements](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [FAQs About Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
