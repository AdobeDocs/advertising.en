---
title: View the Placement Forecast Report
description: See the number of impressions, spend, and optimum max bid forecasted for a particular targeting strategy for a placement.
feature: DSP Placements
exl-id: 6ff228b2-b656-493e-a299-98c7a68a0f51
---
# View the Placement Forecast Report

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

The placement forecast tool shows the forecasted number of impressions, spend, and optimum maximum bid for a particular targeting strategy. Forecasting is calculated based on the overall inventory that is available with the placement and the unique users that are available.

>[!NOTE]
>
>* No forecast is generated for placements with only programmatic guaranteed (PG) targeting because availability and spending are deterministic.  

## Information in the Forecast

The forecast includes the following information:

* **[!UICONTROL Summary]:** 

  * **[!UICONTROL Estimated CPM]:** The estimated cost per thousand impressions (eCPM) that the targeting settings can expect to reach.

  * **[!UICONTROL Budget]:** The estimated budget for the targeting settings.

  * **[!UICONTROL Impression]:** The estimated number of impressions for the targeting settings.

* **[!UICONTROL Budget Yield Curve]:** The estimated number of impressions the placement can deliver at different budget levels if all other targeting settings are the same.

* **[!UICONTROL Max Bid Yield Curve]:** The estimated spend for the placement at different Max Bid levels, when all other targeting settings are the same.  

* **[!UICONTROL Message]:** Provides information about the forecasted output, including any scenarios in which the forecast could not be generated. It also highlights any targeting settings reviewed but not considered in that scenario due to a lack of data. 

### Budget Calculation

* For placements that aren't assigned to a package, the placement budget is used for calculations. Within a flight, the same overall budget is calculated.

* For placements within a package, the budget assigned to the placement is used for calculations. During the flight, the budget allocated to the placement is calculated and is included in the message.

* For placements added to a package in flight, the budget is divided equally based on the number of placements. When the placement goes live, the budget assigned by the package is calculated.

## Requirements

* Minimum spend: $25 daily or equivalent in local currency per placement.

* Maximum spend: $15,000 daily or the equivalent in local currency per placement.

* Minimum Max Bid, Maximum Max Bid: There is a minimum max bid (for the Budget Yield Curve) and maximum max bid (for the Max Bid Yield Curve) by placement type. These values are true globally and do not take into account regional variations. Sometimes, these values may be too high or low for the targeted region. 

* Historical Data: The placement forecast is available when sufficient historical data is available. The following are examples of when insufficient historical data may be available:

  * The placement targets a new region for the campaign.

  * The placement targets a new inventory deal for the campaign.

  * The placement uses a new ad type for the campaign.

    A placement is usually a collection of multiple ad templates as defined by supply-side platforms. So, even if the placement has existed for a long time, the underlying ad template can be new, and the forecasting tool will be unable to forecast.

## Open the Placement Forecast Report

1. In the main menu, click **[!UICONTROL Campaigns]**.
   
1. Click the name of the campaign, and then click **[!UICONTROL Placements]**.
   
1. Next to the placement name, click  **[!UICONTROL ...]** > **[!UICONTROL Edit]**.
   
1. Locate the **[!UICONTROL Forecast]** section in the upper right. If necessary, click ![Forecast](/help/dsp/assets/placement-forecast.png).

   >[!NOTE]
   >
   >* Sometimes the forecast may be unavailable due to browser cache. If this happens, clear the cache and try again.

>[!MORELIKETHIS]
>
>* [Types of Performance Reports in Campaign Management Views](campaign-reports-about.md)
>* [View the Placement Diagnostic Reports](/help/dsp/campaign-management/reports/placement-diagnostics.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
