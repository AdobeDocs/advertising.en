---
title: Experience-level performance reports
description: Learn how to view experience-level performance reports.
feature: Creative Experiences
---
# Experience-level performance reports

*Closed beta*

You can view detailed performance data for any experience.

## Data in experience-level performance reports

The Report view includes the following data:

* **Overview** tab: A performance overview for the entire experience, including:

  * **Overall Performance** section:
   
   * **Overall Performance**: The total impressions; clicks; click-through rate (CTR); and view-through conversions and click-through conversions for a single conversion metric. <!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

<!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
-->

   * **Default Rate**: (Experiences with decision tree targeting only) The number of impressions resulting from targeted creatives, generic creatives without a target or targeted to "Everyone Else", and the default creative for the experience.
   
<!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"}
-->

  * **Performance Breakdown** section: 
   
    * **Regional Performance:*: Individual metrics by geographical location.
    
      <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->
      
      <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

    * **Device Performance:** Individual metrics by device type, operating system, and browser. Optionally click the value for any device category to see a list of the top <!-- NN --> creatives served with that criteria.
    
      <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Creative Performance** tab*: A performance overview by creative and bundle or ad tag, including:

   * **Creatives** sub-tab: The total number of impressions, clicks, and CTR for each creative in the experience.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->
   
   * **Bundles/Tags** sub-tab:  The total number of impressions, clicks, and CTR for individual bundles (experiences with decision tree targeting) or ad tags (experiences without decision tree targeting) in the experience.
   
     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## View performance reports for an experience

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific experiences.

1. Select the experience:
   
   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Reports]**.
   
   * In table view, hold the cursor over the row and click **[!UICONTROL Reports]**.

   The [!UICONTROL Overview] tab opens.

1. (Optional) In the upper right toolbar, specify the date range, conversion attribution rule, and conversions reported within all of the performance reports:

   * (Optional) To change the date range for the performance data, choose an option in the date menu:
   
     * To specify a preset period, select the report: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* or *[!UICONTROL Yesterday]*.
     
     * To specify a custom date range, specify the start date and end date <!-- in the format MM/DD/YYYY or M/D/YYYY,--> or click ![calendar icon](/help/search-social-commerce/assets/calendar.png) next to a field and select a date.
   
   * (Optional) To change the rule used to attribute conversion data in a series of events that lead to a conversion, click ![Settings](/help/creative/assets/settings.png) and change the **[!UICONTROL Attribution Rule]**.

   * (Optional) To change the conversions reported, click ![Settings](/help/creative/assets/settings.png) and select the conversion names in the **[!UICONTROL Conversions]** menu.<!-- Just one or multiple? Verify how these show up -- I need to see an advertiser with multiple conversions already set up -->

     The available conversion columns include the conversions available in Advertising Search, Social, & Commerce, whether or not you are a Search, Social, & Commerce customer. This can include conversion and site engagement metrics synced from Adobe Analytics. <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> For more information about including collected conversions in reports, see the Search, Social, & Commerce Guide topic “[About managing an advertiser's conversion metrics](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)."

1. (On the [!UICONTROL Overview] tab):

  * (Optional) In the [!UICONTROL Overall Regional Performance] section, hold the cursor over a point in the chart to see data for that point.

  * (Optional) In the [!UICONTROL Regional Performance] section, do any of the following:
  
    * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.
    
    * Select the region in the [!UICONTROL Region] menu.

    * Hold the cursor over a country or state to see data for that region.

   * (Optional) In the [!UICONTROL Device Performance] section, do any of the following:

    * Hold the cursor over value for any device category to see data for that criteria.
    
    * Click the value for any device category to see a list of the top <!-- NN--> creatives served with that criteria.

1. (Optional) To view data by creative and by bundle or ad tag, click the **[!UICONTROL Creative Performance]** tab.

   * On the [!UICONTROL Creatives] subtab, you can do any of the following:
   
     * (Optional) To switch between chart view and grid view, click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid"), respectively.

     * (Optional) In the chart view, hold the cursor over a point in the chart to see data for that point.
     
     * (Experiences with decision tree targeting only; optional) To break out the performance for each applied ad target, enable **[!UICONTROL Split targeting]**.

1. To view data by by bundle (experiences with decision tree targeting) or ad tag (experiences without decision tree targeting), click the **[!UICONTROL Bundles]** subtab. You can do any of the following:

   * (Optional) To switch between chart view and grid view, click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid"), respectively.
   
   * (Optional) In the chart view, hold the cursor over a point in the chart to see data for that point.
   
   * (Experiences with decision tree targeting only; optional) To break out the performance for each applied ad target, enable **[!UICONTROL Split targeting]**.

1. (Optional) To download the data in a [!DNL Microsoft Excel] file in spreadsheet (XLSX) format, click ![Download](/help/creative/assets/download.png "Download") in the toolbar.

   The file is downloaded according to your browser's normal procedure.

>[!MORELIKETHIS]
>
>* [Custom Creative Report](/help/creative/report-custom-creative.md)
