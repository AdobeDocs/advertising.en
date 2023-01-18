---
title: Troubleshooting Performance
description: Reference common performance issues and see how to troubleshoot them.
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
---
# Troubleshooting Performance

| Issue | Possible Cause | Actions to Take|
| --- | --- | --- |
| No spend on placement | The placement doesn't include ads, and/or the ads aren’t active. | Verify that all expected ads are attached to the placement and are approved and active.<br><br>Also, see if the placement includes a custom ad schedule, which may limit the flight period for each ad. To see the ad schedule for a placement from the Placements view, click  **[!UICONTROL ...] > [!UICONTROL Ad schedule]** next to the placement name. |
| | The affected dates aren’t within the configured flight dates. | Check that the flight dates are valid at the campaign, package, and placement level​s. |
| | The budget goal has been met and/or isn't high enough. | Check the budget settings at the campaign, package, and placement levels. |
| | The account doesn't have enough funding. | To see if that your account is adequately funded, go to **[!UICONTROL Settings] > [!UICONTROL Account]** and look at the amount of [!UICONTROL Usable Funds]. If you need to add more funds, contact your [!DNL Adobe] account team. |
| | No inventory is available. | Verify if the specified inventory sources ([!UICONTROL Public], [!UICONTROL Private], or [!UICONTROL On Demand]) are:<ul><li>Set up correctly.</li><li>Active and sending through auctions.</li><li>Compatible with the applicable ad and placement type.</li></ul><br>If the inventory sources are all valid and active, then target additional or all inventory sources when possible. |
| | No users are available. | Check that the specified audience targets include enough active users. If they don't, then expand the targets by adding more audiences. |
| Low spend on placement | The [!UICONTROL Non Bids] section of the placement diagnostics report shows possible reasons for why the placement didn't bid. | [Review the [!UICONTROL Non Bids] report](/help/dsp/campaign-management/reports/placement-diagnostics.md) to understand why the placement didn't bid.  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | The placement uses [pre-bid filters](/help/dsp/campaign-management/placements/placement-settings.md) that limit bidding. | Lower the thresholds of pre-bid filters by 5% to assess the balance of spend and performance. <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>Keep in mind that using multiple placement targets, such as pre-bid filters, geos, inventory, and audiences, may cumulatively limit bidding and spend. |
| | The placement has a low win rate. | Increase the [!UICONTROL Max Bid] to improve the win rate.<br><br><b>NOTE:</b> Inventory prices may vary based on the placement’s targeting.<br><br>A 10%-win rate is considered healthy. |
| | A low number of inventory is available. | Target additional or all inventory sources if possible.<br><br>Keep in mind that using multiple placement targets, such as pre-bid filters, geos, inventory, and audiences, may cumulatively limit bidding and spend. |
| | A low number of users are available. | Check that the specified audience targets include enough active users. If they don't, then expand the targets by adding more audiences.<br><br>Keep in mind that using multiple placement targets, such as pre-bid filters, geos, inventory, and audiences, may cumulatively limit bidding and spend. |
| | The package includes a large number of active placements. | Either reduce the number of active placements within the package or increase the overall package budget.<br><br>If the package has many placements but not enough budget, DSP may not be able to allocate enough budget to each placement. Each placement should have an opportunity to spend at least 2 USD/day. For example, if your package has a budget of 10 USD/day, then it's best to include five or fewer placements. ​|

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Campaign Settings](/help/dsp/campaign-management/campaigns/campaign-settings.md)
