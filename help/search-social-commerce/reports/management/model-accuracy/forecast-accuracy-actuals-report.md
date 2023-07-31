---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Learn about the [!UICONTROL Forecast Accuracy (Actuals) Report], including the data columns.
exl-id: ff49284a-2d13-48bf-a172-3bd461db7a3c
---
# The [!UICONTROL Forecast Accuracy (Actuals) Report]

This report shows the actual impression, click, cost, and revenue data from the ad network by day for each portfolio.

## Available columns

The following are the columns that are automatically included in each report. You can't add additional columns.

| Column | Default? | Description |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Default | The name of the portfolio group to which the portfolio belongs. |
| [!UICONTROL Portfolio ID] | Default | The numeric portfolio ID. |
| [!UICONTROL EF Portfolio Group ID] | Default | The numeric ID for the portfolio group to which the portfolio belongs. |
| [!UICONTROL Portfolio] | Default | The portfolio. |
| [!UICONTROL Portfolio Status] | Default | The portfolio status:<ul><li><i>[!UICONTROL Optimize]:</i> The optimization capability is gathering click and revenue data for the relevant campaigns, modeling the data to optimize bids, and optimizing bids and/or campaign budgets (depending on the optimization type and the campaign bid strategies).</li><li><i>[!UICONTROL Active]:</i> The optimization capability is gathering click and revenue data for the relevant campaigns and is modeling the data, but it isn't optimizing bids or campaign budgets.</li><li><i>[!UICONTROL Inactive]:</i> The optimization capability is gathering click data for the relevant campaigns for reporting purposes, but it's not modeling the data nor optimizing bids or campaign budgets. |
| [!UICONTROL Day of Week] | Default | The day of the week reported: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, or <i>[!UICONTROL Saturday]</i>.  |
| [!UICONTROL Event Date] | Default | The date reported. |
| [!UICONTROL Device] | Default |(Google Ads, Microsoft® Advertising, Yahoo! Display Network, Yahoo! Japan Ads, and Yahoo Native campaigns) The device type on which ads were displayed: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, or <i>[!UICONTROL N/A]</i> (no value). Rows for other ad networks have values of <i>[!UICONTROL N/A]</i>.<br><br>In search campaigns, if the tracking templates or destination URLs for the keywords, ads, and/or ad extensions included parameters to track data by device (<code>&ev_dvc={device}&ev_dvm={devicemodel}</code>) at the time the ad was clicked, then conversion data is also included in the row for each device type. Otherwise, if conversion data can't be attributed to a device type, it's aggregated in a separate row with a "[!UICONTROL Device]" value of <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Default | The total revenue. |
| [!UICONTROL Impressions] | Default | The total impressions. |
| [!UICONTROL Clicks] | Default | The total clicks. |
| [!UICONTROL Cost] | Default | The total cost. |

>[!MORELIKETHIS]
>
>* [About model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Generate a model accuracy report](model-accuracy-report-generate.md)
>* [Model accuracy report settings](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
