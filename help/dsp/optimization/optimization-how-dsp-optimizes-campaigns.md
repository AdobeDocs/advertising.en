---
title: How DSP Optimizes Your Campaigns
description: Learn how DSP optimizes the packages in your campaigns.
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
---
# How Advertising DSP Optimizes Your Campaigns

This page outlines how the DSP optimization engine, which is powered by [!DNL Adobe Sensei], optimizes the packages in your campaigns. For tips and tricks on how to manually optimize your campaigns, contact your [!DNL Adobe] account team. <!-- add link to trading playbook if we add it to help -->

Package optimization goals operate at two levels:

* For each package: DSP allocates budget to each placement within the package based on the placement's performance against the selected KPI.  

* For each placement/auction in the package: DSP calculates the real-time economic KPI value for each auction per placement, and then uses this value to determine the bid.

   >[!NOTE]
   >
   >The economic value can be heavily weighted based on how well a placement is spending. If a placement is behind its spend goal, then it will be allowed to buy lower-quality auctions. If a placement is easily meeting its spend goal, then it will focus on higher quality auctions.

## Package Optimization

DSP can optimize your delivery in two fundamental ways, with 20 variations available to align with your specific performance goal. You can choose to:

* Prioritize the performance rate

* Prioritize balancing cost efficiency with performance rate

See [Optimization Goals and How to Use Them](optimization-goals.md) to determine which optimization goal will help you achieve your KPI(s).

### Packages That Prioritize the Performance Rate

For optimization goals that prioritize the performance rate, DSP predicts the performance of each auction and always bids at the Max Bid. Examples of applicable optimization goals include [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate], and so on.  

This optimization mode works well if:

* You already know the effective/acceptable CPM level (for example, a historical benchmark).

* You're willing to manually adjust the [!UICONTROL Max Bid] for each placement if you experience challenges with scaling.  

* You're prioritizing scale over efficiency.

#### Pacing logic {#pacing-logic-performance}

* If spending is on pace, bidding will become more selective, so that you'll only bid on auctions predicted to have high performance rates.

* If spending is behind pace, bidding will become less selective, so that you'll bid on auctions predicted to have lower performance rates in order to catch up to the pacing goal.

#### Clearing Price/Bid Shading {#clearing-price-performance}

After it executes the pacing logic, DSP runs the proposed bid through a clearing price prediction model. If the prediction indicates that the bid can be lowered with minimal decrease to the win rate, then the bid is decremented per the prediction.

### Packages That Prioritize Balancing Cost Efficiency with Performance Rate

For some optimization goals, DSP predicts the performance of each auction and adjusts bid prices automatically, never exceeding a placement's [!UICONTROL Max Bid]. Examples of applicable optimization goals include [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click], and so on.

#### Pacing Logic {#pacing-logic-balanced}

* If spending is on pace, then DSP becomes more price sensitive, bidding lower amounts to trade off win rate with the pacing plan.

* If a performance metric is also being balanced (all goals except [!UICONTROL Lowest CPM]), then the predicted KPI is blended into the amount that is bid. You therefore bid higher for auctions that are predicted to be more performant on a “cost per” basis. 

* If spending is behind pace, then DSP becomes less price sensitive and bids higher amounts, up to the [!UICONTROL Max Bid], to trade off win rate with the pacing plan. 

#### Clearing Price/Bid Shading {#clearing-price-balanced}

After it executes the pacing logic, DSP runs the proposed bid through a clearing price prediction model. If the prediction indicates that the bid can be lowered with minimal decrease to the win rate, then the bid is decremented per the prediction.  

## Placement Optimization

Placement pre-bid filters are the strictest way to ensure strong performance. DSP uses pre-bid filters strategically across different ad types to achieve performance goals across placements within each package. You can use pre-bid filters concurrently with package-level optimization or independently.  

>[!NOTE]
>
>The available pre-bids filters vary by ad type. For example, for a standard display placement, you can filter by click-through rate and viewability but not by completion rate.

See [Placement-level Pre-Bid Filters and How to Use Them](optimization-pre-bid-filters.md) to determine which pre-bid filter will help you achieve your KPI(s).

>[!MORELIKETHIS]
>
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Placement-level Pre-Bid Filters and How to Use Them](optimization-pre-bid-filters.md)
>* [Troubleshooting Performance](/help/dsp/optimization/troubleshooting-performance.md)
