---
title: About Performance Reports in Campaign Management Views
description: Learn about the report data included in the campaign management views.
feature: DSP Campaign Data Views
exl-id: 7af97704-2053-4862-a851-12db009e6776
---
# About Performance Reports in Campaign Management Views

The campaign management views include comprehensive report data. The available reports help you to identify the packages and placements that are performing well and those that need your attention. Quick action buttons also make you more productive.

## All Campaigns View

The [!UICONTROL Campaigns] view opens to a set of performance data charts and a list of all campaigns within your account.

### Chart View {#chart-view}

You can [customize time series trend charts](campaign-data-views-manage.md#data-visualizations-manage) across all campaigns using three metrics. By default, data for [!UICONTROL Net Spend], [!UICONTROL Impressions], and [!UICONTROL Net CPM] are included in separate charts (trellis charts). You can optionally change the metrics. To enable hourly data in the time series trend charts, change your date selection to a single day ([!UICONTROL Today], [!UICONTROL Yesterday], or a specific day).  

![separate trend charts for three metrics](/help/dsp/assets/trend-chart-separate.png)

You also can optionally overlay the three metrics for easy detection of anomalies and areas in which to improve scale or performance.

![trend chart with overlay](/help/dsp/assets/trend-chart.png)

### Table View

![Campaigns list](/help/dsp/assets/campaigns-list.png)

By default, each campaign row includes pacing and delivery metrics. Pacing metrics include [!UICONTROL Gross Spend (Lifetime)], which includes a gauge of the actual on-target spend versus the expected on-target spend across all packages in the campaign, so you can identify under-performing campaigns at a glance. You can optionally [change the column view](campaign-data-views-manage.md#column-view-change) or even [create a custom column view](campaign-data-views-manage.md#column-view-create).

You can further [customize the data tables](campaign-data-views-manage.md#data-tables-manage) in additional ways and [filter the visible data](campaign-data-views-manage.md#filter-data-tables).

<!--
An "Alerts" column indicates when a campaign (or any child entity under it) has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

To view a campaign in more detail, click the campaign name.

## Single Campaign Reporting {#single-campaign-reporting}

Within a campaign, you can filter data based on the campaign entity: [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads]. You can further [filter the visible data](campaign-data-views-manage.md#filter-data-tables) to include only the packages, placements, or ads that you want to see.

![Campaign entity tabs](/help/dsp/assets/campaign-subtabs.png)

### Chart View

For each campaign, you can [customize time series trend charts](campaign-data-views-manage.md#data-visualizations-manage) with three metrics, which are available in each entity view. The same metrics are persisted across all trend charts for the campaign.

See the ["Chart View" section on cross-campaign metrics](#chart-view) for more information.

### Table View

In each entity tab, each row includes pacing and delivery metrics, by default, but you can [change the column view](campaign-data-views-manage.md#column-view-change) or even [create a custom column view](campaign-data-views-manage.md#column-view-create) to apply across all subtabs for the campaign. You can further [customize the data tables](campaign-data-views-manage.md#data-tables-manage) in additional ways. Each data table includes a [!UICONTROL Subtotals] row, which shows either the sum or the average value of each metric across all visible rows.

<!--
An "Alerts" column indicates when a package, placement, or ad &mdash; or any child entity under a package or placement &mdash; has an issue. Alert indicators include "Critical" (![Critical](/help/dsp/assets/indicator-critical.png "Critical")) and "Warning" (![Warning](/help/dsp/assets/indicator-warning.png "Warning")). See "[View Alerts and Notifications](campaign-alerts.md) for more information.
-->

### Other Types of Campaign-level Reporting

For other data breakouts, view [the campaign-level reporting pages](/help/dsp/campaign-management/campaigns/campaign-view-report.md). The report includes sections on [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], and [!UICONTROL Audience Performance] data.

### Other Types of Placement-level Reporting

For other data breakouts, view [the placement-level reporting pages](/help/dsp/campaign-management/placements/placement-view-report.md). The report includes sections on [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability], [!UICONTROL Audience Performance], [!UICONTROL Notifications], and [!UICONTROL Ads] data.

In addition, you can view the following data within the placement settings:

* [A (detail view [!UICONTROL Inspector])](placement-details-view.md), which shows all targeted sites, ads, frequency data, and deals for a placement.

* A [placement forecast report](/help/dsp/campaign-management/reports/placement-forecast.md)
 
* [Placement diagnostic reports](/help/dsp/campaign-management/reports/placement-diagnostics.md).


### Other Types of Ad-level Reporting

For other data breakouts, view [the ad-level reporting pages](/help/dsp/campaign-management/ads/ad-view-report.md). The report includes [!UICONTROL Overview], [!UICONTROL Geography], and [!UICONTROL Viewability] data.

>[!MORELIKETHIS]
>
>* [View the Sites, Ads, and Frequency Details for a Placement](placement-details-view.md)
>* [Manage Your Campaign Data Views](campaign-data-views-manage.md)
>* [Export Data from a Campaign Management View](campaign-export-data.md)
>* [View a Detailed Report for a Campaign](/help/dsp/campaign-management/campaigns/campaign-view-report.md)
