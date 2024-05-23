---
title: Manage Bid Multipliers for Placements
description: Learn how to create and edit bid multipliers for your placement targets.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
---
# Manage Bid Multipliers for Placements

You can create and manage bid multipliers, by which a bid is multiplied to increase or decrease the bid, for your existing placement targets of [eligible target types](#bid-multiplier-by-target). You can either manually edit bid multiplier values or upload a spreadsheet with values.

By default, the bid multiplier for a target is 1.00, which means that the bid isn't adjusted for that target. Values can range from 0.10 to 10.00. For example, a bid modifier of 0.5 decreases a USD 6 bid to USD 3 (0.5 x 6). When an auction qualifies for multiple bid modifiers, all of the applicable bid modifiers are multiplied. Bid modifiers never increase the bid to more than the maximum bid.

You can set bid multipliers (with values other than 1.00) for a [limited number of targets](#bid-multiplier-limits-by-target).

This feature works with your existing placement targets. To change the selected targets for your placements, see "[Edit Placements](/help/dsp/campaign-management/placements/placement-edit.md)."

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Adjust the bid multipliers for eligible targets:

   * To manually adjust the bid multiplier values, move to each [target-specific tab](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], and [!UICONTROL Brand Safety]) and edit the existing values for the placement targets.
   
     Most target categories list sub-categories on the left. Click a sub-category to manage bid multipliers for that sub-category, as applicable.

   * To upload a CSV file with bid multiplier values to overwrite the existing values:

     1. Click **[!UICONTROL CSV File Edit]** in the upper right.

     1. Either a) click **[!UICONTROL Download Template]** and enter the targets using the same syntax visible in the user interface and the corresponding bid multiplier values or b) edit a previously-downloaded template with the same information. Save the edited file to your device or network.

     1.  Click **[!UICONTROL Next]** to move to the [!UICONTROL Upload File] section and either a) drag and drop the edited file into the box or b) click inside the box to select the file from your device or network.

     1. Verify the uploaded data in the [!UICONTROL Review & Submit] section, and then click **[!UICONTROL Save]**.

## Target Types Eligible for Bid Multipliers {#bid-multiplier-by-target}

You can configure bid modifiers only for included targets, not excluded targets.

* **Geo targets**: geography (countries, states, and cities),  postal codes, and DMAs

* **Inventory targets**: sources and feeds for public inventory and [!UICONTROL On Demand] inventory

* **Site targets:** targeted (but not excluded) sites/apps, site categories

* **Audience targets:** segments, dayparts, and topics

* **ads.txt targets:** (When you opt out of ads.txt, which allows you to buy inventory from all sellers) ads.txt sellers only, ads.txt direct sellers, and ads.txt sellers plus sites without ads.txt <!-- bid multipliers for the different subsets of inventory; not available when the placement targets only one subset -->

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

>[!MORELIKETHIS]
>
>* [About Placement Management](placement-about.md)
>* [Edit Placements](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
