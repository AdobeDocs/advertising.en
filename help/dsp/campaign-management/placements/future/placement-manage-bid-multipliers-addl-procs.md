---
title: Manage Bid Multipliers for Placements
description: Learn how to create and edit bid multipliers for specified placement targets.
feature: DSP Placements
---
# Manage Bid Multipliers for Placements


<!--

See if any of these procedures are implemented; may need to be edited and/or re-worded based on functionality/UI

-->

You can change the bid multipliers for your existing placement targets using this feature.

To change the selected targets for your placements, see "[Edit a Placement](/help/dsp/campaign-management/placements/placement-edit.md)."

## Manage the Bid Multipliers for One or More Placements

For all selected placements, you can either manually edit values or upload a spreadsheet with values.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Select the check box next to each placement whose bid multipliers you want to manage.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Adjust the bid multipliers for eligible target manually or by uploading a CSV file with target values:

   *  To manually adjust the bid multiplier values, move to each target-specific tab ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], [!UICONTROL Brand Safety]<!--verify all-->) and edit the existing values for the placement targets.

     The same changes will be made to all of the selected placements.

   * To upload a CSV file with bid multiplier values that will overwrite the existing values:

     1. Click **[!UICONTROL CSV Edit]** in the upper right.

     1. Either a) click **[!UICONTROL Download Template]** and edit the bid multiplier values or b) edit a previously-downloaded template. Save the edited file to your device or network.

     1.  Either a) drag and drop the edited file into the box or b) click inside the box to select the file from your device or network. 

    1. Click **[!UICONTROL Upload]**.

   By default, the bid multiplier for a target is 1.00, which means the bid isn't adjusted for that target. Values can range from 0.10 to 10.00. For example, a bid modifier of 0.5 decreases a USD 6 bid to USD 3 (0.5 x 6). You can set bid multipliers (with values other than 1.00) for a [limited number of targets](#bid-multiplier-limits-by-target).
   
   When an auction qualifies for multiple bid modifiers, all of the applicable bid modifiers are multiplied.
   
   Bid modifiers never increase the bid to more than the maximum bid.

1. Click **[!UICONTROL Save]**.

-->

## Upload a Spreadsheet to Manage the Bid Multipliers for a Single Placement<!-- Is this still going to exist independently, or will you just do this via the "Bid Multiplier" option in the main context menu for placements? If both options, then reword headings for distinction -->

Changes in the uploaded file overwrite the existing bid multiplier values.<!-- what if you delete a row? -->

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Upload Bid Multiplier Excel Sheet]**.

1. <!-- Verify the rest of these steps. -->

1. Either a) click **[!UICONTROL Download Template]** and edit the bid multiplier values or b) edit an previously-downloaded template. Save the edited file to your device or network.

   By default, the bid multiplier for a target is 1.00, which means the bid isn't adjusted for that target. Values can range from 0.10 to 10.00. For example, a bid modifier of 0.5 decreases a USD 6 bid to USD 3 (0.5 x 6). You can set bid multipliers (with values other than 1.00) for a [limited number of targets](#bid-multiplier-limits-by-target).
   
   When an auction qualifies for multiple bid modifiers, all of the applicable bid modifiers are multiplied.
   
   Bid modifiers never increase the bid to more than the maximum bid.

1.  Either a) drag and drop the edited file into the box or b) click inside the box to select the file from your device or network. 

1. Click **[!UICONTROL Upload]**.

1. Click **[!UICONTROL Save]**.<!-- Verify this step -->

## Target Types Eligible for Bid Multipliers {#bid-multiplier-by-target}

* **Geo targets**: countries, states, cities, DMAs, and postal codes

* **Inventory targets**: sources and feeds for private inventory and [!UICONTROL On Demand] inventory

* **Site targets:** site categories, targeted (but not excluded) sites/apps. Not available for keywords.<!-- Clarify this: I don't see a place to specify keywords -->

<!-- Not until Phase 2:  * **Audience targets:** audiences and segments -->

* **Daypart targets:** daypart intervals

* **Topic targets:** topics

* **ads.txt targets:** (When you opt out of ads.txt) ads.txt sellers only, ads.txt direct sellers, and ads.txt sellers plus sites without ads.txt. <!-- ???  Clarify how this will work. -->

## Maximum Number of Bid Multipliers by Target Type {#bid-multiplier-limits-by-target}

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

<!--

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit a Placement](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
 -->
 