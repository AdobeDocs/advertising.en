---
title: Manage Bid Multipliers for Placements
description: Learn how to create and edit bid multipliers for specified placement targets.
feature: DSP Placements
---
# Manage Bid Multipliers for Placements

>[!NOTE]
>
>You can change only the bid multipliers for your existing placement targets using this feature. To change the selected targets for your placements, see "[Edit a Placement](/help/dsp/campaign-management/placements/placement-edit.md)."

## Manage the Bid Multipliers for One or More Placements

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Select the check box next to each placement whose bid multipliers you want to manage.

   The same changes will be made to all of the selected placements.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Adjust the bid multipliers for eligible target manually or by uploading a CSV file with target values:

   *  To manually adjust the bid multiplier values, move to each target-specific tab ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], [!UICONTROL Brand Safety]<!--verify all-->) and edit the existing values for the placement targets.

   * To upload a CSV file with bid multiplier values that will overwrite the existing values:

     1. Click **[!UICONTROL CSV Edit]** in the upper right.

     1.  Either drag and drop a file into the box, or click inside the box to select a file from your device or network.

        The file must include the headers (column names) "XXX" and "XXX" and data rows with a value in each column.<!-- Fill in full specs somewhere -- probably in a section below --> 

    1. Click **[!UICONTROL Upload]**.

   By default, the bid multiplier for a target is 1.00, which means the bid isn't adjusted for that target. Values can range from 0.10 to 10.00. For example, a bid modifier of 0.5 decreases a USD 6 bid to USD 3 (0.5 x 6).
   
   When an auction qualifies for multiple bid modifiers, all of the applicable bid modifiers are multiplied.
   
   Bid modifiers never increase the bid to more than the maximum bid.

1. Click **[!UICONTROL Save]**.

## Upload a Spreadsheet to Manage the Bid Multipliers for One or More Placements<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? -->

You can manage the bid multipliers for multiple placements using a [!DNL Microsoft Excel] spreadsheet.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. <!-- Fill in the rest. -->

1. 

1. 


## Maximum Number of Bid Multipliers by Target Type

You can set bid multipliers (with values other than 1.00) for a limited number of targets. For example, you can set bid multipliers for up to 20 country targets. The maximum number of targets for each target type that can have bid multipliers are listed below.

| Category | Parameter | Maximum Number |
| -------- | --------- | ----- |
| Geo | Country | 20 |
| Geo | State | 100 |
| Geo | City | 100 |
| Geo | Metro | 100 |
| Geo | Postal codes | 100 |
| Inventory | Sources | 100 |
| Inventory | Feeds | 100 |
| Sites | Site Category | 100 |
| Sites | Sites/Apps | 100 |
| Audience | Segments | 500 |
| Audience | Topics | 100 |
| Brand Safety | Ads.txt | N/A |

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit a Placement](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
