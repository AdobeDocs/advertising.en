---
title: Attach an Ad to a Placement
description: Learn how to attach an ad to a placement.
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
---
# Attach an Ad to a Placement

## Attach a New Ad from the [!UICONTROL Ads] View

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Ads]**.

1. Next to the ad name, click  **... > [!UICONTROL Add to Placements]**.

1. In the Place Ad screen, do either of the following:

    * To create a new placement for the ad:

        1. Click **[!UICONTROL Create New Placement]**.

        1. Enter the [placement settings](/help/dsp/campaign-management/placements/placement-settings.md), and then click **[!UICONTROL Create Placement]**.

    * To add the ad to one or more existing placements:

        1. Click **[!UICONTROL Select a Placement].**

        1. Do either of the following:

            * To add one ad at a time:

                1. Next to the ad name, click **[!UICONTROL Select].**

                1. (Optional) For each additional ad you want to attach, click **[!UICONTROL Attach to Other Placement]**. Next to the ad name, click **[!UICONTROL Select].**

            * To attach the ad to up to 20 placements at a time:

                1. Select the check box next to **Bulk Select."

                1. Select the check box next to each placement to which to attach the ad.

                1. Click **[!UICONTROL Attach]**.

        1. On the Complete & Review tab, select one of the following:

            * To return to the Ads view, click **[!UICONTROL I'm done for now]**.

            * To attach the ad to another placement, click **[!UICONTROL Attach To Other Placement]**.

## Attach a New or Existing Ad from the [!UICONTROL Placements] View

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **... > [!UICONTROL Attach Ads].**

1. In the [!UICONTROL Add Ad to Placement] screen, do either of the following:

    * To create a new ad:

        1. Click **[!UICONTROL Create a New Ad]**.

        1. Enter the ad settings for [audio ads](ad-settings-audio.md), [connected TV](ad-settings-connected-tv.md), [display ads](ad-settings-display.md), [mobile ads](ad-settings-mobile.md), [native ads](ad-settings-native.md), or [pre-roll ads](ad-settings-pre-roll.md).

        1. Click **[!UICONTROL Save & Submit for Review]**.
        
             The [ad review](ad-about.md) for the new ad takes 24-48 hours and includes checks for sensitive categories, click URL functionality, and preview rendering. The [!UICONTROL Status] column indicates whether DSP has approved the ad. Broken ads may have a pending status for longer than 24-48 hours so you have time to fix errors before they're rejected.
             
             >[!NOTE]
             >
             >Your ad will only be served if both DSP and the SSP have approved the creative. Each SSP has its own approval requirements and process.

    * To select existing ads:

        1. Click **[!UICONTROL Select an Ad].**

        1. Specify the ads:
            * To add one ad at a time:

                1. Next to the ad name, click **[!UICONTROL Select].**

                1. (Optional) For each additional ad you want to attach, click **[!UICONTROL Add Another Ad]**. Next to the ad name, click **[!UICONTROL Select].**

            * To add up to 20 ads at a time:

                1. Select the check box next to **[!UICONTROL Bulk Select]**."

                1. Select the check box next to each ad to add.

                1. Click **[!UICONTROL Attach]**.

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

        1. Click **[!UICONTROL I'm done for now]**.

>[!MORELIKETHIS]
>
>* [About Ad Management](ad-about.md)
>* [Create a Single Ad](ad-create.md)
>* [Create Multiple Third-party Ads](ad-create-multiple.md)
>* [Edit an Ad](ad-edit.md)
>* [List the Placements Associated with an Ad](ad-list-placements.md)
>* [Edit the Ad Schedule for a Placement](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
