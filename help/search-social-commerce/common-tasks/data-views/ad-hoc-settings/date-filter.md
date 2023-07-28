---
title: Filter data by date range
description: Learn how to use the global date range filter.
exl-id: e67e843a-1a73-4ab1-9ef7-c97afeb999f6
feature: Search Common Tasks, Search Custom Data Views
---
# Filter data by date range

The same global date range filter is applied to most of your campaign data views, across all of your advertisers, except for default and custom views for which you've saved specific date ranges. The system default date range for campaign management views is "Yesterday."

Your date range settings are saved to a browser-specific cookie, so any changes to the date range filter are used for all of your advertisers each time you log in using the same browser application until you change the filter or delete the cookie. Each browser application you use will store date range filter settings in a different cookie.

When you save a specific date range for a default view or custom view, that range is applied whenever you apply the view, regardless of the browser application you are using. 

>[!NOTE]
>
>* You can view data for the previous 13 months, but any existing custom views can include data for only up to the previous 180 days.
>* To view earlier data, go to the [[!UICONTROL Reports] view](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) and run a basic report.
>* You can also save a date range for a [default view or custom view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Change the global date filter in campaign views

1. Above any data table in Search \> Campaigns \> Campaigns, click the current date range.

1. In the **[!UICONTROL Date Range]** field, specify the range:

   * For a preset range: Select from the list of common time increments, ranging from *[!UICONTROL Today]* to *[!UICONTROL Last 180 Days]*. The default is *[!UICONTROL Yesterday]*.

   * For a specific range: Select **[!UICONTROL Custom Date Range]** , and then specify the beginning date and the end date.

      Enter dates in the format MM/DD/YYYY or MM-DD-YYYY, or click ![Calendar icon](/help/search-social-commerce/assets/calendar.png "Calendar icon") next to each field to open the calendar and select a date.

1. (Optional) Compare data for the specified date range with data for a second date range:

   1. Move the **[!UICONTROL Comparison]** slider to *[!UICONTROL On]*.

      When you select this option, two additional columns are added for each regular data column. For example, instead of including just one column for "[!UICONTROL Impressions]," the table includes columns for "[!UICONTROL Impressions R1]," "[!UICONTROL Impressions R2]," and "[!UICONTROL Impressions Diff]."  If you export the data, then the same columns are spelled out as "[!UICONTROL Impressions Range 1]," "[!UICONTROL Impressions Range 2]," and "[!UICONTROL Impressions Difference]."

   1. Specify the second date range.

   1. Choose how to express the difference between data in the two selected date ranges in the "\[_Data field_\] Difference" column:

      * *[!UICONTROL Variance]* (the default): Shows the difference as a numeric value.

      * *[!UICONTROL % Change]:*  Shows the difference as a percentage.

1. Click **[!UICONTROL Apply]**.
