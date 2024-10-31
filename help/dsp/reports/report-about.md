---
title: About Custom Reports
description: Learn about options for creating custom reports manually or using pre-configured report templates.
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
---
# About Custom Reports

Custom reports allow you to customize the content and delivery of your report data using the campaign dimensions (such as the advertiser, placement, sites, or geos) and the metrics that matter most to you. You can either:

* Completely configure campaign performance reports at a granular level.

* Choose from pre-configured report templates, and optionally customize them further.

You can generate reports once, or schedule them daily, weekly, or monthly at 03:00 in the specified time zone according to specified criteria (such as every 15 days or on the 1st of each month). Once a report is generated, you can download it from [!UICONTROL Reports] > [!UICONTROL Custom Reports] or from linked [report destinations](/help/dsp/reports/report-destinations/report-destination-about.md) of the following types:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* FTP SSL <!-- (in beta) -->
* SFTP

>[!NOTE]
>
>You can also view on-demand data at all levels of a campaign (campaign, package, placement, or ad) [within the relevant campaign management view](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Available Report Types

* **[!UICONTROL Custom]:** This report is a blank template that you can use to create your own custom report using most dimensions and metrics. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], and [!UICONTROL Site] reports are variations of this template with pre-selected columns and dimensions for their respective use cases.

* Pre-configured Report Templates

    * **[!UICONTROL Billing]:** Use this report to understand key billing metrics like spend metrics for media billing by campaign. Data isn't available for placements that target universal IDs.

       >[!NOTE]
       >
       >This report includes data about the billing segment. If a user or device is served an impression that belongs to multiple segments, only one billable segment is credited with the impression.

    * **[!UICONTROL Conversion]:** Use this report to understand how your campaigns are performing based on conversion metrics captured using Adobe Advertising conversion tracking. This report includes multi-touch attribution.

    * **[!UICONTROL Device]:** Use this pre-populated template to see key metrics by device-related dimensions.

    * **[!UICONTROL Frequency (by Impression)]:** Use this report to understand the distribution of impressions shown to unique viewers (for example, how many unique viewers saw one impression, two impressions, three impressions, and so on. Data is available by placement or campaign.

       >[!NOTE]
       >
       >* Data is available after 1 March 1 2019.
       >* Frequency is estimated based on a sampling of data.
       >* For some inventory, publishers don't pass along a device identifier, which prevents frequency tracking. This report includes only impressions for which a device identifier was available.

    * **[!UICONTROL Frequency (by App/Site)]:** Use this report to understand how many unique users your ads reached by app or by site. You can also see how many unique users your ads reaced reached via only a particular app or site ("distinct unique users").

       >[!NOTE]
       >
       >* Data is available after 15 November 15 2018.
       >* For some private inventory, publishers don't pass along a device identifier, which prevents frequency tracking.

    * **[!UICONTROL Geo]**: Use this pre-populated template to see key metrics by geographic dimensions.

    * **[!UICONTROL Margin]:** Use this report to see key metrics like margin, profit, and other spend metrics by campaign or placement. Data isn't available for placements that target universal IDs.

    * **[!UICONTROL Segment]:** Use this pre-populated template to see key metrics by segment.

       >[!NOTE]
       >
       >* This report is intended to show how different targeted segments perform. It uses segment membership data. When an impression is served to a person or device belonging to two or more targeted segments, this report includes one row for each segment. For this reason, totals in this report may not match actual delivery.
       >* Conversion metrics and custom goal data for segments are available after 2 August 2019. All other data for segments is available beginning after 1 June 1 2018.

    * **[!UICONTROL Site]:** By default, includes standard metrics, total media net spend, and total billable net spend by site.

    * **[!UICONTROL Household Reach & Frequency]:** Use this report to see impressions, reach, and frequency for a single dimension across ad formats at a household level based on IP address, rather than at a device/cookie level. Use the insights to optimize your media mix, improve performance, and identify opportunities for incremental reach. See "[FAQs About Household Reports](/help/dsp/reports/faq-reports.md)" for more information. Data isn't available for placements that target universal IDs.
    
    * **[!UICONTROL Household Conversions]:** Use this report to see view-through conversions at the household level based on IP address, rather than at a device/cookie level. Use the insights to measure and optimize campaign performance. See "[FAQs About Household Reports](/help/dsp/reports/faq-reports.md)" for more information. Data isn't available for placements that target universal IDs.
  
    * **[!UICONTROL Path to Conversion Beta]:** (Beta feature) Use this report to identify how to optimize budgets and personalize ads based on top-performing ad interaction sequences. The report shows the sequence of interaction points in the same household that lead to each of the selected conversion metrics in the specified data range. The report uses a specified lookback period between the first interaction and a conversion and can include one dimension:
    
      * [!UICONTROL Channel Assist Type]: Shows how the following  marketing channels have assisted the conversion process: [!UICONTROL Audio Impression], [!UICONTROL CTV Impression], [!UICONTROL Display Click], [!UICONTROL Display Impression], [!UICONTROL Native Click], [!UICONTROL Native Impression], [!UICONTROL Search Click], [!UICONTROL Video Click], or [!UICONTROL Video Impression].
      
      * [!UICONTROL Campaign ID] or [!UICONTROL Campaign Name]: Shows which campaigns have assisted the conversion process.
      
      *  [!UICONTROL Ad ID] or [!UICONTROL Ad Name] shows which DSP ads have resulted in conversions.
      
      * [!UICONTROL Ad ID & Paid Keyword (SSC)] or [!UICONTROL Ad Name & Paid Keyword (SSC)] shows which Search, Social, & Commerce keywords have resulted in conversions.
    
      Columns in the report include "[!UICONTROL Event #1]" through "[!UICONTROL Event #10],""[!UICONTROL Path Length]," "% \<Conversion Metric Name 1\>," "% \<Conversion Metric Name 2\>," and so on.
      
      Up to the 10 most recent interaction points are included. The path rows are ordered by the number of conversions.

      For a comparison of this report to reports created by [!DNL Advanced Measurement Services] and Adobe Analytic, see "[FAQs About Custom Reports](/help/dsp/reports/faq-reports.md)."
  
    * **[!UICONTROL Path Length Beta]:** (Beta feature) Use this report to      track the number of user interaction points required for conversions over time so you can choose the optimal ad frequency. The report shows the number of conversions by path length (interaction points), such as how many conversions occurred after users had only one ad interaction, two ad interactions, and so on. The report can include data for multiple conversion metrics and uses a specified lookback period between the first interaction and a conversion. Columns in the report include "[!UICONTROL Path Length]," "[!UICONTROL Number of] \<Conversion Metric Name 1\>," "% \<Conversion Metric Name 1\>," \<Conversion Metric Name 2\>," "% \<Conversion Metric Name 2\>," and so on.
    
      Data is shown for each path length of up to 10; data for path lengths greater than 10 are grouped together.
    
    * **[!UICONTROL Time to Conversion Beta]:** (Beta feature) Use this report to determine the optimal attribution lookback window and to identify campaigns with longer times to conversion, which may benefit from retargeting. The report shows the number of conversions by the length of time in days from the last interaction (ad exposure or click) to conversion. The report can include data for multiple conversion metrics and uses a specified lookback period between the first interaction and a conversion. Columns in the report include "[!UICONTROL Time Taken (in days)]," "[!UICONTROL Number of] \<Conversion Metric Name 1\>," "% \<Conversion Metric Name 1\>," \<Conversion Metric Name 2\>," "% \<Conversion Metric Name 2\>," and so on. Conversions that take longer than the lookback period are grouped together in one row (for example, if the report uses a 30-day lookback period, then all conversions that take longer than 30 days to occur are grouped together in a row with a "[!UICONTROL Time Taken (in days)]" value of "30+").    

## Cross-Account Reporting {#cross-account-reporting}

Any organization with multiple DSP accounts can optionally enable cross-account data in custom reports, according to the organization's needs. For example, you can give Account A access to Account B's data, and give Account B access to Account C's (but not Account A's) data. To enable and configure this feature, contact your Adobe Account Team.

Once the feature is enabled for your organization, you can [filter](report-settings.md) any of the following report types by account:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], and [!UICONTROL Conversion].

Your account settings at [!UICONTROL Settings] > [!UICONTROL Account] indicate a) the other accounts whose data is available to your account and b) the other accounts that can access your account's data.

## The [!UICONTROL Custom Reports] View

[!UICONTROL Reports] > [!UICONTROL Custom Reports] lists your existing reports, including reports that were generated, those that are scheduled for future generation, and those that failed. The “[!UICONTROL Report Run]" column shows dates on which the report was triggered beginning on 22 August 2024. By default, all unarchived reports created by the user are listed, with the most recent on top. You can further filter the list by status, whether the report is recurring or one-time, the report type, the destination type, and the report creator. 

You can create new custom reports, edit existing reports or duplicate them to create new reports, run reports immediately, download any report instance from the last four months, and delete reports. 

## Report Statuses {#custom-report-status}

* **[!UICONTROL Yet to start]:** The report has never been run.

* **[!UICONTROL Report generating]:** The report is currently being created.

* **[!UICONTROL Ready to download]:** (Recurring reports only) One or more instances of the report is available to download, and more report instances are scheduled.

* **[!UICONTROL Failed]:** The report job failed. To see why individual report instances failed for a report tow, click ![the Down arrow](/help/dsp/assets/chevron-down.png "the Down arrow") next to [!UICONTROL Download]. Failed report jobs are indicated with an error icon (![error indicator](/help/dsp/assets/indicator-critical.png "error indicator")). Hold the cursor over the error icon for a description of the error.

* **[!UICONTROL Completed]:** For non-recurring reports, the report is completed. For recurring reports, all report instances are completed. You can download all reports completed in the last four months.

* **[!UICONTROL Archived]:** The report is archived and can't be run. This status is set when report generation fails multiple times for a report. Currently, you can't set this status from the user interface.

>[!MORELIKETHIS]
>
>* [Create a Custom Report](/help/dsp/reports/report-create.md)
>* [Download a Custom Report](/help/dsp/reports/report-download.md)
>* [Custom Report Settings](/help/dsp/reports/report-settings.md)
>* [FAQs About Household Reports](/help/dsp/reports/faq-reports.md)
>* [Types of Performance Reports in Campaign Management Views](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Available Report Columns](/help/dsp/reports/report-columns.md)
>* [About [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
