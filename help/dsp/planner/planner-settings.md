---
title: Settings for Connected TV Reach Plans
description: See descriptions of the settings for connected TV reach plans.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
---
# Settings for Connected TV Reach Plans

<!-- Move out of table for consistency at some point. -->

| Parameter | Description | Required? |
| --- | --- | --- |
| [!UICONTROL Name] | The name to identify your plan. | Yes |
| [!UICONTROL Advertiser] | The specific advertiser in the account for which the plan is being created. | Yes |
| [!UICONTROL Media Type] | The type of media to include in the plan.<br><br>Currently, only [!UICONTROL Connected TV] is available.| Yes |
| [!UICONTROL Date Range] | The start and end dates for the plan.<br><br>The start date can't be before the current date. The date range can't be greater than 90 days. | Yes | 
| [!UICONTROL Goal Type] | The type of goal (such as [!UICONTROL Budget]) to consider for the plan.<br><br>Currently, only [!UICONTROL Budget] is available. | Yes |
| [!UICONTROL Goal Value] | The goal value for the forecast. For more accurate forecast results, use a value > 5000 USD. | Yes | 
| [!UICONTROL Max Bid] | The maximum amount to pay for 1000 impressions. If the [!UICONTROL Connected TV] media type is selected, enter a value of at least 10 USD. | Yes |
| [!UICONTROL Frequency Cap] | The number of times a unique household should be served ads.<br><br>When you implement a plan and must create multiple placements, apply the frequency cap setting at the package level, not the placement level, to ensure proper delivery. | Yes |
| [!UICONTROL Geo-Targeting] | Locations to include or exclude as targets. Options include:<ul><li>Countries, cities, states: Click the **[!UICONTROL Country/State/City]** tab; select whether the area is a *Country*, *State*, or *City*; optionally expand any location to view its subcomponents, and then click **[!UICONTROL Include]** or **[!UICONTROL Exclude]** next to the location.</li><li>Designated market areas (DMAs) in the United States: Click the **[!UICONTROL DMA]** tab; optionally expand any state to view its DMAs, and then click **[!UICONTROL Include]** or **[!UICONTROL Exclude]** next to the location.</li><li>Postal codes: You can either:<ul><li>Click the **[!UICONTROL Search postal code]** tab, select the country, enter the full city name or letters contained within the city name and then press the **[Enter]** key, click the correct city name to view all zip codes for the city, click the correct zip code, and then click **[!UICONTROL Include]** or **[!UICONTROL Exclude]**.</li><li>Click the **[!UICONTROL Paste postal code]** tab,, select the country, enter or paste comma-separated values, and then click **[!UICONTROL Include All]** or **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Yes |
| [!UICONTROL Inventory Targeting] | Inventory sources to include or exclude as targets. Select at least one feed or source. | Yes |
| [!UICONTROL Site/App Targeting] | Websites and apps to include or exclude as targets. Enter one URL per line, and then click **[!UICONTROL Include All]** or **[!UICONTROL Exclude All]**. | No |
| [!UICONTROL Audience Targeting] | Audiences to include or exclude as targets. | No |
| [!UICONTROL Ad duration] | The duration of ads to consider for the plan. | No |

>[!MORELIKETHIS]
>
>* [About the DSP Planner Tool](planner-about.md)
>* [Create a Connected TV Reach Plan](planner-create.md)
>* [Duplicate a Connected TV Reach Plan](planner-duplicate.md)
>* [Edit a Connected TV Reach Plan](planner-edit.md)
>* [Export a Connected TV Reach Plan](planner-export.md)
>* [Regenerate the Forecast for a Connected TV Reach Plan](planner-forecast.md)
>* [Archive a Connected TV Reach Plan](planner-archive.md)
