---
title: Edit Ad Schedules for Placements
description: Learn how to change the ad schedules for the ads attached to placements.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
---
# Edit Ad Schedules for Placements

## Edit the Ad Schedules for One or More Placements

You can change the scheduled flight dates and ad rotation for the ads attached to multiple placements using a [!DNL Microsoft Excel] spreadsheet. Each ad can be active during multiple flights.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Select the check box next to each placement whose ad data you want to download.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. When the file is available, click **[!UICONTROL Download]** in the notification at the top of the browser page to download a worksheet file (in XLSX format) according to your browser's normal procedure.

   ![Download Ready notification](/help/dsp/assets/download-ready.png "Download Ready notification")

1. Open the downloaded file, edit the flight information fields for each ad row to include in the flight, and save the updated file:

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (such as [!UICONTROL Flight 1 Start Date] and [!UICONTROL Flight 1 End Date]): The first and last dates of the flight. Use the format YYYY-MM-DD for each date. Any ads with empty flight date fields are treated as non-participating ads.

   * **[!UICONTROL Flight N Weight]** (such as [!UICONTROL Flight 1 Weight]): How to rotate the ads for a flight. Enter a value:

     * To rotate the ads for a flight evenly, enter `[!UICONTROL Even]`.

     * To rotate the ads for a flight unevenly, enter the relative weight by which to rotate each ad, as a percentage (such as `40` for 40%). The total weights for the flight must equal 100.

1. Upload the edited ad schedule template:

   1. Select the check box next to each applicable placement.

   1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**, and specify the file to upload.

## Edit the Ad Schedule for a Single Placement

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

You can change the scheduled flight dates and ad rotation for the ads attached to a placement. Each ad can be active during multiple flights.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

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
>* [Edit a Placement](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
