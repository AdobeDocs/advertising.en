---
title: Manage an advertiser's conversion metrics in DSP.
description: Learn how you can use the conversion metrics that Adobe Advertising tracks for a DSP advertiser.
feature: Conversions
---
# Manage an advertiser's conversion metrics

<!-- EDIT ALL, including metatdata -- FROM SSC help -->

*Beta feature*

The conversion metrics that Adobe Advertising tracks for an advertiser, including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), are used throughout Advertising DSP. You can use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available and include a display name, which is the name that is shown. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

## View the conversion metrics tracked for an advertiser

You can view a list of all conversion metrics that Adobe Advertising has tracked for an advertiser. Each metric row includes the source of the metric.

* In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions Beta]**.

All conversion metrics that have been gathered for the advertiser, and any different display names assigned to them, are listed.

>[!TIP]
>
>Once the advertiser stops collecting a conversion metric, [hide it from campaign management views and reports](#change-the-conversion-metrics-available-in-ui) unless you want to use it for viewing historical data.

## Change the conversion metrics available in campaign management views and reports {#change-the-conversion-metrics-available-in-ui}

When Adobe Advertising tracks a conversion metric for an advertiser, it's initially excluded from campaign management views, custom objectives, and reports. To make a conversion metric visible, you must explicitly make it available, and then optionally change the default display name, which is the name that's shown in DSP.

Similarly, you can hide a conversion metric from campaign management views, custom objectives, and reports. When you hide a conversion metric that previously was visible, it's removed from any derived metrics that contain the conversion metric.

From the list of conversion metrics that are available, each user with access to the advertiser's data can customize the metrics they see for management views and reports, including or omitting specific metrics as they choose.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions Beta]**.

   All conversion metrics that have been gathered for the advertiser, and any different names that have been specified for display, are listed.

1. (Optional) Filter the list:

   1. Above the list, click ![Filter](/help/dsp/assets/filter.png "Filter").
   
   1. Specify the filters, and then click **[!DNL Apply]**.
   
      You can filter the metrics by the AMO Client ID, by whether the metrics are visible or hidden in the UI, and by data source.
     
1. Change the conversion metrics available for management views and reports:

   * To show a metric, hold the cursor over the row and click **[!UICONTROL Show in UI and Reports]**.
   
   * To hide a metric, hold the cursor over the row and click **[!UICONTROL Hide in UI and Reports]**.
   
>[!NOTE]
>
>If Adobe Advertising collects data for new conversion metrics, then the new metrics are automatically excluded from management views and reports until you include them.

## Change the display name for a conversion metric

You can optionally change the name that is shown in column headings for readability when a conversion is available for campaign management views, custom objectives, and in reports. For example, if you collect registration data using a conversion metric named *reg*, then you can optionally change the display name to see it displayed as "Registrations."

You can't delete an existing display name.

<!-- Is this note relevant? -->

>[!NOTE]
>
>For [metrics from Google Analytics](/help/search-social-commerce/admin/data-sources/data-source-about.md), any manual changes to the display name are overwritten if you update or reauthenticate the integration. Similarly, any name changes within Google Analytics are ignored unless you [update](/help/search-social-commerce/admin/data-sources/data-source-edit.md) or [reauthenticate](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) the integration.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Conversions Beta]**.

1. Hold the cursor over the row and click **[!UICONTROL Edit Display Name]**.

1. Enter the name that should be displayed, and then click **[!UICONTROL Save]**.
   
   Display names must be unique and can't include the following special characters: `\"<'>&`

>[!MORELIKETHIS]
>
>* [Manage Your Campaign Data Views](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Manage Custom Objectives](/help/dsp/admin/custom-objectives-manage.md)
