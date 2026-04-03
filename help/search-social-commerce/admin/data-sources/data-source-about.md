---
title: About syncing [!DNL Google Analytics] conversion metrics
description: Learn about syncing [!DNL Google Analytics] conversion metrics for optimization and reporting.
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/dN7AVijGEiKM1o2iu3Fcb2D61pFkTguFOOu0qIe-mZk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Search admin
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
    internal-label: Search data sources
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# About syncing [!DNL Google Analytics] conversion metrics

Search, Social, & Commerce can sync conversion metrics for a specific [!DNL Google Analytics] account, property, and view combination for optimization and reporting. [Page views](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=page_tracking&jump=ga_pageviews), [Sessions](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessions), [Bounce Rate](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_bouncerate) (calculated as bounces/sessions), and [Session Duration](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&group=session&jump=ga_sessionduration) are automatically included. You can include up to 16 additional metrics per data source.

>[!NOTE]
>
>Advertising DSP users can use the conversion metrics as custom goals and in reports.

All API usage for the data transfers is assessed to a project in the applicable [!DNL Google Analytics] account. You can view your quotas for this project in [the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). See [!DNL Google Analytics] documentation for more information about [quotas and call limits for reporting API requests](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

The following steps outline the process for syncing conversion data from [!DNL Google Analytics].

1. [Perform the prerequisite tasks](data-source-prerequisites.md)
   
   * Implement an Adobe Advertising token (`ef_id` query string parameter) in the landing page URLs for all applicable advertising accounts.
   
   * Capture the Adobe Advertising token (`ef_id` query string parameter) in a [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Agency account administrator, agency account manager, [!DNL Adobe] account manager, and administrator users only) [Create one data source per [!DNL Google Analytics] account, property, and view combination](data-source-configure.md).
   
   To integrate metrics for multiple properties or for multiple views for a single property, set up a separate data source for each.
   
   Once a data source is configured, Search, Social, & Commerce pulls data daily, beginning at 05:00 in the advertiser's time zone. Once the metrics are available, you can include them in campaign and portfolio management views and in reports, and use them in optimization objectives, as needed.

>[!MORELIKETHIS]
>
>* [Prerequisites for configuring a [!DNL Google Analytics] data source](data-source-prerequisites.md)
>* [Configure a [!DNL Google Analytics] view as a data source](data-source-configure.md)
>* [Edit a [!DNL Google Analytics] data source](data-source-edit.md)
>* [Pause syncing of a data source](data-source-pause.md)
>* [Reauthenticate a [!DNL Google Analytics] data source](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] data source settings](data-source-settings.md)
>* [Appendix - Available [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
