---
title: Campaign strategy plan settings
description: See descriptions of the settings for campaign strategy plans.
feature: DSP Planner
---
# Campaign strategy plan settings

*Beta feature*

| Parameter | Description | Required? |
| --- | --- | --- |
| Name | The name to identify your plan. | Yes |
| Advertiser | The specific advertiser in the account for which the plan is being created. | Yes |
| Media Type | The type of media to include in the plan.<br><br>Currently, only [!UICONTROL Connected TV] is available.| Yes |
| Date Range | The start and end dates for the plan.<br><br>The start date can't be before the current date. The date range can't be greater than 90 days. | Yes | 
| Goal Type | The type of goal (such as [!UICONTROL Budget]) to consider for the plan.<br><br>Currently, only [!UICONTROL Budget] is available. | Yes |
| Goal Value | The goal value for the forecast. For more accurate forecast results, use a value > 5000 USD. | Yes | 
| Max Bid | The maximum amount to pay for 1000 impressions. If the [!UICONTROL Connected TV] media type is selected, enter a value of at least 10 USD. | Yes |
| Frequency Cap | The number of times a unique household should be served ads.<br><br>When you implement a plan and must create multiple placements, apply the frequency cap setting at the package level, not the placement level, to ensure proper delivery. | Yes |
| Geo-Targeting | Locations to include or exclude as targets. | Yes |
| Inventory Targeting | Inventory sources to include or exclude as targets. Select at least one feed or source. | Yes |
| Audience Targeting | Audiences to include or exclude as targets. | No |
| Ad Duration | The duration of ads to consider for the plan. | No |

>[!MORELIKETHIS]
>
>* [About the DSP planner tool](planner-about.md)
>* [Create a campaign strategy plan](planner-create.md)
>* [Duplicate a campaign strategy plan](planner-duplicate.md)
>* [Edit a campaign strategy plan](planner-edit.md)
>* [Export a campaign strategy plan](planner-export.md)
>* [Regenerate the forecast for a campaign strategy plan](planner-forecast.md)
>* [Archive a campaign strategy plan](planner-archive.md)
