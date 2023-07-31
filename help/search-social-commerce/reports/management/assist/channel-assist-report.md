---
title: '[!UICONTROL Channel Assist Report]'
description: Learn about the [!UICONTROL Channel Assist Report].
exl-id: 49616327-72e9-49c6-90b9-91c7486e8417
---
# The [!UICONTROL Channel Assist Report]

*Advertisers with Search, Social, & Commerce click tracking and with conversion tracking from Adobe Advertising, Adobe Analytics (with an [!DNL Analytics] integration), or provided in feeds using a token (`ef_id`) only*

The [!UICONTROL Channel Assist Report] indicate how various marketing channels (search or social from Search, Social, & Commerce; or display or video from Advertising DSP) have assisted the conversion process. The report shows how each pattern of event types that led to one or more conversions has contributed to your overall conversions. For example, you would see how many conversions occurred when users first saw a display ad impression, then clicked a search ad, and then
placed an order; or you can see how many conversions occurred after users interacted with more than 10 ads. Event types include search clicks, display impressions and clicks, video impressions and clicks, and other impressions and other clicks. <!-- [DSP metrics may show up as "Other Path Length (<length>)" or empty; we're supposed to fill in more values for DSP at some point.] -->

The report results include aggregated data for each pattern of event types in the conversion path &mdash; up to the N earliest event types &mdash; that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). For example, if you select a path size of five (5), then the report includes conversion paths that included up to the five earliest events, with one row for each pattern of event types tracked (such as "search click" and then "display impression"). Each row shows one pattern of events, including the first event in the path and the last event that resulted in conversions (even if the last event is outside the specified path size.) By default, the rows are in ascending order by the number of events in the path.

You optionally can include aggregate conversion data for each row. When you include conversions/revenue columns in the report, each conversion type is represented in four columns, showing a) the total number of conversions, b) the percentage of your overall conversions that were attributed to that event pattern, c) the average latency in day from the first event to a conversion, and d) the average latency in days from the last event to a conversion. When the conversion path includes more events than the specified path size, the report includes additional rows aggregating data for conversions resulting from the higher numbers of events (such as all patterns that included six event types).

You can view data for the previous 18 months.

## Available columns

The following are the columns that are available for each report. The default columns are automatically included by default. You can add the available custom columns from the Columns section of the report settings.

| Column | Default? | Description |
| ---- | ---- | ---- |
| [!UICONTROL 1st Event] to [!UICONTROL 5th Event] | Default | The five earliest event types in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Path Size] | Default | The number of event types in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Event Type] | Default | The event type of the first (earliest) event in the conversion path. |
| [!UICONTROL Last Event Type] | Default | The event type of the last event that resulted in conversions (even if the last event is outside the specified path size). |
| \[Advertiser-specific custom (derived) metrics\] | Custom | The value for a custom metric you've created that’s calculated from existing metrics. |
| \[Advertiser-specific conversion metrics\] | Custom | The number of conversions for a specified conversion metric or site engagement metric. |
| [!UICONTROL % of Total] \[conversion metric\] | Automatic | (Not available in report settings but automatically included in report output for each conversion metric included) The percentage of your overall conversions across portfolios that were attributed to the event pattern. |
| [!UICONTROL 6th Event] to [!UICONTROL 30th Event] | Custom | The sixth through 30th event types in the conversion path that occurred within the advertiser's [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL Avg. Conv. Latency (First Channel To Conversion)] \[conversion metric\] | Automatic | (Not available in report settings but automatically included in report output for each conversion metric included) The average latency in days from the first event to a conversion. |
| [!UICONTROL Avg. Conv. Latency (Last Channel To Conversion)] \[conversion metric\] | Automatic | (Not available in report settings but automatically included in report output) The average latency in days from the last event to a conversion. |
| [!UICONTROL Path Frequency] | Custom | The number of times that the path for this row occurred before conversion. |

>[!MORELIKETHIS]
>
>* [About assist reports](assist-report-about.md)
>* [The [!UICONTROL Campaign Assist Report]](campaign-assist-report.md)
>* [The [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Assist report settings](assist-report-settings.md)
>* [Generate an assist report](assist-report-generate.md)
