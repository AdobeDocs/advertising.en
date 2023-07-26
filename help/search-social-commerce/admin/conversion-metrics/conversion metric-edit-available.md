---
title: Change the conversion metrics available in management views and reports
description: Learn how to make conversion metrics available in your management views and reports.
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
---
# Change the conversion metrics available in management views and reports

When Adobe Advertising tracks a [conversion](/help/search-social-commerce/glossary.md#c-d) metric for an advertiser, it's initially excluded from portfolio objectives, reports, and management views. To make a conversion metric visible, you must explicitly make it available, and then optionally change the default display name, which is the name that's shown. The only exception is that conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags are automatically available and visible.

Similarly, you can hide a conversion metric from portfolio objectives, reports, and management views. When you hide a conversion metric that previously was visible, it's removed from any derived metrics that contain the conversion metric.

From the list of conversion metrics that are available, each user with access to the advertiser's data can customize the metrics they see for management views and reports, including or omitting specific metrics as they choose.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]**.

   All conversion metrics that have been gathered for the advertiser, and any different names that have been specified for display, are listed.

1. (Optional) Filter the list:

   * To search for a specific metric name or display name, click ![Search](/help/search-social-commerce/assets/search.png "Search"), enter the word or string in the input field, and then press the **[!DNL Enter]** key.
   
     You can search for strings that appear anywhere within the phrase (such as the first letter or the last three letters), and the search terms aren't [case-sensitive](/help/search-social-commerce/glossary.md#c-d).
     
   * To search for conversion metrics by their availability in management views and reports, click ![Filter](/help/search-social-commerce/assets/filter.png "Filter"), and select the filter **[!UICONTROL Show in UI and Reports]**. Then select either **[!UICONTROL Show]** (to view the conversion metrics available to include in reports and management views) or **[!UICONTROL Hide]** (to view the conversion metrics not available in reports and management views).

1. Change the conversion metrics available for management views and reports:

   * To show or hide a single metric, click the switch in the **[!UICONTROL Show in UI and Reports]** column to change the setting.
   
   * To show or hide multiple metrics, do the following:
   
     1. Select the check box next to each conversion metric.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

     1. In the toolbar above the data table, click ![Show](/help/search-social-commerce/assets/show.png "Show") to show the metrics or ![Hide](/help/search-social-commerce/assets/hide.png "Hide") to hide the metrics.
     
     1. (To hide metrics) In the confirmation message, click **[!UICONTROL Yes]** to hide the metrics, including removing them from any derived metrics that contain the metrics.

1. (Optional) [Change the name that appears in column headings](conversion metric-edit-display-name.md) for any of the conversion metrics.

   The default display name for each visible conversion metric is the metric name as it's spelled in the retrieved data.

>[!NOTE]
>
>If Adobe Advertising collects data for new conversion metrics, then the new metrics &mdash; except for conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags &mdash; are automatically excluded from management views and reports until you include them. New conversions tracked by [!DNL Google Ads], [!DNL Google Analytics], and [!DNL Microsoft® Advertising] universal event tracking tags are always automatically available.

>[!MORELIKETHIS]
>
>* [About managing an advertiser's conversion metrics](conversion metric-about.md)
>* [View the conversion metrics tracked for an advertiser](conversion metric-view-tracked.md)
>* [Change the display name for a conversion metric](conversion metric-edit-display-name.md)
