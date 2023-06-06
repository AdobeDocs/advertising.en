---
title: Custom metric settings
description: Reference the settings for custom metrics, which are calculated from standard metrics. 
---
# Custom metric settings

Custom metric settings are slightly different in different parts of the interface. 

## Custom metric settings in campaign management views

| Parameter/Section | Description |
|----|----|
| Custom Metric Name | The name of the metric, which appears as the column name. <b>Tip:</b> Use a meaningful metric name, but consider that longer names make the column wider. |
| Insert Metric | The mathematical formula used to calculate the new metric (such as [Cost]/[Registrations]:<ul><li>To insert a metric from the list of traffic and revenue metrics, place your cursor where you want to insert the metric, and then either select the metric from the list or enter it manually and enclosed in brackets (for example, `[CPC]`).</li><li>To insert an operator, place your cursor where you want to insert the operator, and then either click the button or enter the symbol manually. The available mathematical operators: `+ - * / ( ) ()`</li></ul><b>Note:</b> Complex custom metrics take longer to calculate, and reports and views that include them &mdash; especially when they include separate columns for click-through and view-through conversions &mdash; take longer to generate. |
| Format | How to present the data for this metric: *[!UICONTROL Currency]* (a monetary value), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, or *[!UICONTROL Percentage]* (a percentage with two decimal points).<br><br><b>Caution:</b> If you create a derived metric with the format [!UICONTROL Number w/out Decimal Points] (which shows data as integers) and include it in a view or a report that uses a weighted conversion attribution rule ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], or [!UICONTROL Even Distribution]), then the output is shown in integers, not decimals. As a result, individual data fields may be incorrect, even though the totals are correct. For example, if an order is divided evenly between three events, then one order (rather than 0.33 order) is attributed to each of the three events. To prevent the issue, use the metric format [!UICONTROL Number to 2 Decimal Points]. |
 
## Custom metric settings in reports and report templates and in the [!UICONTROL Portfolios] views

| Parameter/Section | Description |
|----|----|
| Custom Metric Name | The name of the metric, which appears as the column name. <b>Tip:</b> Use a meaningful metric name, but consider that longer names make the column wider. |
| Format | How to present the data for this metric: *[!UICONTROL Currency]* (a monetary value), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, or *[!UICONTROL Percentage]* (a percentage with two decimal points).<br><br><b>Caution:</b> If you create a derived metric with the format [!UICONTROL Number w/out Decimal Points] (which shows data as integers) and include it in a view or a report that uses a weighted conversion attribution rule ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], or [!UICONTROL Even Distribution]), then the output is shown in integers, not decimals. As a result, individual data fields may be incorrect, even though the totals are correct. For example, if an order is divided evenly between three events, then one order (rather than 0.33 order) is attributed to each of the three events. To prevent the issue, use the metric format [!UICONTROL Number to 2 Decimal Points]. |
| Insert Metric | A list of existing metrics from which you can create a formula.<br><br>To insert a metric in the formula input field, place your cursor where you want to insert the metric, and then either select the metric from the list or enter it manually and enclosed in brackets (for example, `[CPC]`). |
| Insert Operator | The available mathematical operators: `+ - x / ( )`<br><br>To insert an operator in the formula input field, place your cursor where you want to insert the operator, and then either click the button or enter the symbol manually. |
| [Formula input field for the metric] | The mathematical formula used to calculate the new metric based on one or more existing properties or standard metrics (such as `[Cost]/[Registrations]`. It can include any combination of metrics and operators.<br><br><b>Note:</b> Complex custom metrics take longer to calculate, and reports and views that include them &mdash; especially when they include separate columns for click-through and view-through conversions &mdash; take longer to generate. |

>[!MORELIKETHIS]
>
>* [About custom metrics](custom-metric-about.md)
>* [Create a custom metric](custom-metric-create.md)
>* [Edit a custom metric](custom-metric-edit.md)
>* [Delete a custom metric](custom-metric-delete.md)
