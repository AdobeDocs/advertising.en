---
title: Custom Report Settings
description: See descriptions of the custom report settings.
feature: DSP Custom Reports
exl-id: 0e9e4332-3c10-44b0-b315-691b22dfb3c7
---
# Custom Report Settings

**[!UICONTROL Name]:** The report name. The maximum length is 180 characters.

**[!UICONTROL Report Type]:** The type of report: *[!UICONTROL Custom]* (which includes most available options), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*, *[!UICONTROL Site]*, *[!UICONTROL Household Reach & Frequency]*, *[!UICONTROL Household Conversions]*, *[!UICONTROL]*, *[!UICONTROL Path Length]*, or *[!UICONTROL Time to Conversion]*.

## [!UICONTROL Report Range] Section

This section determines the data that's included in the report. To set up dates for the report schedule, see the "[!UICONTROL Report run schedule]" section.

**[!UICONTROL Timezone]:** The timezone for reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Considers Daylight Saving Time in the reported times.

**Range:** The date range for which to generate data. The number of days available varies by report and by the selected dimensions. Choose one:

* **[!UICONTROL Previous Calendar Week]:** Includes data for the previous calendar week.

* **[!UICONTROL Previous Calendar Month]:** Includes data for the previous calendar month.

* **[!UICONTROL Custom Range]:** Includes data between specific beginning and end dates. To report data through the previous day, select **[!UICONTROL Present]**.

## [!UICONTROL Report Run schedule] Section

This section determines the dates on which the report is run. To set up the dates for which to include report data, see the "[!UICONTROL Report range]" section.

**\[Schedule\]:** When to generate the report:

* *[!UICONTROL Immediately]*: Immediately adds the report to the report queue.

  >[!NOTE]
  >
  >You can also [run a custom report at any time](report-run-now.md) from the [!UICONTROL Reports] view.

* *[!UICONTROL On] \<Date\>:* Runs the report on a specified date for completion by 09:00 in the account's time zone.

* *[!UICONTROL Recurring]:* Runs the report according to a schedule during a specified time period.

  * **\[Schedule\]:** How often to run the report: 
  
    * *Daily* to run the report every N number of days. For example, to run the report every two weeks (14 days), select this option and enter **14**.
  
    * *Weekly* to run the report on specified days of the week. For example, to run the report every Monday and Friday, select this option and select the check boxes next to **Monday** and **Friday**.

    * *Monthly* to run the report on a specific numeric day of the month, from 1 to 30. For example, the run the report on the first day of every month, select this option and enter **1**.

  * **From**: The first date on which the report can be run. Depending on the specified schedule, the first report instance may occur after this date.
  
  * **Until**: The report expiration date, which can be up to four calendar months away. Before a report expires, all specified email destinations receive an email alert seven days and one day before the expiration date. To keep the report longer, change this date.

## [!UICONTROL Apply Filters] Section

**[!UICONTROL Filter by]:** (Optional) Additional dimensions by which to filter the data, whether or not the dimensions are included as columns in the report. The available filters vary by report type and may include: *[!UICONTROL Account]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Ads]*, *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Country]*, *[!UICONTROL Package]*, *[!UICONTROL Placement]*, *[!UICONTROL Video]*, and *[!UICONTROL Video Duration]*.

<!-- Add when available:
*[!UICONTROL Deal ID]*, *[!UICONTROL Deal List]*, 
-->

To apply one or more filters, do the following:

* Select a dimension, select the operator (*equals* or *not equals*), and then select the applicable value. For example, to return data for only preroll ads, specify "[!UICONTROL Ad Type equals Preroll]."
* (Optional) Add additional criteria to the filter.
* (Optional) Add additional filters, each with one or more criteria.

\* *[!UICONTROL Account]* is available for the following report types only when your organization is configured for [cross-account reporting](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], and [!UICONTROL Conversion]. Contact your Adobe Account Team for more information about cross-account reporting.

**[!UICONTROL Include data from Adobe Advertising SSC]:** (Path to Conversion, Path Length, and Time to Conversion reports only) Includes data for clicks on search ads from specified Advertising Search, Social, & Commerce campaigns. When you select this option:

1. Select the Search, Social, & Commerce account using the **Filter by [!UICONTROL SSC Account]** filter.

1. Select the campaigns using the **Filter by [!UICONTROL SSC Campaign]** filter.

   To select multiple campaigns, click **[!UICONTROL Add Criteria]** for the second and subsequent campaigns.

## [!UICONTROL Build Your Report] Section

**[!UICONTROL Select To Add As Report Headers]:**  The data columns, or headers, to include in the report. To add a column, expand the category and select the check box next to the column name. The available columns vary by report, and all unavailable metrics are disabled. The available data categories may include:

* [!UICONTROL Dimensions]

  >[!NOTE]
  >
  > The [!UICONTROL Household Reach & Frequency] and [!UICONTROL Path to Conversion] reports can include only one dimension.
  > The [!UICONTROL Path Length] and [!UICONTROL Time to Conversion] reports don't include dimensions.

* [!UICONTROL Metrics]

  >[!NOTE]
  >
  >The [!UICONTROL Household Reach & Frequency] report can include either overlap metrics or non-overlap metrics, but not both.

* [!UICONTROL Conversion Metrics] (sorted by advertiser)

* [!UICONTROL Custom Goals] (sorted by advertiser)

See "[Available Report Columns](report-columns.md)" for descriptions of all options.

**[!UICONTROL Drag to Re-Order Report Headers Below]:** The order of the column headers. You can drag and drop any column to customize the order.

**[!UICONTROL Format]:** Whether to generate a report in *[!UICONTROL CSV]* (comma-separated values) or *[!UICONTROL Tab]* (tab-separated values) format.

**[!UICONTROL Headers]:** Whether to *[!UICONTROL Include]* or *[!UICONTROL Do Not Include]* column headers.

## [!UICONTROL Multi-Touch Conversion Options] Section

**[!UICONTROL Attribution Rule Settings]:** The settings vary by report type:

* **\[Attribution Type\]:** ([!UICONTROL Household Conversion] reports with [!UICONTROL Conversion Metrics] or [!UICONTROL Custom Goals] columns) Within the report, how to attribute conversion data in a series of events that lead to a conversion:
  
  * *[!UICONTROL Unique]:* (The default) Counts the number of times a dimension value (such as a device or placement) was on the path to conversion.
  
  * *[!UICONTROL Multi-Touch Attribution (MTA)]:*  Distributes the credit of each conversion based on the frequency of occurrence of the dimension value (such as a device or placement) on the path to conversion. For example, if there were total of 10 impressions before conversion, with 8 on CTV and 2 on Mobile, then 80% of the credit (0.8) is given to CTV screens and 0.2 to Mobile.

* **\[Rule Type\]:** (All [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], and [!UICONTROL Site] reports with [!UICONTROL Conversion Metrics] or [!UICONTROL Custom Goals] columns; advertisers with Adobe Advertising conversion tracking only) Within the report, how to attribute conversion data in a series of events that lead to a conversion. You can choose more than one rule if you want to compare differences between the rules.

  >[!NOTE]
  >
  >Conversion paths include any impressions and clicks within the advertiser's impression or click lookback windows, which are configured in [!DNL Advertising Search, Social, & Commerce]. Clicks are given preference to impressions during conversion attribution. Any clicks in a conversion path receive full credit based on the attribution rule. Impressions receive credit only when no clicks are tracked in the conversion path.

  * *[!UICONTROL Last Event]:* Attributes conversions to the last click or impression in the conversion path.  

  * *[!UICONTROL Weight Last More]:* Attributes conversions to all events in the conversion path but gives the most weight to the last event and successively less weight to the preceding events.

  * *[!UICONTROL Even Distribution]:* Attributes conversions equally to each event in the conversion path.

  * *[!UICONTROL Weight First More]:* Attributes conversions to all events in the conversion path but gives the most weight to the first event and successively less weight to the following events.

  * *[!UICONTROL First Event]:* Attributes conversions to the first click or impression in the conversion path.

  * *[!UICONTROL U-shaped]:* Attributes the conversion to all events in the conversion path but gives the most weight to the first and last events, with successively less weight to the events in the middle of the conversion path.

  * *[!UICONTROL Display Only]:*  Attributes conversions to the last DSP click or impression in the conversion path. This includes video and connected TV ads and excludes clicks on [!DNL Advertising Search, Social, & Commerce] ads.

  * *[!UICONTROL Social Only]:* Obsolete

 See also "[How Attribution Rules Are Calculated for Adobe Advertising](/help/search-social-commerce/reports/attribution-rules.md)."

* **Lookback:** ([!UICONTROL Household Conversion] reports with [!UICONTROL Conversion Metrics] or [!UICONTROL Custom Goals] columns, and [!UICONTROL Path to Conversion], [!UICONTROL Path Length], or [!UICONTROL Time to Conversion] reports with [!UICONTROL Conversion Metrics] columns only; advertisers with Adobe Advertising conversion tracking only) Within the report, the maximum number of days after an impression event or a click event (for [!UICONTROL Path to Conversion], [!UICONTROL Path Length], or [!UICONTROL Time to Conversion] reports) in which a conversion event can be attributed to it. The default is *[!UICONTROL 30 days]*, and the maximum is 92 days.

  >[!TIP]
  >
  >If you use [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), then use the same lookback window that you use in [!DNL Analytics].

**[!UICONTROL Paths as Columns]:**  (All [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment], and [!UICONTROL Site] reports with [!UICONTROL Conversion Metrics] or [!UICONTROL Custom Goals] columns) Which types of conversions to report when prior events occurred on the same device. You can include up to three types. For each selected type, a separate column is included for each conversion metric and is appended with the specified suffix ([!UICONTROL (tl)], [!UICONTROL (ct)], or [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Includes conversions attributed to clicks (CT for click-through) and to impressions (VT for view-through). Conversions attributed to impressions are multiplied by the specified view-through weight. The default view-through weight is 100%, which means that conversions attributed to impressions are counted as 100% of the value of conversions attributed to clicks.

* *[!UICONTROL With Clicks (CT)]:* Includes only conversions attributed to clicks.

* *[!UICONTROL Impressions Only (VT)]:* Includes only conversions that were attributed to impressions because no clicks were tracked in the conversion path.

**[!UICONTROL Conversion Reporting Based On]:**  How to report conversion data:

* *[!UICONTROL Conversion Timestamp]:* (The default) Conversions are associated with the conversion date.

* *[!UICONTROL Event Timestamp]:* Conversions are reported based on the date of the impression or click that caused the conversion, as determined by the specified [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Section

**[!UICONTROL Destination Type]:** Where to deliver the completed reports and error notifications. You can't change the destination type once you save the report.

>[!NOTE]
>
>You can always download completed reports from the [!UICONTROL Reports] > [!UICONTROL Custom Reports] view.

* *[!UICONTROL None]:* To not deliver any reports or notifications.

* *[!UICONTROL S3]:* To send the completed report to one or more [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) locations, which you must select in the **[!UICONTROL Destination Name]** field.

* *[!UICONTROL sFTP]:* To send the completed report to one or more SFTP locations, which you must select in the **[!UICONTROL Destination Name]** field.

* *[!UICONTROL FTP]:* To send the completed report to one or more FTP locations, which you must select in the **[!UICONTROL Destination Name]** field.

* *[!UICONTROL FTP SSL] (Currently in Beta):* To send the completed report to one or more FTP SSL locations, which you must select in the **[!UICONTROL Destination Name]** field.

* *[!UICONTROL Email]:* To specify email address(es) to which to send completed reports or notifications if the report is canceled because of errors.

**[!UICONTROL Email]:** (Email destination type only) For each address, enter the address and click **+**.

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP, and FTP SSL destination types only) The names of the report destinations to which the custom report is sent.

* To specify an existing destination, select a destination name from the list. You can select multiple destination names separately.

* To create a new destination:

  1. Click **Add New Destination**.

  1. Enter the [report destination settings](/help/dsp/reports/report-destinations/report-destination-settings.md), and click **Save**.

  1. Back in the report settings, click **Refresh Destination Names.**

      The new destination is now available from the list of existing destinations, and you can optionally add it to the report.

>[!MORELIKETHIS]
>
>* [About Custom Reports](/help/dsp/reports/report-about.md)
>* [Create a Custom Report](/help/dsp/reports/report-create.md)
>* [Duplicate a Custom Report](/help/dsp/reports/report-copy.md)
>* [Edit a Custom Report](/help/dsp/reports/report-edit.md)
>* [Download a Custom Report](/help/dsp/reports/report-download.md)
>* [Run a Custom Report](/help/dsp/reports/report-run-now.md)
>* [Custom Report Settings](/help/dsp/reports/report-settings.md)
>* [About Report Destinations](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Available Report Columns](/help/dsp/reports/report-columns.md)
