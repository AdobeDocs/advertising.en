---
title: '[!DNL Google Ads] conversion data'
description: Learn about the types of [!DNL Google Ads]-tracked conversion data available in in Search, Social, & Commerce.
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management
---
# [!DNL Google Ads] conversion data in Search, Social, & Commerce

Search, Social, & Commerce automatically syncs [!DNL Google Ads]-tracked conversion data for all of your campaigns on the [!DNL Google Ads] search and shopping networks into Search, Social, & Commerce for reporting and optimization.

All of the metrics are automatically available in your campaign management views and basic reports, and are also available to use in portfolio objectives for optimization.

## Available conversion data

Search, Social, & Commerce syncs data for conversions for which the "[!DNL Include in 'Conversions']" option is enabled, pulling the data for the last 35 days and then pulling changes to the data daily by 09:00-10:00 in the advertiser's time zone. Historical data may change from day to day as new conversions are tracked for each click.

Up to three metrics for each [[!DNL Google Ads]-tracked conversion](https://support.google.com/google-ads/answer/4677036) (which you set up in [!DNL Google Ads]) are automatically available in Search, Social, & Commerce, using the conversion names configured in [!DNL Google Ads]. The metrics for each conversion include:

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

* `GGL_CT*` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `GGL_XD_CT*` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

[!DNL Google Ads] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Google Ads]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.

>[!NOTE]
>
>* If you have multiple accounts with the same conversion names, then you may see duplicate conversion names in Adobe Advertising. If this occurs, [change the display name](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md for one of the duplicate metrics in [!UICONTROL Admin] > [!UICONTROL Conversions]. Reporting isn't accurate when two different metrics have the same name.
>* Data at the bid unit level matches data in [!DNL Google Ads] at the same level. However, [!DNL Google Ads]' own conversion data for higher levels may include additional conversions that aren't attributed to the child bid units. Data in Search, Social, & Commerce is always rolled up from the bid unit level, so, for example, a campaign-level report might not have the same totals as a campaign-level report in Google Ads.
>* Data variance is typically less after the morning sync than it is later in the day, when additional conversions haven't yet been synced. We recommend validating data in the morning.
>* Conversion data isn't available for [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App], and [!DNL YouTube] ads. Filter out those types of ads when you compare data in [!DNL Google Ads] with data in Search, Social, & Commerce.
>* Data for [!DNL Google Ads] conversions isn't available at the audience or geographical location level and therefore isn't used to auto-optimize RLSA and location bid adjustments.

## How to compare conversion data in [!DNL Google Ads] with data in Search, Social, & Commerce

If you compare data in Search, Social, & Commerce with that in [!DNL Google Ads], use the view or report option to view conversions based on the click date (not the transaction date).

Use the following report settings to validate comparable data.

### Report settings to use in [!DNL Google Ads]

Generate the report for the selected conversion actions by day, and include data for all ad statuses. 

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### Report settings to use in Search, Social, & Commerce

In Search, Social, & Commerce, use the view or report option to view conversions based on the click date (not the transaction date).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]**.

1. In the toolbar above the data table, click **[!UICONTROL Create Report]**, hold the cursor over **[!UICONTROL Basic Reports]**, and then click **[!UICONTROL Search Engine Account Report]**.

1. In the [!UICONTROL Report Settings] window, specify the following report settings:
   
   1. In the **[!UICONTROL Conversions Based]** on section, select **[!UICONTROL Click date]**.
   
   1. Specify the same date range that you used for the [!DNL Google Ads] report.
   
   1. In the **[!UICONTROL Search/Content]** section, select **[!UICONTROL Search Only]**.
   
   1. In the **[!UICONTROL Search Engine Hierarchy]** section, expand the [!UICONTROL Google Adwords] section and select the account.
   
   1. Open the [!UICONTROL Columns] tab, and add the [!DNL Google Ads] metrics (beginning with "GGL") that you want to compare.

1. Click **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Overview of implementing ad network accounts and campaigns](campaign-implemention-overview.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [View the conversion metrics tracked for an advertiser](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [Create a conversion tag for [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
