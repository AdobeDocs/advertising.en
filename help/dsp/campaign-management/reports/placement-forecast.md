---
title: View the Placement Forecast Report
description: See the number of impressions, spend, and optimum max bid forecasted for a particular targeting strategy for a placement.
feature: DSP Placements
---
# View the Placement Forecast Report

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

*Placements with open auction deals only*

The placement forecast tool shows the forecasted number of impressions, spend, and optimum maximum bid for a particular targeting strategy. Forecasting is calculated based on the overall inventory.

## Information in the Forecast

The forecast includes the following information:

* **[!UICONTROL Summary]:** 

  * **[!UICONTROL Estimated CPM]:** The estimated cost per thousand impressions (eCPM) that the targeting settings can expect to reach.

  * **[!UICONTROL Budget]:** The estimated budget for the targeting settings.

  * **[!UICONTROL Impression]:** The estimated number of impressions for the targeting settings.

* **[!UICONTROL Budget Yield Curve]:** The estimated number of impressions the placement can deliver at different budget levels if all other targeting settings are the same.

* **[!UICONTROL Max Bid Yield Curve]:** To be updated based on user feedback.  

* **[!UICONTROL Message]:** Provides information about the forecasted output, including any scenarios in which the forecast could not be generated. It also highlights any targeting settings reviewed but not considered in that scenario due to a lack of data. 

>[!NOTE]
>
>* No forecast is generated for placements with programmatic guaranteed (PG) targeting because availability and spending are deterministic.  
>* Sometimes the forecast may be unavailable due to browser cache. I this happens, clear the cache and re-open the forecast tool.

### Budget Calculation

* For placements that aren't assigned to a package, the placement budget is used for calculations. Within a flight, the same overall budget is calculated.

* For placements within a package, the budget assigned to the placement is used for calculations. During the flight, the budget allocated to the placement is calculated.

* For placements added to a package in flight, an equal share of the budget based on the number of placements is calculated. When the placement goes live, the budget assigned by the package is calculated.

## Best Practices (Requirements? or Best Practices for __what?__ -- getting useful data?)<!-- wording:  Are these requirements? If best practices, best practices to what? Get useful data? Get complete data? --?

The forecast data will be most useful in the following conditions:

* Minimum spend: $25 daily or equivalent in local currency per placement. Currently, the UI shows calculations in USD. <!--, which will be updated to the campaign currency in a future release. -->

* Maximum spend: $15,000 daily or the equivalent in local currency per placement.

* Historical Data: The placement forecast is available when sufficient historical data is available. The following are examples of when insufficient historical data may be available:

  * The placement targets a new region for the campaign.

  * The placement targets a new inventory deal for the campaign.

  * The placement is a new placement type for the campaign.<!-- a new ad type? -->

    A placement is usually a collection of multiple ad templates as defined by supply-side platforms. So, even if the placement has existed for a long time, the underlying ad template can be new, and the forecasting tool will be unable to forecast.

## Open the Placement Forecast Report

1. Open the placement settings:

   1. In the main menu, click **[!UICONTROL Campaigns]**.
   
   1. Click the name of the campaign, and then click **[!UICONTROL Placements]**.
   
   1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.
   
1. In the upper right, click ![Forecast](/help/dsp/assets/placement-forecast.png) or **[!UICONTROL Forecast]**.

>[!MORELIKETHIS]
>
>* [About In-Platform Reports](campaign-reports-about.md)
>* [View the Placement Diagnostic Reports](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
