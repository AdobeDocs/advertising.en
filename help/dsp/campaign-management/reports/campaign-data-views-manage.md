---
title: Manage the Campaign Data Views
description: Learn how you can customize the data views for campaigns, packages, placements, and ads.
feature: DSP Campaign Data Views
-->
---

# Manage the Campaign Data Views

You can customize the data that appears within your campaign management views ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads]).

## Manage Data Visualizations

You can change the metrics and chart mode for all data visualizations across campaigns or for a single campaign. Changes to a single campaign are applied across all data visualizations for the campaign, including those in the [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads] views.

### Change the Metrics for a Data Visualization

1. In the upper right of the data visualization, click ![Settings](/help/dsp/assets/settings-chart.png).

1. Select the metrics.

   You can't select the same metric twice.

1. Click **[!UICONTROL Apply]**.

### Change the Display Mode for a Data Visualization

* In the upper right of the data visualization, click the [!UICONTROL Overlay] switch (![Overlay switch](/help/dsp/assets/overlay.png)) to change between overlay mode (all charts overlaid together) and trellis chart mode (three separate charts).

## Manage Data Tables

In all campaign management views ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads]), you can customize the data that appears within the data table.

### Manage Column Views

Each campaign management level ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements], and [!UICONTROL Ads]) includes built-in [!UICONTROL Pacing] and [!UICONTROL Performance] views that include relevant metrics for that entity. By default, the [!UICONTROL Pacing] view is shown so that you can identify under-performing campaigns and campaign components at a glance. You can optionally create and edit custom column sets.

![column view selector](/help/dsp/assets/column-view-selector.png)

DSP saves your most recent view as the default view so that, every time you return to the page, you always view the metrics that are pertinent to you.

#### Change the Column View {#column-view-change}

* In the View selector, click ![down arrow](/help/dsp/assets/chevron-down.png), and then click the name of the desired column view.

#### Create a Custom Column View {#column-view-create}

1. In the View selector, click ![down arrow](/help/dsp/assets/chevron-down.png), and then click **[!UICONTROL Create View]**.

1. Specify the metrics to include in the view:

    1. In the list of available metrics, select the check box next to each metric to include.

       All metrics are alphabetical by category: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (standard metrics that DSP tracks), [!UICONTROL Viewability], and [!UICONTROL Conversions]. Metrics appended with "([!UICONTROL Lifetime])" return values from the start of the campaign, regardless of the date range selected on the page.

    1. Edit the column order, as needed, by clicking column names in the right panel and dragging them to the required positions.

   Some columns have fixed positions and can't be moved or removed.

1. Apply or save the settings:

    * To apply the settings temporarily without saving them to the view, click **[!UICONTROL Apply].**

    * To save the settings to a new, custom column view, click **[!UICONTROL Save As]**. In the [!UICONTROL Save View] window, enter the name of the new view, and then click **[!UICONTROL Save]**.

#### Edit a Column View {#column-view-edit}

>[!NOTE]
>
>You can't save changes to a standard (pre-defined) column view but can apply your changes temporarily or save them to a new custom view.

1. In the View selector, click ![down arrow](/help/dsp/assets/chevron-down.png), and then click the existing column view name.

1. In the View selector, click ![down arrow](/help/dsp/assets/chevron-down.png), and then click **[!UICONTROL Edit View]**.

1. Edit the metrics to include in the view:

    1. In the list of available metrics, select the check box next to each metric to include, and clear the check box next to each metric to exclude.

       All metrics are alphabetical by category: [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (standard metrics that DSP tracks), [!UICONTROL Viewability], and [!UICONTROL Conversions]. Metrics appended with "([!UICONTROL Lifetime])" return values from the start of the campaign, regardless of the date range selected on the page.

    1. Edit the column order, as needed, by clicking column names in the right panel and dragging them to the required positions.

   Some columns have fixed positions and can't be moved or removed.

1. Apply or save the settings:

    * (Custom views only) To save the settings, click **[!UICONTROL Save]**.
        
    * To apply the settings temporarily without saving them to the view, click **[!UICONTROL Apply].**

    * To save the settings to a new, custom column view, click **[!UICONTROL Save As]**. In the [!UICONTROL Save View] window, enter the name of the new view, and then click **[!UICONTROL Save]**.

### Filter Campaign Data

Filters change the data that is displayed on the current tab. Available filters vary by entity type but may include entity name, status, and additional property columns.

1. In the main toolbar, click ![Filter button](/help/dsp/assets/filter.png).
1. For each filter you want to apply, click the filter name in the left column, and then specify the filter value(s).
1. Click **[!UICONTROL Apply]**.

#### Available Filters

The following filters are available for your [!UICONTROL Campaigns], [!UICONTROL Packages], and [!UICONTROL Placements] views:

* [!UICONTROL Campaigns] view filters:
    * [!UICONTROL Campaign status]
    * [!UICONTROL Advertiser]
* [!UICONTROL Packages] view filters:
    * [!UICONTROL Custom flights] (whether or not they exist)
    * [!UICONTROL Custom goal] (if applicable)
    * [!UICONTROL End end date]
    * [!UICONTROL Optimization goal]
    * [!UICONTROL Flight pacing]
    * [!UICONTROL Intraday pacing]
    * [!UICONTROL Package status]
    * [!UICONTROL Start date]
* [!UICONTROL Placements] view filters:
    * [!UICONTROL Custom ad scheduling]
    * [!UICONTROL Custom goal] (if applicable)
    * [!UICONTROL End date]
    * [!UICONTROL Max bid] ([!UICONTROL less than], [!UICONTROL greater than], or [!UICONTROL equal to] a specified value)
    * [!UICONTROL Optimization goal]
    * [!UICONTROL Pacing on] ([!UICONTROL impressions] or [!UICONTROL spend])
    * [!UICONTROL Flight pacing]
    * [!UICONTROL Intraday pacing]
    * [!UICONTROL Package]
    * [!UICONTROL Placement status]
    * [!UICONTROL Placement type]
    * [!UICONTROL Placement sub-type]
    * [!UICONTROL Start date]
    * [!UICONTROL Creation date]
* [!UICONTROL Ads] view filters:
    * [!UICONTROL Adobe ad approval status]
    * [!UICONTROL Ad ID]
    * [!UICONTROL Ad name]
    * [!UICONTROL Ad type]   
    * [!UICONTROL Creation date]


### Change the Date Range

Change the date range used in all standard and custom views using the date range selector above any data table.

![Date range selector](/help/dsp/assets/date-range-selector.png "Date range selector")

* For a preset range: Select from the list of common time increments. The default is [!UICONTROL Last 30 days]*.

* For a specific range, do either of the following:

  * Click ![Calendar](/help/dsp/assets/calendar.png "Calendar"), and then click the beginning date and the end date within the calendar.

  * Click within the date range, and then either enter a beginning date and end date or select them within the calendar.

    You can enter numeric values (from M-D-YY to MM-DD-YYYY) and/or month names or abbreviations (such as Jan or January).

### Sort a Data Column

You can sort any data column in ascending order (A to Z, or 1 to 10) or descending order (Z to A, or 10 to 1).

* Click the column header to switch between ascending order and descending order.


### Specify the Number of Data Rows

On the bottom right of any page, next to **[!UICONTROL Items per page]** , select *[!UICONTROL 25]*, *[!UICONTROL 50]*, or *[!UICONTROL 100]*.

>[!MORELIKETHIS]
>
>* [About In-Platform Reports](campaign-reports-about.md)
>* [Manage Data Visualizations](/help/dsp/campaign-management/reports/campaign-data-visualization-manage.md)
>* [Change the Column View](column-view-change.md)
>* [Create a Custom Column View](column-view-create.md)
>* [Edit a Custom Column View](/help/dsp/campaign-management/reports/column-view-edit.md)
>* [Filter Campaign Data](campaign-data-filter.md)
>* [Sort a Data Column](campaign-data-sort.md)
>* [View the Sites, Ads, and Frequency Details for a Placement](placement-details-view.md)
>* [View the Placement Forecast Report](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [View the Placement Diagnostic Reports](placement-diagnostics.md)
>* [Export Data from a Campaign Management View](campaign-export-data.md)
>* [Video: DSP Account Structure and User Interface](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
