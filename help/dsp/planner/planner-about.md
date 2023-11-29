---
title: About the DSP planner tool
description: Learn about the planner tool to forecast the unique reach  for a campaign strategy according to specified budget and targeting criteria.
feature: 
---

*Beta feature*

# About the DSP planner tool

The planner tool helps you forecast the unique reach at the household level for a campaign strategy according to specified budget and targeting criteria before you begin spending on inventory. After you evaluate multiple plans, you can implement the plan that best aligns with the desired outcomes in your packages and placements.

The planner tool uses historical bid, impression, and reach data from the last 90 days to estimate the unique reach, average CPM, average frequency, and impressions for a plan configuration.

## Planner forecast

The forecast consists of a reach-budget forecast curve that shows the amount of reach achievable with the plan settings. Move the cursor over the visualization to see incremental reach opportunities with higher budgets.

![Planner forecast](/help/dsp/assets/planner-forecast.png "Planner forecast")

The forecast output also includes an [!UICONTROL Inventory Breakdown] section that shows how different publishers contribute to unique reach, offering valuable discovery opportunities.

>[!NOTE]
>
>* The [!UICONTROL Inventory Breakdown] section displays data for only private and [!UICONTROL On Demand] inventory.
* The estimated unique reach shown for two publishers can be overlapping.

## FAQs

+++What types of inventory does the planner tool support?

The planner tool supports all types of inventory, including programmatic guaranteed (PG), private marketplace (PMP), [!UICONTROL On Demand], and public. To generate accurate forecasts, include deals with at least 50,000 impressions in the last seven days.

+++

+++Why am I seeing "[!UICONTROL Unable to generate forecast]?"

One of the most common reasons for this error is an insufficient budget or maximum bid. For best results, use a minimum budget of 5000 USD. If the [!UICONTROL Connected TV] media type is selected, enter a maximum bid of at least 10 USD.

Also, ensure that the included publishers or deals are active and have recent impression activity.

+++

+++I built a placement based on the forecast, but it didn't achieve the amount of unique reach indicated by the reach planner. Why? 

The reach planner output is only an estimate, and actual results are expected to vary because of multiple factors &mdash; such as seasonality, bid competitiveness, and supply & demand &mdash; which change frequently. Therefore, it is not expected be fully accurate but is most useful for directional insights into campaign strategies that can potentially drive the best outcomes. 

+++

+++Can the planner generate different forecast results with the same input settings?

The planner continuously updates based on the latest observed data, so the forecasted outputs generated at different times with the same plan settings might vary. Consider saving the results.

+++

+++Can I save the planner forecast output?

Yes, you can export a forecast into a [!DNL Microsoft® Excel] spreadsheet by clicking the three dots icon (...) next to [!UICONTROL Edit Plan]. The  spreadsheet captures the information displayed in the reach budget curve using two data columns: [!UICONTROL Budget] and [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [About the DSP planner tool](planner-about.md)
>* [Create a plan](planner-create.md)
>* [Edit a plan](planner-edit.md)
>* [Plan settings](planner-settings.md)
