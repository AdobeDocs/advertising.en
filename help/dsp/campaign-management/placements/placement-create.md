---
title: Create a Placement
description: Learn how to create a placement.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
---
# Create a Placement

>[!TIP]
>
>Create placements based on specific campaign goals or reporting needs.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign in which to include the placement.

1. Above the data table, click **[!UICONTROL Create]**. In the [!UICONTROL Placement Types] section of the menu, click the placement type.

    The placement type determines the ad type that the placement can include.

1. Enter the [placement settings](placement-settings.md):

   1. Specify the [!UICONTROL Placement Basics] settings.

   1. In the [!UICONTROL Goals] section, specify the [!UICONTROL Gross Budget] and, optionally, specify additional placement goals.

      Some fields have default values that you can override.

      If the package to which the placement is assigned has package-level pacing, then your goals and pacing settings will reflect the package settings.

   1. (Optional) In the [!UICONTROL Geo-Targeting] section, narrow down the locations that are included or excluded.

      If you don't identify specific locations, all locations are targeted.

      >[!NOTE]
      >
      >City and DMA locations aren't available for Roku placements.

   1. In the [!UICONTROL Inventory Targeting] section, narrow down the inventory sources to include or exclude.

      For most placement types, all inventory types, and all sources for each type, are included by default. For [!DNL Roku] placements, you must specify the inventory type and sources.

   1. (Optional) In the [!UICONTROL Site Targeting] section, narrow down the sites that you want to target, and specify any sites that you want to exclude.

   1. (Optional) In the [!UICONTROL Audience Targeting] section:

      1. Narrow down the audience. This includes selecting audience segments to target within the placement.

         For [!DNL Roku] placements, you can leverage [DSP’s unique audience matching with [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) by including one or more one audience segments that can be matched against the [!DNL Roku] (opted-in) deterministic dataset.

      1. (For campaigns with people-level cross-device targeting; optional) When the placement targets one or more specific audiences, enable people-based cross-device targeting for the placement.

         People-based cross-device targeting is provided by [!DNL LiveRamp] using U.S. data only. The service is available to all advertisers at $0.35 CPM for impressions that are delivered by using the [!DNL LiveRamp] device graph (that is, for devices not found within the targeted audience segments).

   1. (Optional) In the [!DNL Brand Safety and Media Targeting] section, apply brand safety restrictions for your placements.

   1. (Optional) In the [!DNL Tracking] section, enter third-party event pixels or conversion pixels for ads in the placement.

      >[!NOTE]
      >
      >([!DNL Roku] placements) Third-party pixel vendors approved by [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk], and [!DNL Research Now].

1. Click **[!UICONTROL Create Placement]**.

1. (Optional) Attach ads to the placement:

   1. Click **[!UICONTROL Attach an ad]**.

   1. Do either of the following:

      * To create a new ad:

        1. Click **[!UICONTROL Create a New Ad].**

        1. Specify the ad settings for [audio ads](/help/dsp/campaign-management/ads/ad-settings-audio.md), [connected TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [display ads](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobile ads](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [native ads](/help/dsp/campaign-management/ads/ad-settings-native.md), [pre-roll ads](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md), or [universal video ads](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Universal video placements can contain only universal video ads.

        1. Click **[!UICONTROL Save & Submit for Review]**.

        1. (Optional) For each additional ad you want to create for the placement, click **[!UICONTROL Attach Another Ad]**, and then repeat Steps 1-3.

        1. If you won't attach any existing ads, click **[!UICONTROL I'm done for now]**.

       * To attach existing ads in the campaign:

        1. Click **[!UICONTROL Select an Ad]**.

        1. Do either of the following:

            * To add one ad at a time:

              1. Next to the ad name, click **[!UICONTROL Select].**

              1. (Optional) For each additional ad you want to attach, click **[!UICONTROL Attach Another Ad]**, and then repeat the process.

            * To add up to 20 ads at a time:

               1. Select the check box above the ad list.

               1. Select the check box next to each ad to add.

               1. Click **[!UICONTROL Attach]**.

               1. Next to the ad name, click **[!UICONTROL Select]**.

         1. (Optional) To override the default flight period and ad rotation for specific ads in the placement:

            1. Click **[!UICONTROL Custom Schedule Ads]**.

            1. Do any of the following:

               * To add a flight, click **[!UICONTROL Add Flight]**, and then specify the start date and end date.

               * To add an existing flight to an ad, click **[!UICONTROL +]** in the ad row for the flight column.

               * To remove an existing flight from an ad, click **[!UICONTROL x]** in the ad row for the flight column.

               * (When multiple ads have the same flight) To rotate the ads unevenly, click **[!UICONTROL Even Rotation]** in the flight information, and then enter the relative weight by which to rotate each ad, as a percentage.

                  The total weights must equal 100.

            1. In the upper right, click **[!UICONTROL Continue]**.

            1. Review the flight details, and then click **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [Manage Bid Multipliers for Placements](placement-manage-bid-multipliers.md)
>* [Edit the Ad Schedules for Placements](placement-edit-ad-schedule.md)
>* [Pause or Activate a Placement](placement-pause-activate.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
>* [View the Placement Forecast Report](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [FAQs About Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Keyboard Shortcuts](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Troubleshooting Performance](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: How to Create a Standard Display Placement](https://video.tv.adobe.com/v/340454)
