---
title: Manage an advertiser's conversion metrics in DSP.
description: Learn how you can use the conversion metrics that Adobe Advertising tracks for a DSP advertiser.
feature: Conversions
---
# Manage an advertiser's conversion metrics

An advertiser's conversion metrics are used throughout Adobe Advertising:

* In Advertising DSP, you can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use an advertiser's conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

* (Advertisers with Advertising Search, Social, & Commerce) In Search, Social, & Commerce, data for the conversion metrics can be displayed in columns in campaign, portfolio, and objective management views and in reports. Users with sufficient access privileges can also use conversion metrics to create objectives, which are used to optimize portfolios.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

The types of metrics tracked for DSP users include:

* Conversion metrics that Adobe Advertising tracks for an advertiser.

* [Conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Conversions from custom feeds.

From the list of conversion metrics that are available, each user with access to the advertiser's data can customize the metrics they see available for management views and reports, including or omitting specific metrics as they choose. You can either use a metric name exactly as it is spelled in the retrieved data or change the name that's shown in column headings for readability.

>[!IMPORTANT]
>
>By default, none of an advertiser's conversion metrics are available for inclusion in campaign management views, custom objectives, and custom reports. To make a conversion metric available, you must explicitly make it available.

>[!TIP]
>
>Once the advertiser (or the ad network) stops collecting a conversion metric, [hide it from management views and reports](#conversion-metrics-change-available) unless you want to use it for viewing historical data.

## View the conversion metrics tracked for an advertiser

* In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions Beta]**.

All conversion metrics that have been gathered for the advertiser, and any different display names assigned to them, are listed. Each metric row includes the source of the metric.

## Change the display name for a conversion metric

For example, if you collect registration data using a conversion metric named *reg*, then you can optionally change the display name to see it displayed as "Registrations."

You can't delete an existing display name.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions Beta]**.

1. Hold the cursor over the row and click **[!UICONTROL Edit Display Name]**.

1. Enter the name that should be displayed, and then click **[!UICONTROL Save]**.
   
   Display names must be unique and can't include the following special characters: `\"<'>&`

## Change the conversion metrics available in campaign management views, custom objectives, and custom reports {#change-the-conversion-metrics-available-in-ui}

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions]**.

   All conversion metrics that have been gathered for the advertiser, and any different names that have been specified for display, are listed.

1. (Optional) Filter the list:

   1. Above the list, click ![Filter](/help/dsp/assets/filter.png "Filter").
   
   1. Specify the filters, and then click **[!DNL Apply]**.
   
      You can filter the metrics by the AMO Client ID, by whether the metrics are visible or hidden in the UI, and by data source.
     
1. Change the conversion metrics available for management views and reports:

   * To show a metric, hold the cursor over the row and click **[!UICONTROL Show in UI and Reports]**.
   
   * To hide a metric, hold the cursor over the row and click **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Manage your campaign data views](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Manage custom objectives](/help/dsp/admin/custom-objectives-manage.md)
