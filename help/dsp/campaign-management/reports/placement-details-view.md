---
title: View the Sites, Ads, Frequency, and Inventory Details for a Placement
description: Learn how to view the targeted sites, ads, frequency, and inventory data for a placement.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
---
# View the Sites, Ads, Frequency, and Inventory Details for a Placement

For each placement, you can [open a (detail view [!UICONTROL Inspector])](placement-details-view.md), which lists all targeted sites, ads, and deals in a placement. It also includes frequency data for the placement. You can optionally export the data from any tab.

![placement Inspector](/help/dsp/assets/placement-inspector.png)

## Information in the Placement [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** All of the sites on which the placement has had impressions.

   The [!UICONTROL Sites] tab includes search and filter features, the same standard and custom column view options that are available on the main page, and an [!UICONTROL Exclude] button in each row so you can quickly exclude a site from the placement.

* **[!UICONTROL Ads]:** All of the ads in the placement.

   The [!UICONTROL Ads] tab includes search and filter features, the same standard and custom column view options that are available on the main page, and quick action buttons in each row, such as [!UICONTROL View Ad Approvals].

* **[!UICONTROL Frequency]:** Data for each ad frequency level for the placement, including:
    * the ad frequency level (such as "1" for all instances in which users saw an ad one time)
    * the estimated unique number of devices/browsers or people (depending on the specified [!UICONTROL Cross Device Level] for the campaign) who received impressions at the specified frequency level
    * the estimated number of impressions at the specified frequency level
    * the estimated average frequency for the specified frequency level. This value is equal to (Estimated Impressions)/(Estimated Uniques).

* **[!UICONTROL Inventory]:** Information about all deals targeted by the placement.

    The [!UICONTROL Inventory] tab enables quick troubleshooting by showing performance statistics, such as [!UICONTROL Auctions], [!UICONTROL Bids], and [!UICONTROL Win Rate]. The tab includes search and filter features, the same standard and custom column view options that are available on the main page, and quick action buttons in each row, including [!UICONTROL Edit], [!UICONTROL View Report], and [[!UICONTROL Auction Insights] for further troubleshooting](/help/dsp/inventory/private-deal-auction-insights.md).

## Open the [!UICONTROL Placement Inspector] {#inspector-open}

1. Open the placements view for the parent campaign or package:

    * View all placements within the parent campaign:

        1. In the main menu, click **[!UICONTROL Campaigns]**.

        1. Click the name of the campaign.

        1. Click the **[!UICONTROL Placements]** tab.

    * View all placements within the parent package:

        1. In the main menu, click **[!UICONTROL Campaigns]**.

        1. Click the name of the campaign.

        1. Click the **[!UICONTROL Packages]** tab.

        1. Click the name of the parent package.

1. Hold the cursor over the placement row, click **[!UICONTROL ...]** > **[!UICONTROL Analyse]** > **[!UICONTROL Inspector]**.

1. (Optional) [Change the column view](campaign-data-views-manage.md#column-view-change) as needed to view the required metrics.

1. (Optional) To export the data on any tab, click ![More](/help/search-social-commerce/assets/more.png "More") in the upper right, and then click **[!UICONTROL Export]**.

   The data is saved to your browser's default download folder as a report in XLSM format.

## Remove an Ad from a Placement from the [!UICONTROL Placement Inspector] {#remove-ads-placement-inspector}

1. [Open the [!UICONTROL Placement Inspector]](#inspector-open).

1. Click the **[!UICONTROL Ads]** tab.

1. Next to the ad name, click  **[!UICONTROL ...]** > **[!UICONTROL Detach]**.

## Troubleshooting Inventory

| Issue | Possible Cause  | Actions to Take |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | The publisher hasn't started sending bid requests. | Contact the publisher to activate the deal. |
| | The deal was set up incorrectly, such as by entering an incorrect external deal ID. | Confirm the deal details and edit the deal. |
| [!UICONTROL Auctions but no Bids] | The placement targeting doesn't match the incoming bid requests for the deal. <br><br> For example, a placement might be targeting a geography that isn't eligible for the deal. | Edit the placement targets as needed to avoid targeting mismatches. |
| | The placement doesn't have an active ad with the required media type for the deal. | Create and attach an ad with the correct media type to the placement. |
| | The placement doesn't have adequate budget. | Increase the placement budget to allow bidding on incoming requests. |
| | The placement flight dates don't overlap with the impression delivery dates for the deal. | Edit the placement's flight dates as needed. |
| [!UICONTROL Low Win Rate] | The placement's maximum bid (floor or fixed) is below the minimum required by the deal. | Increase the placement's [!UICONTROL Max Bid] as needed. |
| | The placement uses pre-bid filters that limit bidding. | Lower the thresholds of the pre-bid filters to allow more bidding. |
| | Audience targeting for the placement is too restrictive. | Check if the specified audience targets have enough active users, and expand the audience if possible. |

>[!MORELIKETHIS]
>
>* [Types of Performance Reports in Campaign Management Views](campaign-reports-about.md)
>* [Manage Your Campaign Data Views](campaign-data-views-manage.md)
