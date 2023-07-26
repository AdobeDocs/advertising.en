---
title: '[!DNL Microsoft Advertising] conversion data'
description: Learn about the types of [!DNL Microsoft Advertising]-tracked conversion data available in in Search, Social, & Commerce.
---
# [!DNL Microsoft Advertising] conversion data in Search, Social, & Commerce

Search, Social, & Commerce automatically syncs all conversions tracked by your [Microsoft Advertising universal event tracking (UET) tags](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) for for website conversions, including view-through conversions, for reporting and optimization.

All of the metrics are automatically available in your campaign management views and basic reports, and are also available to use in portfolio objectives for optimization of Microsoft Advertising campaigns.

## Available conversion data

Search, Social, & Commerce syncs data for conversions for which the "[!DNL Include in 'Conversions']" option is enabled, pulling the data for the last 35 days and then pulling changes to the data daily by 09:00-10:00 in the advertiser's time zone. Historical data may change from day to day as new conversions are tracked for each click.

Two metrics for each [[!DNL Microsoft Advertising]-tracked conversion](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) (which you set up in [!DNL Microsoft Advertising]) are automatically available in Search, Social, & Commerce, using the conversion names configured in [!DNL Microsoft Advertising]. The metrics for each conversion include:

* `<conversion-name>` &mdash; The conversion value for the keyword (such as Purchase). 

  >[!TIP]
  >
  >Use this type of conversion metric in the objective for portfolios that include [!DNL Microsoft Advertising] campaigns with the Max Conversion Value and Target ROAS bid strategies.

* `CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "CT_" prefix (such as CT_Purchase).

  >[!TIP]
  >
  >Use this type of conversion metric in the objective for portfolios that include [!DNL Microsoft Advertising] campaigns with the Max Conversions and Target CPA bid strategies.

Data is available based on the click time and based on the conversion/transaction time from the date at which the feature is enabled for the account.

[!DNL Microsoft Advertising] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Microsoft Advertising]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.

>[!NOTE]
>
>* If you have multiple accounts with the same conversion names, you may see duplicate conversion names in Adobe Advertising. If this occurs, [change the display name](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) for one of the duplicate metrics in [!UICONTROL Admin] > [!UICONTROL Conversions]. Reporting isn't accurate when two different metrics have the same name.
>* Data at the bid unit level matches data in the ad network at the same level. However, the ad network's own conversion data for higher levels may include additional conversions that aren't attributed to the child bid units. Data in Search, Social, & Commerce is always rolled up from the bid unit level, so, for example, a campaign-level report might not have the same totals as a campaign-level report in the ad network.
>* Data variance is typically less after the morning sync than it is later in the day, when additional conversions haven't yet been synced. We recommend validating data in the morning.
>* Data isn't available at the audience or geographical location level and therefore isn't used to auto-optimize RLSA and location bid adjustments.

## How to compare conversion data in [!DNL Microsoft Advertising] with data in Search, Social, & Commerce

Use the following report settings to validate comparable data.

### Report settings to use in [!DNL Microsoft Advertising]

Generate the report for the selected conversion actions by day, and include data for all ad statuses. 

### Report settings to use in Search, Social, & Commerce

In Search, Social, & Commerce, use the view or report option to view conversions based on the click date (not the transaction date).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports]**.

1. In the toolbar above the data table, click **[!UICONTROL Create Report]**, hold the cursor over **[!UICONTROL Basic Reports]**, and then click **[!UICONTROL Search Engine Account Report]**.

1. In the [!UICONTROL Report Settings] window, specify the following report settings:
   
   1. In the **[!UICONTROL Conversions Based]** on section, select **[!UICONTROL Click date]**.
   
   1. Specify the same date range that you used for the [!DNL Microsoft Advertising] report.
   
   1. In the **[!UICONTROL Search/Content]** section, select **[!UICONTROL Search Only]**.
   
   1. In the **[!UICONTROL Search Engine Hierarchy]** section, expand the [!UICONTROL Microsoft Advertising] section and select the account.
   
   1. Open the [!UICONTROL Columns] tab, and add the [!DNL Microsoft Advertising] metrics that you want to compare.

1. Click **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Overview of implementing ad network accounts and campaigns](campaign-implemention-overview.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [View the conversion metrics tracked for an advertiser](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
