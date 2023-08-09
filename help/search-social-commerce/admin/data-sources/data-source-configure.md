---
title: Configure a [!DNL Google Analytics] view as a data source
description: Learn how to configure a data source from a [!DNL Google Analytics] view.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
---
# Configure a [!DNL Google Analytics] view as a data source

*Agency Administrators, Agency Account Managers, Adobe Account Managers, and Administrators Only*

You can create one data source per [!DNL Google Analytics] account, property, and view combination.

To integrate metrics for multiple properties or for multiple views for a single property, set up a separate data source for each.

1. [Perform all prerequisites to integrating the [!DNL Google Analytics] account](data-source-prerequisites.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Data Source Setup]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. In the [!UICONTROL Deployment Prerequisites] dialog, select the check box to confirm that the required custom dimension "ef_id" is implemented in the [!DNL Google Analytics] account, and then click **[!UICONTROL Continue]**.

   Some prerequisites may have been performed by other roles in your organization. If you have questions about the prerequisites, talk to your Adobe Account Team.

1. Enter the [data source settings](data-source-settings.md):

   1. In the **[!UICONTROL Connect to [!DNL Google Analytics]]** section, do the following.
      
      1. Enter the numeric ID for the [!DNL Google Analytics] account.
      
      1. Enter the email address to use to access data for this data source. The email address must be registered to a [!DNL Google] account and have "Read & Analyze" permissions for the [!DNL Google Analytics] account. See the [instructions for assigning user permissions in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >To make sure that only specific [!DNL Google Analytics] properties and views are available within Adobe Advertising, log in using an email address that has access to only those properties and views.

         >[!NOTE]
         >
         >If you later change the password for this email account, then all open connections to the email account are closed. To resume syncing data, return to this page and [reauthenticate](data-source-reauthenticate.md).

      1. Select the check box to authorize Adobe Advertising to access metrics for the account.
       
      1. Click **[!UICONTROL Authenticate]**.

   1. In the [!UICONTROL Account Details] section, specify the property and view for the metrics to import. In addition, specify the custom dimension that's populated with the value of the "ef_id" query string parameter.
   
   1. In the [!UICONTROL Import Metrics] section, specify the metrics to include in the feed(s).

      You can't remove [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], or [!UICONTROL Session Duration], which are included automatically. You can add up to 16 additional valid metrics or metrics without data.

      >[!WARNING]
      >
      >[!DNL Google Analytics] permits up to 10 metrics in a single data feed. Search, Social, & Commerce can support up to two feeds with a total of 20 metrics, but using a second feed doubles your API calls to [!DNL Google Analytics]. If you have many metrics, select only the metrics that you want to use in objectives for optimization. See more about [quotas and call limits for API requests to [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).
    
    1. In the [!UICONTROL Metric Tag] section, enter the name of the tag to append to each metric for the data source.

1. In the upper right, click **[!UICONTROL Post]**.

   The data source is named "AccountName > PropertyName > ViewName" and is automatically activated. To pause the data source, see "[Pause a Feed from a Data Source](data-source-pause.md)."

   The metrics are available the next day after completion of the daily data sync, which begins at 05:00 in the advertiser's time zone. Once the metrics are available, they're visible in [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Each new conversion metric is named "`ga:backEndMetricName_propertyID_viewID`," where "backEndMetricName" is the metric name used by the API. The display name for each new conversion metric is "`friendlyMetricName_ga:MetricTag`,"  where "friendlyMetricName" is the metric name that appears in [!DNL Google Analytics] and "MetricTag" is the [!UICONTROL Metric Tag] defined in the data source settings.

   You can add the metrics directly to campaign management and portfolio management views, reports, and optimization objectives.

>[!MORELIKETHIS]
>
>* [About syncing [!DNL Google Analytics] conversion metrics](data-source-about.md)
>* [Prerequisites for configuring a [!DNL Google Analytics] data source](data-source-prerequisites.md)
>* [Edit a [!DNL Google Analytics] data source](data-source-edit.md)
>* [Pause syncing of a data source](data-source-pause.md)
>* [Reauthenticate a [!DNL Google Analytics] data source](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] data source settings](data-source-settings.md)
>* [Appendix - Available [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
