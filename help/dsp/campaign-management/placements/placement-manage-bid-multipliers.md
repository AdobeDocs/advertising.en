---
title: Manage Bid Multipliers for Placements
description: Learn how to create and edit bid multipliers for specified placement targets.
feature: DSP Placements
exl-id: fbd44960-c9df-4713-94b7-13bcdb7e2568
---
# Manage Bid Multipliers for Placements

You can change the bid multipliers for your existing placement targets using this feature. You can manage the bid multipliers for one placement at a time.<!-- remove that line once we can edit multiple -->

To change the selected targets for your placements, see "[Edit a Placement](/help/dsp/campaign-management/placements/placement-edit.md)."

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Move to each [target-specific tab](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], and [!UICONTROL Brand Safety]) and edit the existing values for the placement targets. Most target categories list sub-categories on the left. Click a sub-category to manage bid multipliers for that sub-category, when it's applicable.

   By default, the bid multiplier for a target is 1.00, which means the bid isn't adjusted for that target. Values can range from 0.10 to 10.00. For example, a bid modifier of 0.5 decreases a USD 6 bid to USD 3 (0.5 x 6). Bid modifiers never increase the bid to more than the maximum bid.
   
   When an auction qualifies for multiple bid modifiers, all of the applicable bid modifiers are multiplied.
   
   You can set bid multipliers (with values other than 1.00) for a [limited number of targets](#bid-multiplier-limits-by-target).

1. In the upper right, click **[!UICONTROL Save]**.

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
>* [Edit a Placement](placement-edit.md)
>* [View the Change Log for a Placement](placement-change-log.md)
>* [Placement Settings](placement-settings.md)
