---
title: About In-Platform Reports
description: Learn about the report data included in the campaign management views.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
---
# About In-Platform Reports

<!-- rename "About Performance Reports in Campaign Management Views?" -->
The campaign management views include comprehensive report data. The available reports help you to identify the packages and placements that are performing well and those that need your attention. Quick action buttons also make you more productive.

## All Campaigns View

The [!UICONTROL Campaigns] view opens to a set of performance data charts and a list of all campaigns within your account.

### Chart View {#chart-view}

You can [customize time series trend charts](campaign-data-visualization-manage.md) across all campaigns using three metrics. By default, data for [!UICONTROL Net Spend], [!UICONTROL Impressions], and [!UICONTROL Net CPM] are included in separate charts (trellis charts). You can optionally change the metrics. To enable hourly data in the time series trend charts, change your date selection to a single day ([!UICONTROL Today], [!UICONTROL Yesterday], or a specific day).  

![separate trend charts for three metrics](/help/dsp/assets/trend-chart-separate.png)

You also can optionally overlay the three metrics for easy detection of anomalies and areas in which to improve scale or performance.

![trend chart with overlay](/help/dsp/assets/trend-chart.png)

### Table View

![Campaigns list](/help/dsp/assets/campaigns-list.png)

By default, each campaign row includes pacing and delivery metrics. Pacing metrics include [!UICONTROL Gross Spend (Lifetime)], which includes a gauge of the actual on-target spend versus the expected on-target spend across all packages in the campaign, so you can identify under-performing campaigns at a glance. You can optionally [change the column view](column-view-change.md) or even [create a custom column view](column-view-create.md).

You can further [customize the data tables](campaign-data-views-about.md) in additional ways and [filter the visible data](campaign-data-filter.md).

To view a campaign in more detail, click the campaign name.

## Single Campaign Reporting {#single-campaign-reporting}

Within a campaign, you can filter data based on the campaign entity: [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads]. You can further [filter the visible data](campaign-data-filter.md) to include only the packages, placements, or ads that you want to see.

![Campaign entity tabs](/help/dsp/assets/campaign-subtabs.png)

### Chart View

For each campaign, you can [customize time series trend charts](campaign-data-visualization-manage.md) with three metrics, which are available in each entity view. The same metrics are persisted across all trend charts for the campaign.

See the ["Chart View" section on cross-campaign metrics](#chart-view) for more information.

### Table View

In each entity tab, each row includes pacing and delivery metrics, by default, but you can [change the column view](column-view-change.md) or even [create a custom column view](column-view-create.md) to apply across all subtabs for the campaign. You can further [customize the data tables](campaign-data-views-about.md) in additional ways. Each data table includes a [!UICONTROL Subtotals] row, which shows either the sum or the average value of each metric across all visible rows.

### Placement [!UICONTROL Inspector] {#placement-inspector}

For each placement, you can [open a (detail view [!UICONTROL Inspector])](placement-details-view.md), which includes the following in-depth data:

* **[!UICONTROL Sites]:** All of the sites on which the placement has had impressions.

   The [!UICONTROL Sites] tab includes search and filter features, the same standard and custom column view options that are available on the main page, and an [!UICONTROL Exclude] button in each row so you can quickly exclude a site from the placement.

* **[!UICONTROL Ads]:** All of the ads in the placement.

   The [!UICONTROL Ads] tab includes search and filter features, the same standard and custom column view options that are available on the main page, and quick action buttons in each row, such as [!UICONTROL Pause] (so you can quickly pause an ad).

* **[!UICONTROL Frequency]:** Data for each ad frequency level for the placement, including:
    * the ad frequency level (such as "1" for all instances in which users saw an ad one time)
    * the estimated unique number of devices/browsers or people (depending on the specified [!UICONTROL Cross Device Level] for the campaign) who received impressions at the specified frequency level
    * the estimated number of impressions at the specified frequency level
    * the estimated average frequency for the specified frequency level. This value is equal to (Estimated Impressions)/(Estimated Uniques).

* **[!UICONTROL Inventory]:** Information about all deals targeted by the placement.

    The [!UICONTROL Inventory] tab enables quick troubleshooting by showing performance statistics, such as [!UICONTROL Auctions], [!UICONTROL Bids], and [!UICONTROL Win Rate]. The tab includes search and filter features, the same standard and custom column view options that are available on the main page, and quick action buttons in each row, including [!UICONTROL Edit], [!UICONTROL View Report], and [[!UICONTROL Auction Insights] for further troubleshooting](/help/dsp/inventory/private-deal-auction-insights.md). 

#### Troubleshooting Inventory

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

![placement Inspector](/help/dsp/assets/placement-inspector.png)

You can export the data on the [!UICONTROL Sites], [!UICONTROL Ads], or [!UICONTROL Frequency] tab to your browser's default download folder as a report in XLSM format.

### Other Types of Campaign-level Reporting

For other data breakouts, view [the campaign-level reporting pages](/help/dsp/campaign-management/campaigns/campaign-view-report.md). The <!--legacy --> report includes sections on [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], and [!UICONTROL Audience Performance] data.

>[!MORELIKETHIS]
>
>* [View the Sites, Ads, and Frequency Details for a Placement](placement-details-view.md)
>* [About the Campaign Data Views](campaign-data-views-about.md)
>* [Create a Custom Column View](column-view-create.md)
>* [Change the Column View](column-view-change.md)
>* [Manage Data Visualizations](campaign-data-visualization-manage.md)
>* [Export Data from a Campaign Management View](campaign-export-data.md)
>* [View a Detailed Report for a Campaign](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
