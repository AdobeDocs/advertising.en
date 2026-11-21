---
title: Filter data by date range
description: Learn how to use the global date range filter.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Filter data by date range

Use the date range filter to specify the period for which to show performance data. In views that support date comparison, you can also compare performance for two periods.

## (New UI) Change the date range {#date-filter-new-ui}

1. In the page header, click the date range control with the calendar icon.

1. Specify the date range:

   * To use a preset range, select an option from the menu above the first calendar, such as **[!UICONTROL Yesterday]** or **[!UICONTROL Last 7 Days]**.

   * To use a custom range, select **[!UICONTROL Custom Date Range]** and select the start and end dates in the calendar. Use the calendar arrows to navigate between months.

1. Click **[!UICONTROL Apply]**.

## (New UI) Compare data for two periods {#compare-periods-new-ui}

*Views that support date comparison only*

1. In the page header, click the date range control with the calendar icon.

1. Turn on **[!UICONTROL Compare Periods]**.

   Two calendar panels are shown side by side. The first period has a teal marker, and the comparison period has a purple marker.

1. In the first panel, specify the date range:

   * To use a preset range, select an option from the menu above the first calendar, such as **[!UICONTROL Yesterday]** or **[!UICONTROL Last 7 Days]**.

   * To use a custom range, select **[!UICONTROL Custom Date Range]** and select the start and end dates in the calendar. Use the calendar arrows to navigate between months.

1. In the second panel, select a comparison preset or click a starting date in the calendar.

   The comparison period has the same number of days as the first period. Review the complete date ranges above both calendars.

1. From **[!UICONTROL Comparison Format]**, select how to display the difference:

   * **[!UICONTROL As percentage]:** Show the difference as a percentage.

   * **[!UICONTROL As variance]:** Show the difference as a numeric value.

1. Click **[!UICONTROL Apply]**.

   The date range control shows both complete date ranges with their period labels and color markers. Each comparable metric is grouped into two period columns and a **[!UICONTROL Change]** column. Fields that aren't comparable remain single columns. The period markers in the column headings identify the corresponding date ranges.

To stop comparing periods, open the date range control, turn off **[!UICONTROL Compare Periods]**, and click **[!UICONTROL Apply]**. Turning off comparison clears filters based on comparison data.

### Change the comparison format from a column menu

1. With date comparison enabled, open the column heading menu for a **[!UICONTROL Change]** column or either period column for a comparable metric.

1. Select **[!UICONTROL As percentage]** or **[!UICONTROL As variance]**.

   The selection applies to all comparison metrics in the data table, not just the selected column. The date range control is synchronized with the selection, and the format is shared across applicable pages for the current advertiser, including views with saved date ranges.

   A confirmation message appears after the data table refreshes successfully. If the data table can't refresh with the selected format, an error message appears instead; try selecting the format again.

Sorting and filtering options remain available in column menus where supported.

## (Legacy UI) Date range settings

The same global date range filter is applied to most of your data views, across all of your advertisers, except for default and custom views for which you've saved specific date ranges. The system default date range for campaign management views is "Yesterday."

Your date range settings are saved to a browser-specific cookie, so any changes to the date range filter are used for all of your advertisers each time you sign in using the same browser application until you change the filter or delete the cookie. Each browser application you use stores date range filter settings in a different cookie.

When you save a specific date range for a default view or custom view, that range is applied whenever you apply the view, regardless of the browser application you are using. 

>[!NOTE]
>
>* You can view data for the previous 13 months, but any existing custom views can include data for only up to the previous 180 days.
>* To view earlier data, go to the [[!UICONTROL Reports] view](/help/search-social-commerce/legacy-ui/reports/management/basic-advanced/basic-advanced-report-about.md) and run a basic report.
>* You can also save a date range for a [default view or custom view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## (Legacy UI) Change the global date filter in campaign views

1. Above any data table in Search \> Campaigns \> Campaigns, click the current date range.

1. In the **[!UICONTROL Date Range]** field, specify the range:

   * For a preset range: Select from the list of common time increments, ranging from *[!UICONTROL Today]* to *[!UICONTROL Last 180 Days]*. The default is *[!UICONTROL Yesterday]*.

   * For a specific range: Select **[!UICONTROL Custom Date Range]** , and then specify the beginning date and the end date.

      Enter dates in the format MM/DD/YYYY or MM-DD-YYYY, or click ![Calendar icon](/help/search-social-commerce/assets/calendar.png "Calendar icon") next to each field to open the calendar and select a date.

1. (Optional) Compare data for the specified date range with data for a second date range:

   1. Move the **[!UICONTROL Comparison]** slider to the "on" position.

      When you select this option, two additional columns are added for each regular data column. For example, instead of including just one column for "[!UICONTROL Impressions]," the table includes columns for "[!UICONTROL Impressions R1]," "[!UICONTROL Impressions R2]," and "[!UICONTROL Impressions Diff]."  If you export the data, then the same columns are spelled out as "[!UICONTROL Impressions Range 1]," "[!UICONTROL Impressions Range 2]," and "[!UICONTROL Impressions Difference]."

   1. Specify the second date range.

   1. Choose how to express the difference between data in the two selected date ranges in the "\[_Data field_\] Difference" column:

      * *[!UICONTROL Variance]* (the default): Shows the difference as a numeric value.

      * *[!UICONTROL % Change]:*  Shows the difference as a percentage.

1. Click **[!UICONTROL Apply]**.
