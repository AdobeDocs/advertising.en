---
title: Manage custom reports
description: Learn how to generate and manage the cross-experience [!UICONTROL Custom Creative Report].
feature: Creative Reporting
---
# [!UICONTROL Manage custom reports]

You can create, duplicate, edit, run, download, and delete custom reports.

## Create a custom report {#report-create}

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. In the upper right, click **[!UICONTROL Create]**.

1. Specify the [report settings](#report-settings).

1. Click **[!UICONTROL Create Custom Report]**.

## Duplicate a custom report

Duplicate a custom report to create a new report with similar settings.

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Next to the report name, click **[!UICONTROL ...]** > **[!UICONTROL Copy]**.

1. (Optional) Edit the [report settings](#report-settings.md) as needed.

    The report name, by default, is "\<*existing report name*\> \#2" (or the next number in the sequence).

## Edit a custom report {#report-edit}

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Next to the report name, click **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

1. Edit the [report settings](#report-settings.md).

1. Click **[!UICONTROL Edit Custom Report]**.

## Run a custom report {report-run-now}

You can run any report that hasn't expired and isn't currently running.

>[!NOTE]
>
>You can also run a custom report when you [create](#report-create) or [edit](#report-edit) it.

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Next to the report name, click **[!UICONTROL ...]** > **[!UICONTROL Run Now]**.

   When the report's completed, it's sent to the destinations specified in the report settings.

## Download a custom report

You can download any completed report instance from the last four months, which has with the status "[!UICONTROL Ready to Download]" or "[!UICONTROL Completed]".

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. In the [!UICONTROL Download Report] column for the report row, do the following:

   * To download the latest instance of the report, click **[!UICONTROL Download]**.
   
   * (Reports with multiple instances) Click ![the Down arrow](/help/dsp/assets/chevron-down.png "the Down arrow") next to [!UICONTROL Download], and then click the completion date for the report you want to download. Downloadable report instances are indicated with a download icon (![download icon](/help/dsp/assets/indicator-downloadable.png "download icon")).
   
     When many instances are available, click **[!UICONTROL Load More]** at the bottom of the list if necessary.

     When a report runs multiple times on the same day, the report instances for that day are listed in chronological order, with the most recent instance on top.
     
     Failed report jobs are indicated with an error icon (![error indicator](/help/dsp/assets/indicator-critical.png "error indicator")) and can't be downloaded. Hold the cursor over the error icon for a description of the error.

## Delete a custom report

1. In the main menu, click **[!UICONTROL Reports]** > **[!UICONTROL Custom Reports]**.

1. Next to the report name, click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## Report Settings {#report-settings}

**[!UICONTROL Name]:** The report name. The maximum length is 180 characters.

**[!UICONTROL Report Type]:** The type of report.

### [!UICONTROL Report Range] Section

This section determines the data that's included in the report. To set up dates for the report schedule, see the "[!UICONTROL Report run schedule]" section.

**[!UICONTROL Timezone]:** The timezone for reporting.

**[!UICONTROL Observe Daylight Savings Time]:** Considers Daylight Saving Time in the reported times.

**Range:** The date range for which to generate data. The number of days available varies by report and by the selected dimensions. Choose one:

* **[!UICONTROL Previous Calendar Week]:** Includes data for the previous calendar week.

* **[!UICONTROL Previous Calendar Month]:** Includes data for the previous calendar month.

* **[!UICONTROL Custom Range]:** Includes data between specific beginning and end dates. To report data through the previous day, select **[!UICONTROL Present]**.

### [!UICONTROL Report Run schedule] Section

This section determines the dates on which the report is run. To set up the dates for which to include report data, see the "[!UICONTROL Report range]" section.

**\[Schedule\]:** When to generate the report:

* *[!UICONTROL Immediately]*: Immediately adds the report to the report queue.

  >[!NOTE]
  >
  >You can also [run a custom report at any time](#report-run-now) from the [!UICONTROL Reports] view.

* *[!UICONTROL On] \<Date\>:* Runs the report on a specified date for completion by 09:00 in the account's time zone.

* *[!UICONTROL Recurring]:* Runs the report according to a schedule during a specified time period.

  * **\[Schedule\]:** How often to run the report: 
  
    * *Daily* to run the report every N number of days. For example, to run the report every two weeks (14 days), select this option and enter **14**.
  
    * *Weekly* to run the report on specified days of the week. For example, to run the report every Monday and Friday, select this option and select the check boxes next to **Monday** and **Friday**.

    * *Monthly* to run the report on a specific numeric day of the month, from 1 to 30. For example, the run the report on the first day of every month, select this option and enter **1**.

  * **From**: The first date on which the report can be run. Depending on the specified schedule, the first report instance may occur after this date.
  
  * **Until**: The report expiration date, which can be up to four calendar months away. Before a report expires, all specified email destinations receive an email alert seven days and one day before the expiration date. To keep the report longer, change this date.

### [!UICONTROL Apply Filters] Section

**[!UICONTROL Filter by]:** (Optional) Additional dimensions by which to filter the data, whether or not the dimensions are included as columns in the report. The  available filters vary by report type and may include: *[!UICONTROL Advertiser]*, *[!UICONTROL Experience]*, *[!UICONTROL Creative Library]*, and *[!UICONTROL DSP]*<!-- Clarify what this is for, Advertising DSP or whatever DSP the ads were run from? -->.

To apply one or more filters, do the following:

* Select a dimension, select the operator (*equals* or *not equals*), and then select the applicable value. For example, to return data for only preroll ads, specify "[!UICONTROL Ad Type equals Preroll]."
* (Optional) Add additional criteria to the filter.
* (Optional) Add additional filters, each with one or more criteria.

### [!UICONTROL Build Your Report] Section

**[!UICONTROL Select To Add As Report Headers]:**  The data columns, or headers, to include in the report. To add a column, expand the category and select the check box next to the column name. The available columns vary by report, and all unavailable metrics are disabled.<!-- Add back once I have this completed, and reconsider wording of link/anchor:  See "[Available Report Columns](#report-custom-creative-columns)" for descriptions of all options. -->

**[!UICONTROL Drag to Re-Order Report Headers Below]:** The order of the column headers. You can drag and drop any column to customize the order.

**[!UICONTROL Format]:** Whether to generate a report in *[!UICONTROL CSV]* (comma-separated values) or *[!UICONTROL Tab]* (tab-separated values) format.

**[!UICONTROL Headers]:** Whether to *[!UICONTROL Include]* or *[!UICONTROL Do Not Include]* column headers.

### [!UICONTROL Multi-Touch Conversion Options] Section

**[!UICONTROL Attribution Rule Settings]:** The settings vary by report type:

* **\[Rule Type\]:** (Advertisers with Adobe Advertising conversion tracking only) Within the report, how to attribute conversion data in a series of events that lead to a conversion. You can choose more than one rule if you want to compare differences between the rules.

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

**[!UICONTROL Paths as Columns]:**  Which types of conversions to report when prior events occurred on the same device. You can include up to three types. For each selected type, a separate column is included for each conversion metric and is appended with the specified suffix ([!UICONTROL (tl)], [!UICONTROL (ct)], or [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Includes conversions attributed to clicks (CT for click-through) and to impressions (VT for view-through). Conversions attributed to impressions are multiplied by the specified view-through weight. The default view-through weight is 100%, which means that conversions attributed to impressions are counted as 100% of the value of conversions attributed to clicks.

* *[!UICONTROL With Clicks (CT)]:* Includes only conversions attributed to clicks.

* *[!UICONTROL Impressions Only (VT)]:* Includes only conversions that were attributed to impressions because no clicks were tracked in the conversion path.

### [!UICONTROL Add Report Destinations] Section

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

**[!UICONTROL Destination Name]:** (S3, FTP, sFTP, and FTP SSL destination types only) The names of the [report destinations](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"} to which the custom report is sent.

* To specify an existing destination, select a destination name from the list. You can select multiple destination names separately.

* To create a new destination:

  1. Click **Add New Destination**.

  1. Enter the [report destination settings](/help/dsp/reports/report-destinations/report-destination-settings.md){target="_blank"}, and click **Save**.

  1. Back in the report settings, click **Refresh Destination Names.**

      The new destination is now available from the list of existing destinations, and you can optionally add it to the report.


<!-- This needs a lot of updating for new report:

## Available Report Columns {#report-custom-creative-columns}

|Metric Type|Subtype|Column Name|Description|
|-----------|-------|-----------|-----------|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Ad Size]|The dimensions of the published ad.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Is Default]|Whether the served ad was a default image ad or video ad for the experience.|
|\[Dimension\]|[!UICONTROL Ad]|[!UICONTROL Rotation Type]| Whether ads were rotated algorithmically (*Algorithmic*), in a specified sequence (*Sequenced*), or according to relative weights (*Weighted*).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative ID]| The ID that [!UICONTROL Creative] assigned to the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Name]| The name of the creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Creative Type]| The type of creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative ID]| The ID that [!UICONTROL Creative] assigned to the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Name]| The name of the parent creative.|
|\[Dimension\]|[!UICONTROL Creative]|[!UICONTROL Parent Creative Type]| The type of parent creative (such as [!UICONTROL HTML5]).|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Ad Link]| The landing page URL.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Click Type]| The specific type of user interaction.|
|\[Dimension\]|[!UICONTROL Click Events]|[!UICONTROL Direction]| The directional flow or navigation path of the user's click interaction within the creative experience. |
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 1]| The value of Attribute 1 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 2]| The value of Attribute 2 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 3]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 4]| The value of Attribute 3 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Custom Attributes]|[!UICONTROL Custom Attribute 5]| The value of Attribute 5 in the pixel tag, when it was included.|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Browser]|The browser in which the ad was shown (such as [!UICONTROL Chrome] or [!UICONTROL Firefox]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device OS]|The operating system on which the ad was shown (such as [!UICONTROL Windows]).|
|\[Dimension\]|[!UICONTROL Device]|[!UICONTROL Device Type]|The type of device on which the ad was shown (such as [!UICONTROL Desktop]).|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Name]| The name of the DSP on which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement ID]| The ID of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Placement Name]| The name of the placement for which ads were run. |
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site ID]| The ID of the site on which ads were run.|
|\[Dimension\]|[!UICONTROL DSP]|[!UICONTROL DSP Site Name]| The name of the site on which ads were run. |
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Ad Tag Id]|The ID that [!UICONTROL Creative] assigned to the ad experience tag.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Advertiser Name]| The name of the advertiser.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Date/Time]|The date and time of the event.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience ID]| The ID that [!UICONTROL Creative] assigned to the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Experience Name]| The name of the experience.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Targeting Branch Value]| The specific path through the targeting decision tree that determined which creative experience variant was served to the user.|
|\[Dimension\]|[!UICONTROL Experiences]|[!UICONTROL Trafficking Line]| The name of the ad tag. |
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL City]|The city to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Country Code]|The country code for the country to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL DMA]|The Designated Market Area (DMA) to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL State Code]|The state code for the state to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Geo]|[!UICONTROL Zip Code]|The zip code to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category ID]|(Dynamic ads) The target product category ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Category Name]|(Dynamic ads) The target product category name.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 1]|(Dynamic ads) The first creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 2]|(Dynamic ads) The second creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 3]|(Dynamic ads) The third creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 4]|(Dynamic ads) The fourth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Creative Attribute 5]|(Dynamic ads) The fifth creative attribute.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product ID]|(Dynamic ads) The target product ID.|
|\[Dimension\]|[!UICONTROL Product]|[!UICONTROL Product Name]|(Dynamic ads) The target product name.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Matched Audience Segment ID]|The IDs for up to five user segments that matched the ad theme.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment ID]|The ID for a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Pixel Segment Name]|The name of a retargeting pixel to which the reported data is attributed.|
|\[Dimension\]|[!UICONTROL Segment]|[!UICONTROL Segment Values]|The attributes for an audience segment to which the reported data is attributed.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Clicks]|The sum of all clicks on an ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL CTR]|The click-through rate, which is the percentage of clicks divided by ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagement Rate]|The percentage of impressions served that resulted in user engagements.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Engagements]|The number of interactions on a served ad.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Impressions]|The total number of ad impressions.|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Media Match Rate]| The percentage of impressions with a retargeted cookie. |
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Clicks]|(Dynamic ads only) The sum of all clicks on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion]|(Dynamic ads only) The sum of all conversions on ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Conversion Rate]|(Dynamic ads only) The percentage of ads for a product that resulted in conversions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product CTR]|(Dynamic ads only) The click-through rate for ads for a product, which is the percentage of clicks divided by ad impressions. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Impressions]|(Dynamic ads only) The total number of impressions for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Product Revenue]|(Dynamic ads only) The total revenue on served ads for a product. When the product is null, this value is zero (0).|
|[!UICONTROL Metrics]|[!UICONTROL Standard]|[!UICONTROL Revenue]|The total revenue on served ads.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completion Rate]|The percentage of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completion Rate]|The percentage of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completion Rate]|The percentage of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completion Rate]|The percentage of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 100% Completions]|The number of views that watched the ad in its entirety.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 25% Completions]|The number of views that watched at least one quartile of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 50% Completions]|The number of views that watched at least two quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL 75% Completions]|The number of views that watched at least three quartiles of the ad.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Avg Percent Viewed]|The average percentage an ad was watched to completion, accounting for all views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Play Rate]|The percentage of impressions served that resulted in video views.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Playtime per View]|The average duration of a video view, measured in seconds.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Viewed Minutes]|The total number of minutes a video ad was viewed.|
|[!UICONTROL Metrics]|[!UICONTROL Video]|[!UICONTROL Views]|The total number of video ad views.




|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 100% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL 50% Viewable Completion (%)]| .|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewability Rate (%)]|The percentage of viewable impressions out of all measurable impressions, calculated as <code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]</code>.|
|[!UICONTROL Metrics]|[!UICONTROL Viewability]|[!UICONTROL Viewable Impressions]|The number of ad impressions considered viewable.|
|[!UICONTROL Conversion Metrics]|[Grouped by advertiser in report settings]|[Advertiser-specific conversion]| The total for a specified advertiser-specific conversion metric or Adobe Analytics event.|
|[!UICONTROL Custom Goals]|[Grouped by advertiser in report settings]|[Advertiser-specific custom goal]|(Advertisers with Advertising DSP) The weighted sum of all conversions that are included in the specified [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).|

{style="table-layout:auto"}

-->

>[!MORELIKETHIS]
>
>* [Experience-level performance reports](/help/creative/experiences/experience-performance-details.md)
>* [About DSP custom reports](/help/dsp/reports/report-about.md){target="_blank"}
>* [About [!UICONTROL report destinations]](/help/dsp/reports/report-destinations/report-destination-about.md){target="_blank"}
