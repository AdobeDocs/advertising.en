---
title: About insights
description: Learn about performance insights with visualizations.
feature: DSP Campaigns, DSP Packages, DSP Placements
exl-id: 0b7943c4-650c-4515-ae19-4417714ea7dd
---
# About insights

*Beta feature*

High-level performance insights with visualizations give you the information you need to efficiently optimize your campaigns and discover new opportunities to scale performance. You can view data across campaigns for a specified advertiser or drill down to a lower level.

Use performance insights to:

* Track long-term trends for strategic planning and informed decision making.

* Identify opportunities to achieve better outcomes.

* Improve efficiency by reducing the time between getting raw data and attaining actionable insights.

You can export all visualizations for a tab to a PDF file or download the data for a specific insight without visualizations in Microsoft Excel spreadsheet (XLSX) format.

You can also [change the date range, configure the view, and save a custom view](/help/dsp/campaign-management/reports/campaign-data-views-manage.md){target="_blank"} like you can for campaign management views.

## Types of insights

### [!UICONTROL Home] tab

The [!UICONTROL Home] tab provides key standard, performance, and viewability metrics across all of an advertiser's campaigns. By default, cross-placement data for a specific advertiser and custom goal is shown. You can optionally configure filters to show data for a different advertiser, a different custom goal, or a specific placement. <!-- I don't see campaigns or packages anymore:  You can optionally configure filters to show data for a different advertiser or data for only specific campaigns, packages, custom goals, and placements. --> The insights include:

* **[!UICONTROL Trends]:** A trend chart for three customer-specified metrics (by default, [!UICONTROL Net Spend], [!UICONTROL Impressions], and [!UICONTROL Net CPM]).

* **[!UICONTROL Delivery Breakdown]:** A breakdown of the data for specific metrics by three customer-specified dimensions, such as by campaign, publisher, and media type. For each dimensional breakdown, you can choose a different metric.

### [!UICONTROL Household Reach] tab

The [!UICONTROL Household Reach] tab provides household reach metrics across all of an advertiser's campaigns. By default, cross-campaign data is shown. You can optionally configure filters to show data for a different advertiser, for a specific campaign, across packages or placements, or for a specific package or placement. The insights include:

* **[!UICONTROL Trends]:** A trend chart by day or by week for three customer-specified metrics (by default, [!UICONTROL Net Spend], [!UICONTROL Unique Reach], and [!UICONTROL Net CPM]).

* **[!UICONTROL Incremental Household Reach]:** A donut chart showing the incremental household reach by [!UICONTROL Media Type], [!UICONTROL Device Type], or [!UICONTROL Inventory Type]. *Incremental household reach* is defined as a household reached exclusively through a single media, device, or inventory type.

* **[!UICONTROL Reach Breakdown]:** The incremental unique household reach vs. overlapping household reach by [!UICONTROL Media Type], [!UICONTROL Device Type], or [!UICONTROL Inventory Type].

  *Incremental household reach* is defined as a household reached exclusively through a single media, device, or inventory type. *Overlapping household reach* is defined as a household that's reached by multiple media, device, or inventory types.
  
* **[!UICONTROL Top Performers]:** The top-performing campaigns, placements, packages, publishers, sites/apps, media types, inventory types, or device types by [!UICONTROL Unique Reach], [!UICONTROL Net Spend], and [!UICONTROL Cost per Reach].

* **[!UICONTROL Performance Analysis]:** The [!UICONTROL Cost per Reach] and [!UICONTROL Net Spend] by package, publisher, or site/app. Use this insight to see which packages, publishers, or sites/apps show the potential for significant incremental reach.

  The size of each bubble indicates the incremental reach score, with larger bubbles indicating a higher incremental reach on average. To see the full entity name and key metrics for any bubble, hold the cursor over the bubble.

  The levels of impact include:

  * **High impact:** Consider increasing the budget.
  * **Moderate impact**
  * **Limited impact:** Needs attention

### [!UICONTROL Household Conversion] tab

The [!UICONTROL Household Conversion] tab provides household conversion metrics across all of an advertiser's campaigns<!-- active only? -->. By default, cross-campaign data for a specific advertiser and a specific conversion metric is shown. You can optionally configure filters to show data for a different advertiser or conversion metric, for a specific campaign, across packages or placements, or for a specific package or placement. The insights include:

* **[!UICONTROL Trends]:** A trend chart by day or by week for three customer-specified metrics (by default, [!UICONTROL Net Spend], [!UICONTROL Conversions], and [!UICONTROL Net CPM]).

* **[!UICONTROL Conversion Participation Overview]:** A bar chart showing which media types, inventory types, and device types result in most household conversions. 

  Impressions delivered within the lookback period (30 days) are considered valid for conversion participation.

* **[!UICONTROL Top Performers]:** A table of the campaigns, packages, placements, publishers, sites/apps, media types, and inventory types that drive performance for three customer-specified metrics (by default, [!UICONTROL Net Spend], [!UICONTROL CPA], and [!UICONTROL Conversions]). The top performer is listed first.

* **[!UICONTROL Performance Analysis]:** The [!UICONTROL CPA] and [!UICONTROL Net Spend] by package, publisher, or site/app. Use this insight to see which packages, publishers, or sites/apps show the potential for significant incremental reach.

  The size of each bubble indicates the incremental reach score, with larger bubbles indicating a higher incremental reach on average. To see the full entity name and key metrics for any bubble, hold the cursor over the bubble.

  The levels of impact include:

  * **High impact:** Consider increasing the budget.
  * **Moderate impact**
  * **Limited impact:** Needs attention

### [!UICONTROL Audience Analysis] tab

The [!UICONTROL Audience Analysis] tab provides granular, real-time insights into audience targeting effectiveness for your campaigns with CPA placements<!-- verify that caveat applies to both insights. Also, link the following effects to specific info in the charts -->. Use these insights to identify issues such as low match rates, drop-offs in eligibility, and missed opportunities caused by exclusions.

By default, data is shown for a specific advertiser and a specific placement. You can optionally configure filters to show data for a different advertiser or for a different placement.

The insights include:

* **[!UICONTROL Audience Segment Size Trends]:** A trend chart shows the daily number of unique users in the aggregated<!-- targetable? --> audience. Use this insight to track the volume and health of your target pool over time. To see the segment size for a specific point, hold the cursor over the point.

* **[!UICONTROL Audience Funnel Analysis]:**  A daily time-series table showing how your target audience narrows from the total available pool to actual impression wins after all targeting and eligibility filters are applied. Data is shown for yesterday. Metrics include:<!-- Verify the field names in the table and downloaded report, and explain all. -->

  * **[!UICONTROL Audience Size]:** The number of unique users in the aggregated audience.
  
  * **[!UICONTROL Cookies in Bid Stream]:** The number of cookies in the bid stream, including cookies for which the placement bid and didn't bid.

  * **[!UICONTROL Eligible Cookies]:** The number of cookies in the bid stream filtered by geo, then by device type, and then by operating system and browser.
  
  **[!UICONTROL Cookies bid on]:** The number of cookies for which the placement bid.

  * **[!UICONTROL Impression Wins]:** The number of cookies for which the placement won an impression.

## View performance insights

1. Open a set of insights:

   * (To open insights for all campaigns) In the main menu, click **[!UICONTROL Insights BETA]**.

   * (To open insights for a specific campaign, package, or placement) Next to the entity name in the [!UICONTROL Campaigns], [!UICONTROL Packages], or [!UICONTROL Placements] view, click **[!UICONTROL ...]** > **[!UICONTROL Insights]**.

   * (To open insights for a specific placement) Next to the entity name in the [!UICONTROL Campaigns], [!UICONTROL Packages], or [!UICONTROL Placements] view, click **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Insights]** .

1. (Optional) To view data for any point on the 

## Apply filters to a tab

1. In the toolbar at the top of the tab, click ![Filter button](/help/dsp/assets/filter.png).

1. In the left column, select a dimension, and then select one or more values in the right column, as applicable.

   You can select only one advertiser at a time.

1. Click **[!UICONTROL Apply]**.

1. (Optional) To narrow down the data further, select the dimension type in the toolbar, and then select a specific dimension (a single campaign, package, or placement).

1. ([!UICONTROL Audience Funnel Analysis] only; optional) To change the time increments between daily and weekly, select **[!UICONTROL Day]** or **[!UICONTROL Week]**.

## Change the dimension reported for an insight

* From the drop-down menu to the upper left of the insight, select the dimension.

## Change the metrics reported for an insight

*Available for some insights*

For conversion metrics, support is available for both Adobe Advertising-tracked and Adobe Analytics-tracked conversions.

1. To the upper right of the insight, click ![Metric settings](/help/dsp/assets/metric-settings.png "Metric settings").

1. Select the metrics, and then click **[!UICONTROL Apply]**.

## Export all visualizations for a tab to a PDF file

* In the upper right above the tab, click **[!UICONTROL ...]** > **[!UICONTROL Export]**.

  The file is saved to your browser's default Downloads folder.

## Download a specific insight to an XLSX file

* To the upper right of the insight, click ![Download](/help/creative/assets/download.png "Download").

  The file is saved to your browser's default Downloads folder.

<!-- Add:
## Save a custom view for a tab
-->

>[!MORELIKETHIS]
>
>* [About custom reports](/help/dsp/reports/report-about.md)
>* [Types of performance reports in campaign management views](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Available report columns](/help/dsp/reports/report-columns.md)
>* [Manage your campaign data views](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
