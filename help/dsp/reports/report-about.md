---
title: About Custom Reports
description: Learn about options for creating custom reports manually or using pre-configured report templates.
feature: DSP Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
---
# About Custom Reports

Custom reports allow you to customize the content and delivery of your report data using the campaign dimensions (such as the advertiser, placement, sites, or geos) and the metrics that matter most to you. You can either:

* Completely configure campaign performance reports at a granular level.
* Choose from pre-configured report templates, and optionally customize them further.

You can generate reports once, or schedule them to be generated daily, weekly, or monthly at 03:00 in the specified time zone. Once a report is generated, it's delivered to each specified email recipient or to linked [report destinations](/help/dsp/reports/report-destinations/report-destination-about.md) of the following types:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL (in beta)

>[!NOTE]
>
>You can also view on-demand data at all levels of a campaign (campaign, package, placement, or ad) [within the relevant campaign management view](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Available Report Types

* **[!UICONTROL Custom]:** This report is a blank template you can use to create your own custom report using most dimensions and metrics. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], and [!UICONTROL Site] reports are variations of this template with pre-selected columns and dimensions for their respective use cases.

* Pre-configured Report Templates
 
    * **[!UICONTROL Billing]:** Use this report to understand key billing metrics like spend metrics for media billing by campaign.
    
       >[!NOTE]
       >
       >This report includes data about the billing segment. If a user or device is served an impression that belongs to multiple segments, only one billable segment is credited with the impression.

    * **[!UICONTROL Conversion]:** Use this report to understand how your campaigns are performing based on conversion metrics captured using Adobe Advertising conversion tracking. This report includes multi-touch attribution.

    * **[!UICONTROL Device]:** Use this pre-populated template to see key metrics by device-related dimensions.

    * **[!UICONTROL Frequency (by Impression)]:** Use this report to understand the distribution of impressions shown to unique viewers (for example, how many unique viewers saw one impression, two impressions, three impressions, and so on. Data is available by placement or campaign.
           
       >[!NOTE]
       >
       >* Data is available after March 1, 2019.
       >* Frequency is estimated based on a sampling of data.
       >* For some inventory, publishers don't pass along a device identifier, which prevents frequency tracking. This report includes only impressions for which a device identifier was available.
      
    * **[!UICONTROL Frequency (by App/Site)]:** Use this report to understand how many unique users were reached by app or by site. You can also see how many unique users were reached via only a particular app or site ("distinct unique users").

       >[!NOTE]
       >
       >* Data is available after November 15, 2018.
       >* For some private inventory, publishers don't pass along a device identifier, which prevents frequency tracking.

    * **[!UICONTROL Geo]**: Use this pre-populated template to see key metrics by geographic dimensions.

    * **[!UICONTROL Margin]:** Use this report to see key metrics like margin, profit, and other spend metrics by campaign or placement.

    * **[!UICONTROL Segment]:** Use this pre-populated template to see key metrics by segment.

       >[!NOTE]
       >
       >* This report is intended to show how different targeted segments perform. It uses segment membership data. When an impression is served to a person or device belonging to two or more targeted segments, this report includes one row for each segment. For this reason, totals in this report may not match actual delivery.
       >* Conversion metrics and custom goal data for segments is available after August 2, 2019. All other data for segments is available beginning after June 1, 2018.
     
    * **[!UICONTROL Site]:** By default, includes standard metrics, total media net spend, and total billable net spend by site.

## Cross-Account Reporting {#cross-account-reporting}

Any organization with multiple DSP accounts can optionally enable cross-account data in custom reports, according to the organization's needs. For example, you can give Account A access to Account B's data, and give Account B access to Account C's (but not Account A's) data. To enable and configure this feature, contact your [!DNL Adobe] account team.

Once the feature is enabled for your organization, you can [filter](report-settings.md) any of the following report types by account:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)], and [!UICONTROL Conversion].

Your account settings at [!UICONTROL Settings] > [!UICONTROL Account] indicate a) the other accounts whose data is available to your account and b) the other accounts that can access your account's data.

>[!MORELIKETHIS]
>
>* [Create a Custom Report](/help/dsp/reports/report-create.md)
>* [Custom Report Settings](/help/dsp/reports/report-settings.md)
>* [About In-Platform Reports](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Available Report Columns](/help/dsp/reports/report-columns.md)
>* [About [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
