---
title: '[!UICONTROL Campaign Assist Report]'
description: Learn about the [!UICONTROL Campaign Assist Report].
exl-id: 7fbc9c17-c77d-485b-8d51-5e5a153d7a2b
---
# The [!UICONTROL Campaign Assist Report]

*Advertisers with Search, Social, & Commerce click tracking and with conversion tracking from Adobe Advertising, Adobe Analytics (with an [!DNL Analytics] integration), or provided in feeds using a token (`ef_id`) only*

The [!UICONTROL Campaign Assist Report] indicates which campaigns have assisted the conversion process. The reports how each pattern of campaigns whose ads led to one or more conversions has contributed to your overall conversions. For example, you can see how many conversions occurred when users first saw an ad from Campaign A, then clicked an ad from Campaign B, and then placed an order. Similarly, you can see how many conversions occurred after users interacted with ads from more than 10 campaigns.

The report results include aggregated data for each pattern of campaigns in the conversion path &mdash; up to the N earliest campaigns &mdash; for events that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). For example, if you select a path size of five (5), then the report includes conversion paths that included up to the five earliest campaigns, with one row for each pattern of campaigns whose events were tracked. Each row shows one pattern of campaigns, including the first campaign in the path and the last campaign that resulted in conversions (even if the last campaign is outside the specified path size.) By default, the rows are in ascending order by the number of campaigns in the path.

You optionally can include aggregate conversion data, including your custom metrics, for each row. When you include conversions/revenue columns in the report, then each conversion type is represented in four columns, showing a) the total number of conversions, b) the percentage of your overall conversions that were attributed to that campaign pattern, c)  the average latency in days from the first event (in the first campaign) to a conversion, and d) the average latency in days from the last event (in the last campaign) to a conversion. When the conversion path includes more campaigns than the specified path size, then the report includes additional rows aggregating data for conversions resulting from the higher numbers of campaigns (such as all patterns that included six campaigns).

You can also optionally include the ad network and/or the event type after the campaign name, such as `<campaign name> (Google) click`.

You can view data for the previous 18 months.

>[!TIP]
>
>If your brand keywords are in a different campaign than your generic keywords, then the report indicates whether your brand keywords contribute to conversions.

## Available columns

The following are the columns that are available for each report. The default columns are automatically included by default. You can add the available custom columns from the Columns section of the report settings.

| Column | Default? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] to [!UICONTROL 5th Campaign] | Default | The five earliest  campaigns in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j).<br><br>If you included any of the report options to indicate the ad network, account name, or event type after the entity name, then that information is included after the campaign name (such as `"<"campaign name> [Google] [Account1] [impression]`"). |
| [!UICONTROL Path Size] | Default | The number of campaigns in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Default | The first campaign in the conversion path. |
| [!UICONTROL Last Campaign] | Default | The last campaign that resulted in conversions (even if the last keyword is outside of the specified path size.)<br><br>If you included any of the report options to indicate the ad network, account name, or event type after the entity name, then that information is included after the campaign name (such as `"<"campaign name> [Google] [Account1] [impression]`"). |
| \[Advertiser-specific custom (derived) metrics\] | Custom | The value for a custom metric you've created that’s calculated from existing metrics. |
| \[Advertiser-specific transaction properties\] | Custom | The number of conversions for a specified transaction property or site engagement metric. |
| [!UICONTROL % of Total] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output for each transaction property included) The number of conversions for a specified transaction property that resulted from the campaign pattern. |
| [!UICONTROL 6th Campaign] to [!UICONTROL 20th Campaign] | Custom | The sixth through 20th campaigns in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j).<br><br>If you included any of the report options to indicate the ad network, account name, or event type after the entity name, then that information is included after the campaign name (such as `"<"campaign name> [Baidu] [Account1] [click]`"). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output for each transaction property included) The average latency in days from the first event (in the first campaign) to a conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output) The average latency in days from the last event (in the last campaign) to a conversion. |
| [!UICONTROL EF Campaign ID] | Custom | The numeric ID that Search, Social, & Commerce assigns to the campaign. |
| [!UICONTROL EF Portfolio Group ID] | Custom | The numeric ID for the portfolio group to which the portfolio belongs. |
| [!UICONTROL EF Search Engine ID] | Custom | The numeric ID that Search, Social, & Commerce assigns to the ad network: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (deprecated), or <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (deprecated). |
| [!UICONTROL Portfolio ID] | The numeric portfolio ID. |
| [!UICONTROL User SE Account ID] | The numeric ID that Search, Social, & Commerce assigns to the ad network. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [About assist reports](assist-report-about.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Assist report settings](assist-report-settings.md)
>* [Generate an assist report](assist-report-generate.md)
