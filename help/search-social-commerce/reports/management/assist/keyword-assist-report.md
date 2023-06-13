---
title: '[!UICONTROL Keyword Assist Report]'
description: Learn about the [!UICONTROL Keyword Assist Report].
exl-id: 07de2880-111b-498f-9f7f-ec15f89230ae
---
# The [!UICONTROL Keyword Assist Report]

*Advertisers with Search, Social, & Commerce click tracking and with conversion tracking from Adobe Advertising, Adobe Analytics (with an [!DNL Analytics] integration), or provided in feeds using a token (`ef_id`) only*

The [!UICONTROL Keyword Assist Report] indicates which keywords or placements drive clicks. The report shows each pattern of paid search keywords or placements that received clicks in a conversion path and indicates how that pattern contributed to your overall conversions. For example, you would see how many conversions occurred when users first clicked an ad resulting from a keyword search for "leather shoes," then clicked an ad after a keyword search for "suede shoes," and then placed an order; or you can see how many conversions occurred after users clicked ads resulting from more than 10 keywords.

The report results include aggregated data for up to the N earliest paid search keyword or placement clicks in the conversion path that occurred within the advertiser's
click lookback and impression lookback windows. For example, if you select a path size of five (5), then the report consists of conversion paths that included up to the five earliest keywords or placements that received clicks, with one row for each pattern of clicks tracked. Each row includes the first keyword or placement in the path and last keyword or placement that resulted in conversions (even if the last keyword is outside the specified path size.) By default, the rows are in ascending order by the number of events in the path.

>[!NOTE]
>
>If the report includes placements from content-enabled search campaigns (which don't include keywords), then the [!UICONTROL Keyword] column shows the applicable ad group names, such "(adgroup content) Your Ad Group Name."

You optionally can include aggregate conversion data for each row. When you include conversions/revenue columns in the report, each conversion type is represented in four columns, showing a) the total number of conversions, b) the percentage of your overall conversions that were attributed to that keyword pattern, c)  the average latency in days from the first event (on the first keyword) to a conversion, and d) the average latency in days from the last event (on the last keyword) to a conversion. When the conversion path includes more keywords than the specified path size, the report includes additional rows aggregating data for conversions resulting from the higher numbers of keywords (such as all patterns that included clicks on six keywords).

You can view data for the previous 18 months.

## Available columns

The following are the columns that are available for each report. The default columns are automatically included by default. You can add the available custom columns from the Columns section of the report settings.

| Column | Default? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Keyword] to [!UICONTROL 5th Keyword] | Default | The five earliest paid search keyword or placement clicks in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Note:</b> If the report includes placements from content-enabled search campaigns (which don't include keywords), then these columns show the applicable ad group names, such "(adgroup content) Your Ad Group Name," instead. |
| [!UICONTROL Path Size] | Default | The number of keywords and/or placements in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Keyword] | Default | The first keyword or placement in the conversion path. |
| [!UICONTROL Last Keyword] | Default | The last keyword or placement that resulted in conversions (even if the last keyword is outside the specified path size.) |
| \[Advertiser-specific custom (derived) metrics\] | Custom | The value for a custom metric you've created that’s calculated from existing metrics. |
| \[Advertiser-specific transaction properties\] | Custom | The number of conversions for a specified transaction property or site engagement metric. |
| [!UICONTROL % of Total] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output for each transaction property included) The percentage of your overall conversions across portfolios that were attributed to the keyword and/or placement pattern. |
| [!UICONTROL 6th Keyword] to [!UICONTROL 10th Keyword] | Custom | The sixth through tenth paid search keyword or placement clicks in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j).<br><br><b>Note:</b> If the report includes placements from content-enabled search campaigns (which don't include keywords), then these columns show the applicable ad group names, such "(adgroup content) Your Ad Group Name," instead. |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output for each transaction property included) The average latency in days from the first event (on the first keyword or placement) to a conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[transaction property\] | Automatic | (Not available in report settings but automatically included in report output) The average latency in days from the last event (on the last keyword or placement) to a conversion. |
| [!UICONTROL Path Frequency] | Custom | The number of times that the path for this row occurred before conversion. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [About assist reports](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [Assist report settings](assist-report-settings.md)
>* [Generate an assist report](assist-report-generate.md)
