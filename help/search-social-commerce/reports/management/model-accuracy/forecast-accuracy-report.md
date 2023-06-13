---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Learn about the Forecast Accuracy Report, including the data columns.
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
---
# The [!UICONTROL Forecast Accuracy Report]

The report shows the accuracy of the cost and revenue models by day for specified portfolios. By default, it includes the daily predicted and actual revenue, cost, and clicks &mdash; and the accuracy of the forecasts &mdash; for each portfolio. It includes data from campaigns that are currently mapped to the portfolios.

You can view data for the previous 18 months.

>[!NOTE]
>
>* This report provides the same data as the portfolio-level [!UICONTROL Model Accuracy Report] except that you can run it across multiple portfolios and you can change the attribution rule. You can also run and schedule the report using custom parameters, and you can use it to create spreadsheet feeds.
>
>* The best practice is to view the [!UICONTROL Forecast Accuracy Report] for at least the last seven days because, regardless of the portfolio's spend strategy, most portfolios see an inherent day-of-the-week trend. The optimization capability takes this trend into consideration and allocates spend accordingly.
>
>* For cost forecasts, a deviation of 10% in the last seven days is considered acceptable, so actual spend that is between 90% and 110% of the forecasted spend is fine. For revenue forecasts, a 15% deviation in the last seven days is considered acceptable, so actual revenue that is between 85% and 115% of the forecasted spend is fine. Forecasts with higher deviations should be investigated.
>
>* When keywords in the portfolio are associated with bid shift constraints, the portfolio over- or under-spends by the total amount caused by the bid shift. As a result, the predicted cost columns deviate from the target spend by the increased or decreased spend.

## Available columns

The following are the columns that are available for each report. The default columns are automatically included by default. You can add the available custom columns from the [!UICONTROL Columns] section of the report settings.

| Column | Default? | Description |
|----|----|----|
| [!UICONTROL Portfolio] | Default | The portfolio. |
| [!UICONTROL Day of Week] | Default | The day of the week reported: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, or <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Default | The first day reported. |
| [!UICONTROL End Date] | Default | The last day reported. |
| [!UICONTROL Predicted Revenue] | Default | The predicted revenue for the portfolio. |
| [!UICONTROL Revenue] | Default | The actual revenue for the portfolio. |
| [!UICONTROL Revenue Accuracy] | Default | The accuracy of the revenue forecast, expressed as a percentage. |
| [!UICONTROL Predicted Cost] | Default | The predicted cost for the portfolio. |
| [!UICONTROL Cost] | Default | The actual cost for the portfolio. |
| [!UICONTROL Cost Accuracy] | Default | The accuracy of the cost forecast, expressed as a percentage. |
| [!UICONTROL Predicted Clicks] | Default | The number of clicks predicted for the portfolio. |
| [!UICONTROL Clicks] | Default | The actual number of clicks for the portfolio. |
| [!UICONTROL Click Accuracy] | Default | The accuracy of  the click forecast, expressed as a percentage. |
| [!UICONTROL EF Portfolio Group ID] | Default | The numeric ID for the portfolio group to which the portfolio belongs. |
| [!UICONTROL Portfolio Group Name] | Default | The name of the portfolio group to which the portfolio belongs. |
| [!UICONTROL Portfolio ID] | Default | The numeric portfolio ID. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [About model accuracy reports](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [The [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Generate a model accuracy report](model-accuracy-report-generate.md)
>* [Model accuracy report settings](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
