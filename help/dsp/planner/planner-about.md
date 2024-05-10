---
title: About the DSP Planner Tool
description: Learn about the planner tool to forecast the unique reach for connected TV (CTV) placements according to specified budget and targeting criteria.
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
---
# About the DSP Planner Tool

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta feature*

The planner tool helps you to forecast the household-level unique reach of connected TV (CTV) placements according to specified budget and targeting criteria before you begin spending on inventory. After you evaluate multiple reach plans, you can implement the plan that best aligns with the desired outcomes in your packages and placements.

The planner tool uses historical bid, impression, and reach data from the last 90 days to estimate the unique reach, average CPM, average frequency, and impressions for a plan configuration.

## Planner forecast

Each forecast consists of a reach-budget forecast curve that shows the amount of reach achievable with the plan settings. Move the cursor over the visualization to see incremental reach opportunities with higher budgets.

![Planner forecast](/help/dsp/assets/planner-forecast.png "Planner forecast")

The forecast output also includes an [!UICONTROL Inventory Breakdown] section that shows how different publishers contribute to unique reach, offering valuable discovery opportunities.

>[!NOTE]
>
>* The [!UICONTROL Inventory Breakdown] section displays data for only private and [!UICONTROL On Demand] inventory.
>* The estimated unique reach shown for two publishers can be overlapping.

## The Planner View

In the [!UICONTROL Planner] view, you can view your existing CTV reach plans and create new ones.

You can also edit, duplicate, export, archive, or regenerate the forecast for any plan.

## FAQs

+++What types of inventory does the planner tool support?

The planner tool supports all types of inventory, including programmatic guaranteed (PG), private marketplace (PMP), [!UICONTROL On Demand], and public. To generate accurate forecasts, include deals with at least 50,000 impressions in the last seven days.

+++

+++Why am I seeing "[!UICONTROL Unable to generate forecast]?"

One of the most common reasons for this error is an insufficient budget or maximum bid. For best results, use a minimum budget of 5000 USD. If the [!UICONTROL Connected TV] media type is selected, enter a maximum bid of at least 10 USD.

Also, ensure that the included publishers or deals are active and have recent impression activity.

+++

+++I built a placement based on the forecast, but it didn't achieve the amount of unique reach indicated by the reach forecast. Why? 

The reach forecast is only an estimate, and actual results are expected to vary because of multiple factors that change frequently, such as seasonality, bid competitiveness, and supply & demand. It's not expected be fully accurate but is most useful for directional insights into campaign strategies that can potentially drive the best outcomes. 

+++

+++Can the planner generate different forecast results with the same input settings?

The planner generates forecasts based on the latest observed data, so the forecasted output might vary at different times even though the plan settings remain the same. Consider generating multiple forecasts for the same plan and exporting the results for each.

+++

+++Can I save the planner forecast output?

Yes, you can export a forecast into a [!DNL Microsoft Excel] spreadsheet by clicking **[!UICONTROL ...]** > **[!UICONTROL Export]** in the upper right. The spreadsheet captures the information displayed in the reach budget curve using two data columns: [!UICONTROL Budget] and [!UICONTROL Reach].

>[!MORELIKETHIS]
>
>* [About the DSP Planner Tool](planner-about.md)
>* [Create a Connected TV Reach Plan](planner-create.md)
>* [Duplicate a Connected TV Reach Plan](planner-duplicate.md)
>* [Edit a Connected TV Reach Plan](planner-edit.md)
>* [Export a Connected TV Reach Plan](planner-export.md)
>* [Regenerate the Forecast for a Connected TV Reach Plan](planner-forecast.md)
>* [Archive a Connected TV Reach Plan](planner-archive.md)
>* [Settings for Connected TV Reach Plans](planner-settings.md)
