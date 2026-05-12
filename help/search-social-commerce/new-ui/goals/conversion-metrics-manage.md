---
title: Manage an advertiser's conversion metrics
description: Learn how you can use the conversion metrics that Adobe Advertising tracks for an advertiser.
feature: Conversions
---
# Manage an advertiser's conversion metrics

An advertiser's [conversion](/help/search-social-commerce/glossary.md#c-d) metrics are used throughout Adobe Advertising:

* In Search, Social, & Commerce, data for the conversion metrics can be displayed in columns in campaign, portfolio, and objective management views and in reports. Users with sufficient access privileges can also use conversion metrics to create objectives, which are used to optimize portfolios.

* (Advertisers with Advertising DSP) In DSP, you can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

Available metrics include:

* Conversion metrics that Adobe Advertising tracks for an advertiser.

* [Conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).

* Cconversions tracked by [!DNL Google Ads] and conversions tracked by [!DNL Microsoft Advertising] universal event tracking tags.

* (When [you've configured a specific [!DNL Google Analytics] account, property, and view combination as a data source](/help/search-social-commerce/admin/data-sources/data-source-about.md) for Search, Social, & Commerce) Conversions tracked by [!DNL Google Analytics].

* Conversions from custom feeds.

From the list of conversion metrics that are available, each user with access to the advertiser's data can customize the metrics they see available for management views and reports, including or omitting specific metrics as they choose. You can either use a metric name exactly as it is spelled in the retrieved data or change the name that's shown in column headings for readability.

>[!IMPORTANT]
>
>By default, none of an advertiser's conversion metrics &mdash; except for conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft Advertising] universal event tracking tags &mdash; are available for inclusion in campaign and portfolio management views, objectives, and reports. To make a conversion metric available, you must explicitly make it available.
>
>New conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft Advertising] universal event tracking tags are always automatically available.

>[!TIP]
>
>Once the advertiser (or the ad network) stops collecting a conversion metric, [hide it from management views and reports](#conversion-metrics-change-available) unless you want to use it for viewing historical data.

## View the conversion metrics tracked for an advertiser

* In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

All conversion metrics that have been gathered for the advertiser, and any different display names assigned to them, are listed. Each metric row includes the source of the metric.

## Change the display name for a conversion metric

For example, if you collect registration data using a conversion metric named *reg*, then you can optionally change the display name to see it displayed as "Registrations."

You can't delete an existing display name.

>[!NOTE]
>
>For [metrics from [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md), any manual changes to the display name are overwritten if you update or reauthenticate the integration. Similarly, any name changes within [!DNL Google Analytics] are ignored unless you [update](/help/search-social-commerce/admin/data-sources/data-source-edit.md) or [reauthenticate](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md) the integration.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

1. Filter the list [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from a [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. In the **[!UICONTROL Conversion Display Name]** column for the metric, hold the cursor over the metric name, and click **...** > **[!UICONTROL Rename]**.

1. Enter the name that should be displayed, and then click **[!UICONTROL Apply]**.
   
   Display names must be unique and can't include the following special characters: `\"<'>&`

## Change the conversion metrics available in management views, objectives, and reports {#conversion-metrics-change-available}

>[!NOTE]
>
>When you hide a conversion metric that previously was available, it's removed from any derived metrics that contain the conversion metric.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Conversions]**.

   All conversion metrics that have been gathered for the advertiser, and any different names that have been specified for display, are listed.

1. (Optional) Filter the list [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from a [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Change the conversion metrics available for management views and reports:

   * To show or hide a single metric, click the switch in the **[!UICONTROL Visibility]** column to change the setting.
   
   * To show or hide multiple metrics, do the following:
   
     1. Select the check box next to each conversion metric.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

     1. In the bulk actions toolbar, click ![Visibility](/help/search-social-commerce/assets/visible.png "Visibility") to show the metrics or ![Visibility off](/help/search-social-commerce/assets/visibility-off.png "Visibility off") to hide the metrics.
     
     1. (To hide metrics) In the confirmation message, click **[!UICONTROL Confirm]** to hide the metrics, including removing them from any derived metrics that contain the metrics.

<!--
>[!MORELIKETHIS]
>
>* 
-->
