---
title: Manage default and custom views
description: Learn how to customize your default views and custom views.
exl-id: 1f240760-6186-471f-bf1a-3e0ee13ce550
feature: Search Common Tasks, Search Custom Data Views
---
# Manage default and custom views

Your default views and custom views allow you to customize the performance data that is displayed within the search campaign data views. View settings include the columns to include, filters, date range, conversion attribution settings, and other advanced settings &mdash; and you can either apply the settings temporarily or save them. (Exception: You can't save filters for default views.) Each default and regular custom view is applicable for a specific entity view (such as [!UICONTROL Campaigns]) and specific advertiser account only. Each universal custom view is applicable across entity views for a specific advertiser and therefore can't include property columns (such as entity name or status), which vary by entity type.

Default views are displayed by default each time you log in. You can create additional custom views and apply them anytime. You optionally can share any custom view you create with all other users who can view the advertiser's data. In your view lists, each view that another person is sharing is italicized, such as "*Top-performing Campaigns*." Only the person who creates a custom view can delete it.

Each view is available as a shortcut in the [!UICONTROL Custom Views] section of the left panel.

## Apply a default or custom view

* (Default views) In the main menu, click **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live]** \> **\[entity type\]**.

* (Custom views) From the left navigation panel:

  1. In the left panel, click the **[!UICONTROL Custom Views]** menu to expand it.

     Views are sorted by applicable entity.

  1. Expand the available menus.

     "[!UICONTROL Universal Views]" includes custom views that can be used across all entity views. All other custom views are grouped by entity type.

  1. Click the view name.

     If the view is universal or applies to the current entity, then the data table is re-displayed according to the view configuration. If the view applies to a different entity, then data for the applicable entity is displayed according to the view configuration.

## Create a custom view {#create-custom-view}

Custom views are applicable to the campaign management views only.

>[!NOTE]
>
>In addition to the view settings that you specify for the custom view, the current column sort order is also saved.

1. On the right side of the toolbar above the data table, click the name of the current view (which might be "[!UICONTROL Default]").

1. Specify the [custom view settings](#view-settings):

   1. (Optional) To make the data settings available across all entity views (for [!UICONTROL Campaigns], [!UICONTROL Ads], and so on), select **[!UICONTROL Universal View]**. 
    
      Once you enable or disable this option, you can't save the change to the existing view but can create a new view with the change.
   
   1. (Optional) To make the view available to all other users who can view the advertiser's data, move the **[!UICONTROL Shared]** slider to *[!UICONTROL Yes]*.

   1. (Optional) On the **[!UICONTROL Columns]** tab, change the columns available for the tab, their order, and how to sort the rows.

   1. (Optional) Click the **[!UICONTROL Filters]** tab, and then specify any filters to apply.

      Applying filters returns rows only when the value for a metric meets specified criteria, whether or not the metric is included as a column in the report.

   1. (Optional) Click the **[!UICONTROL Date]** tab, and change the default date settings.

   1. (Optional) Click the **[!UICONTROL Additional Settings]** tab, and change the settings.

1. Click **[!UICONTROL Save as New]**.

1. Enter the name of the new view, and then click **[!UICONTROL Save]**.

   >[!TIP]
   >
   >Use a name that helps you identify the tab and the information to which it applies (such as "Paused Campaigns" or "Top 50 Ads").

### Edit a default or custom view

1. Open the view settings:

   * (If you've already applied the view) On the right side of the toolbar above the data table, click the name of the current view (which might be "[!UICONTROL Default]").

   * (Custom views that aren't applied) In the left panel, click ![Custom Views](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Custom Views") to expand the [!UICONTROL Custom Views] menu. Click the custom view name.

1. Edit the [view settings](#view-settings):

   1. (Optional) To enable or disable the data settings across all search entity views (for [!UICONTROL Campaigns], [!UICONTROL Ad Groups], and so on), select or deselect **[!UICONTROL Universal View]**.  
   
      You can't save the change to the existing view but can create a new view with the change.

   1. (Optional; custom views that you created only) If the view isn't already public, make it available to all other users who can view the advertiser's data by moving the **[!UICONTROL Shared]** slider to *[!UICONTROL Yes]*.

   1. (Optional) On the **[!UICONTROL Columns]** tab, change the columns available for the tab, their order, and how to sort the rows.

   1. (Optional) Click the **[!UICONTROL Filters]** tab, and then edit the filters to apply.

      Applying filters returns rows only when the value for a metric meets specified criteria, whether or not the metric is included as a column in the report.

      >[!NOTE]
      >
      >You can apply but not save changes to filters to your default view settings.

   1. (Optional) Click the **[!UICONTROL Date]** tab and change the default date settings.

   1. (Optional) Click the **[!UICONTROL Additional Settings]** tab and change the settings.

1. Apply or save the settings:

   * To apply the settings temporarily without saving them to the view, click **[!UICONTROL Apply]**.

     The settings are applied to the tab until you move away from the top-level management view or (when applicable) [view data for another advertiser](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * (For default views and custom views that you created) To save the settings to the current view, click **[!UICONTROL Save]**.

   * To save the settings to a new, custom view, click **[!UICONTROL Save As]**. In the [!UICONTROL Enter New Custom View Name] window, enter the name of the new view, and then click **[!UICONTROL Save]**.

## Reset a default view to the system default settings

Restoring the default view settings removes all settings you have saved and reapplies the system default settings.

The system default settings vary by tab. For most tabs, the system default view shows data for the previous day for items in enabled accounts and that are active (for example, only active ad groups in active campaigns), with the data sorted by cost, and with conversion data based on transaction date.

1. In the left panel, click ![Custom Views](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Custom Views") to expand the [!UICONTROL Custom Views] menu.

   Views are sorted by applicable entity.

1. Next to the view name, click ![Restore to default settings](/help/search-social-commerce/assets/restore.png "Restore to default settings").

## Delete a custom view

You can delete any custom view that you created.

If you delete a custom view that's applied to the current tab, the tab continues to show the custom view until you move outside of the view set (for example, from views within the [!UICONTROL Search] menu to the [!UICONTROL Reports] menu) or (when applicable) when you [view data for another advertiser](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. In the left panel, click ![Custom Views](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "Custom Views") to expand the [!UICONTROL Custom Views] menu.

1. Hold the cursor over the custom view name, and then click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").

1. In the confirmation message, click **[!UICONTROL Continue]**.

## Default and custom view settings {#view-settings}

| **Tab** | **Field** | **Description** |
| --- | --- | --- |
| [Above all tabs] | Name | A unique name for the view. You can't edit the name of a default view.<p><b>Tip:</b> Use a name that helps you identify the tab and the information to which it applies (such as "Paused Campaigns" or "Top 50 Ads"). |
|   | Universal View | Makes the data settings available across all entity views (for Campaigns, Ads, and so on). Universal views can include metric and label classification columns &mdash; but not property columns (such as entity name and status) because they differ by entity type &mdash; as well as all other view attributes. Any filter criteria are applied to the entity view when applicable and are ignored otherwise. All metric filters are evaluated locally (for example, for clicks \> 1000, the Campaigns views show campaigns with more than 1000 clicks, and the Ad Groups view shows ad groups with more than 1000 clicks).<p>The property columns for a universal view are pulled from the entity's default view. You can change the default property columns for a specific entity in the default view settings.<p>Once you enable or disable this option, you can't save the change to the existing view but can create a new view with the change. |
|   | Share | (Custom views only; optional) Makes the view available to all other users who can view the advertiser's data. Other users can't edit or delete the view, but they can create a new view from the settings. In your view lists, each view that another person is sharing is italicized, such as "_Top-performing Campaigns_." |
| Columns | Selected Columns & Ordering | The columns of data that are displayed, and their order:<ul><li> (To add a column) In the Available Columns list, click a column name, and then either drag it into the Selected Columns & Ordering list or click ![right arrow](/help/search-social-commerce/assets/chevron-right.png) to move it there.</li><li>(To change the horizontal position of a column) In the Selected Columns & Ordering list, click the column name, and then either drag it to the desired position or click ![up arrow](/help/search-social-commerce/assets/chevron-up.png) or ![down arrow](/help/search-social-commerce/assets/chevron-down.png) to move it there. The top column name appears in the left column.</li><li>(To remove a column) In the Selected Columns & Ordering list, click a column name, and then either drag it into the Available Columns list or click ![left arrow](/help/search-social-commerce/assets/chevron-left.png) to move it there.</li></ul><b>Filter data</b><p>To list only a specific type of data, click any of the icons beside the list:<ul><li>![properties icon](/help/search-social-commerce/assets/properties-icon.png) for property names and IDs for search components, such as Status</li><li>![traffic icon](/help/search-social-commerce/assets/traffic-metrics-icon.png) for standard traffic metrics, such as impressions and clicks</li><li>![revenue icon](/help/search-social-commerce/assets/revenue-metrics-icon.png) (for conversion metrics tracked for the advertiser, including conversion and site engagement metrics synced from Analytics)</li><li>![custom icon](/help/search-social-commerce/assets/custom-metrics-icon.png) (for custom derived metrics created by the advertiser)</li><li>![classification icon](/help/search-social-commerce/assets/classifications-icon.png) (for label classifications).</li></ul> <b>Additional notes:</b><ul><li>To add, create, or edit new metrics, see "Create a Custom Metric," "Edit a Custom Metric," and "Delete a Custom Metric."</li><li>If the report includes data for accounts with different currencies, then totals aren't included for monetary-based columns (such as Cost and CPC).</li><li>You can [temporarily edit the column set from the column heading menu](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md), and [edit and sort the column set from the [!UICONTROL Columns] icon](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![Columns icon](/help/search-social-commerce/assets/custom-columns.png "Columns icon")).</li></ul> |
|   | Sort By | The column by which to sort the data. The default value is different for each report type. |
|   | Sort Order | Whether to sort the data in **Ascending** or **Descending** order. Move the slider to select an option. |
| Filters | [Filter definitions] | (Optional) Filters to apply to data. Applying filters returns rows only when the value for a column meets specified criteria.<p>For each filter to apply:<ol><li>In the Add Filter menu, select a column name. The list includes all available columns and is sorted by column type, with property columns first.</li><li>Define the filter on the column</li></ol>(Filters with input fields) Select an operator from the second menu, and then enter the applicable value. Values aren't case-sensitive. Click ![check icon](/help/search-social-commerce/assets/select.png) when you're done.<p>For example, if you've selected the "Clicks" column and want to return only rows with more than 100 clicks, then select _\>_ and enter `100` in the input field.<p>Depending on the data type, available operators may include <i>greater than</i>, <i>less than</i>, <i>equals</i>, <i>contains</i>, <i>doesn't contain</i>, <i>starts with</i>, <i>ends with</i>,<i>no value</i>, or <i>has value</i> <i>before</i>, <i>after</i>,or <i>no date</i>.<p>(Filters without input fields) Click ![arrow down](/help/search-social-commerce/assets/arrow-down-expand.png) next to the Select list items menu, and then select the check boxes next to each value to include. Click ![check icon](/help/search-social-commerce/assets/select.png) when you're done.<p><b>Notes:</b><ul><li>You can apply but not save changes to filters to your default view settings.</li><li>You also can [temporarily change the applicable filters](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) within the view.</li></ul> |
|   | Include rows with performance data only | (Ad Groups, Keyword, Product Groups, Placements, and Auto Targets views only) <p>Includes only rows with performance data during the specified dates. By default, this option is selected to reduce the page load time. <p><b>Warning</b>: If you de-select the option and the view includes many entities without performance data, the data takes longer to be displayed.<p> <b>Note</b>: You can apply but not save changes to filters to your default view settings. Default views always show only entities with performance data. |
| Date | Date Range | (When "Include date range is selected)<p>The date range for which to generate data. Choose one option:<ul><li><i>[Preset range]</i>: A list of common time increments, ranging from <i>Today</i> to <i>Last 180 Days</i>. Choose one from the list; the default is <i>Yesterday</i>. Note: <i>Last Month</i>, <i>Last 3 Months</i>, and <i>Last 6 Months</i> show data for the previous calendar months.</li><li><i>Custom Date Range:</i> Specify the start date and end date. Enter dates in the format MM/DD/YYYY or M/D/YYYY, or click ![calendar icon](/help/search-social-commerce/assets/calendar.png) next to a field and select a date.</li></ul> |
|   | Comparison | Compares data for the specified date range with data for a second date range. When you select this option, two additional columns are added for each regular data column. For example, instead of including just one column for "Impressions," the report includes columns for "Impressions Range 1," "Impressions Range 2," and "Impressions Difference."<p><b>Notes:</b><ul><li>The difference column isn't shown for derived metrics.</li><li>Reports that compare large date ranges may take longer to generate.</li></ul> |
|   | Comparison Format | How to express the difference between data in the two selected date ranges in the "[_Data field_] Difference" column. Choose one option:<ul><li><i>Variance</i> (the default): Shows the difference as a numeric value.</li><li><i>% Change</i>: Shows the difference as a percentage.</li></ul>|
| Additional Settings | Use Default | Applies the attribution settings specified in the advertiser-level conversion attribution settings. |
|   | Attribution Rule | (Advertisers with the Adobe Advertising pixel-based conversion tracking service only) Within the tab, how to attribute conversion data &mdash; potentially across multiple ad channels and portfolios &mdash; in a series of events that lead to a conversion. By default, the rule specified in the advertiser-level conversion attribution settings is selected.<ul><li> <i>First Event</i>: Attributes the conversion to the first paid click in the series within the advertiser's click lookback window or, if no paid clicks occurred, to the last impression within the advertiser's impression lookback window.</li><li><i>Weight First Event More</i>: Attributes the conversion to all events in the series that occurred within the advertiser's click lookback window and impression lookback window, but gives the most weight to the first event and successively less weight to the following events. When the conversion is preceded by both paid clicks and impressions, the specified impression override weight is further applied to the impressions. When the conversion is preceded only by impressions, the impressions are weighted according to the advertiser's view-through weight rather than to the impression override weight.</li><li><i>Even Distribution</i>: Attributes the conversion equally to each event in the series that occurred within the advertiser's click lookback window and impression lookback window. When the conversion is preceded by both paid clicks and impressions, the specified impression override weight is further applied to the impressions. When the conversion is preceded only by impressions, the impressions are weighted according to the advertiser's view-through weight rather than to the impression override weight.</li><li><i>Weight Last Event More</i>: Attributes the conversion to all events in the series that occurred within the advertiser's click lookback window and impression lookback window, but gives the most weight to the last event and successively less weight to the preceding events. When the conversion is preceded by both paid clicks and impressions, the specified impression override weight is further applied to the impressions. When the conversion is preceded only by impressions, the impressions are weighted according to the advertiser's view-through weight rather than to the impression override weight.</li><li><i>Last Event</i> (the default): Attributes the conversion to the last paid click in the series within the advertiser's click lookback window or, if no paid clicks occurred, to the last impression within the advertiser's impression lookback window.</li><li><i>U-shaped</i>: Attributes the conversion to all events in the series that occurred within the advertiser's click lookback window and impression lookback window, but gives the most weight to the first event and last events, with successively less weight to the events in the middle of the conversion path. When the conversion is preceded by both paid clicks and impressions, the specified impression override weight is further applied to the impressions. When the conversion is preceded only by impressions, the impressions are weighted according to the advertiser's view-through weight rather than to the impression override weight.</li></ul><p><b>Notes:</b><ul><li>All attribution rules besides Last Event are available only for advertisers with Adobe Advertising click tracking and with conversion tracking from either Adobe Advertising or Adobe Analytics (with an Analytics integration).</li><li>Attribution rules apply to clicks on paid ads in any channel. They don't apply to impressions for paid search ads, which can't be tracked at the event level.</li><li>When you report conversion data using any attribution rule except one of the "Last Event" rules, the events leading up the conversion may occur across multiple portfolios. When this is so, the view includes data for the conversion only when the ads or keywords in those portfolios are included in the view.</li><li>For default views, we recommend that you keep the default attribution rule, which is used to compute the [objective value](/help/search-social-commerce/glossary.md#o-p) (formerly called "weighted revenue") for each bid unit during bid optimization.</li></ul> |
|   | Conversions Based On | How to report conversion data:<ul><li><i>Transaction date</i> (the default): To see transactions whose transaction date occurred during the specified time period. This indicates how much revenue was earned within the specified time period.</li><li><i>Click date</i>: To see transactions that resulted from a click that occurred during the specified time period. When a portfolio has significant delay between clicks and transactions, this option is useful for computing the historical revenue per click for the portfolio, which indicates the revenue behaviors to expect over time. |
