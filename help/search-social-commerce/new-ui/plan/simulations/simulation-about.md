---
title: About simulations
description: Learn about portfolio simulations.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
TQID: 'https://experienceleague.adobe.com/9B4gKrZnnUmgj0LzxwM2CIkJsIO9Pe9R8RDR4mAmIwo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# About simulations

*Beta feature*

Simulation reports show the estimated marginal cost-to-objective value, cost, number of clicks, and objective value that you can expect for a portfolio at various levels of spending (cost) and the corresponding daily budgets or other targets. You can optionally [customize the view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) to see additional traffic metrics, simulation settings, and only a specific simulation type ([!UICONTROL Weekly] or [!UICONTROL Custom]).

<!--
 Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Types of simulations

* Automated weekly simulations

* Custom, user-generated simulations 

### Automated weekly simulations

Search, Social, & Commerce automatically runs simulation reports each week using the current portfolio settings. Automated weekly simulations are available only for periods in which the portfolio is [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

You can [download weekly simulations for up to 100 portfolios for a selected run date from the [!UICONTROL Portfolios] view](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations), or [download individual simulations from the [!UICONTROL Simulations] view](simulation-download.md).

#### Downloaded weekly simulations

You can download weekly simulations as individual workbooks or combine them in one workbook. The report for each simulation includes the target for each of 20 step levels and the projected cost, clicks, weighted revenue (objective value), and conversion metrics in the objective, based on the corresponding target. The simulation calculates the first 20 data rows without constraints and the remaining data rows with constraints.

#### On-screen weekly simulation details

On-screen simulation details show portfolio-level visual and tabular insights. For data by campaign, ad groups, bid units, or device, [download the simulation](simulation-download.md) instead.

##### Graph view

The graph view shows the expected objective value or other specified metric ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) for the spend target for each of 20 spend levels. The graph identifies the target midpoint, and you can optionally change the target midpoint to see the predicted data using that value. Hold the cursor over any point in the graph to see the data for that point.

You can view data with constraints, without constraints, or both. When you view data with constraints, the view identifies those constraints above the graph.

##### Table view

The table view shows the target spend for each of 20 spend levels. It also includes the corresponding estimated cost, marginal cost to objective value, clicks, objective value, and conversion metrics in the portfolio's objective for each spend level. The table identifies the target midpoint, and you can optionally change the target midpoint to see the predicted data using that value.

You can view data with constraints, without constraints, or both. When you view data with constraints, the view identifies those constraints above the graph.

##### Simulation settings

The view shows read-only simulation settings beneath the graph or table.

##### Portfolio settings

To see the read-only settings for the applicable portfolio, click **[!UICONTROL Portfolio Settings]** in the upper right.

### Custom, user-generated simulations

You can create a custom simulation report for a single [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) portfolio using the current portfolio settings or using custom portfolio settings, with or without bid unit-level constraints applied, to see the results that those settings would produce without actually changing them. For example, you could create a custom simulation to see the effect of using a different spending strategy or learning budget without considering active constraints on bid units in the portfolio. You can view estimated performance at the portfolio, campaign, bid unit, and device levels.

#### Downloaded custom simulations

You can download custom simulations as individual workbooks or combine them in one workbook. The report for each simulation includes one worksheet for each entity level you specify (portfolios, campaigns, ad groups, bid units) when data is available for that level. When you specify device-level data, each worksheet includes a [!UICONTROL Device] column. Each worksheet includes one row for each applicable entity and, when you request device-level data, device type for each of 20 steps (for example, one row per campaign). The data in each row includes the projected marginal cost-to-revenue, cost, clicks, weighted revenue (objective value), the device type, and conversion metrics in the objective, based on the corresponding target. The portfolio-level worksheet also includes the target for the step levels, and the entity-level worksheet includes the ad network, account, campaign, and (when applicable) the ad group.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### On-screen custom simulation details

On-screen simulation details show portfolio-level visual and tabular insights. For data by campaign, ad groups, bid units, or device, [download the simulation](simulation-download.md) instead.

#### Graph view

The graph view shows the expected objective value or other specified metric ([!UICONTROL Y-Axis Metric]<!-- I see Objective Value, Cost, Clicks, the metrics in the portfolio's objective, and then a couple of other conversion metrics. Where do the other conversion metrics come from? -->) for the spend target for the specified number of spend levels (steps) for the simulation. The graph identifies the target midpoint. Hold the cursor over any point in the graph to see the data for that point.

When the simulation accounts for constraints, the view identifies those constraints above the graph.

##### Table view

The table view shows the target spend for each of the specified number of spend levels (steps) for the simulation. It also shows the corresponding estimated cost, marginal cost to objective value, clicks, objective value, and conversion metrics in the portfolio's objective for each spend level. The table identifies the target midpoint.

When the simulation accounts for constraints, the view identifies those constraints above the graph.

##### Simulation settings

The view shows read-only simulation settings beneath the graph or table.

##### Portfolio settings

To see the read-only settings for the applicable portfolio, click **[!UICONTROL Portfolio Settings]** in the upper right.

## The [!UICONTROL Simulations] view

The [!UICONTROL Simulations] view lists weekly simulations and custom simulations. Administrator and some other user types<!-- Verify which --> can see custom simulations that other users create. All other users can see only the custom simulations they create.

The data table shows the progress of each simulation; the [!UICONTROL Target Midpoint] for each row; and columns for cost/impression/click/objective value predictions, actual values, and accuracy. You can optionally add additional custom columns (including lift metrics, such as actual objective value divided by cost).

### Available actions {#simulations-actions}

* [Customize the view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) to include additional metrics, including the estimated impressions; the actual cost, clicks, impressions, and objective value; the cost-to-objective value; the cost accuracy, click accuracy, and objective value accuracy; and the difference (delta) between the predicted and actual objective value and cost-to-objective value. You can also include columns for most of the simulation settings and the simulation type ([!UICONTROL Custom] or [!UICONTROL Weekly]).

* [Generate a custom simulation](simulation-create.md#simulation-create) for a single portfolio, using the portfolio's current settings as defaults.

* [Rerun up to 10 simulations with their existing settings](simulation-create.md#rerun-a-simulation-with-the-existing-settings). Search, Social, & Commerce skips simulations with a status of [!UICONTROL Queued] or [!UICONTROL In Progress].

* [View a weekly or custom simulation on-screen](simulation-view.md).

* [Download up to 10 weekly and custom simulations](simulation-download.md) as a single [!DNL Microsoft Excel] workbook or as separate workbooks in a ZIP file.

* Using the [!UICONTROL Spend Planner] button, open the legacy Spend Recommendation tool, which helps you to identify the optimal spend distribution across portfolios.

## Best practices

Monitor simulation reports in the following situations:

* Before you launch a portfolio to estimate the performance you can expect with the corresponding portfolio settings; use at least two weeks of data. If the simulation results indicate lower performance than you would expect based on historical data for the included campaigns, investigate and resolve the issues before launching the portfolio.

* After any major change to a portfolio, such as adding a campaign or changing the objective. If you make changes to the portfolio's modeling start date, the weight of a conversion metric, or the click value of an objective, then wait until after 17:00 PST the next day to run the simulation, when updated cost and revenue models are available.

* Periodically to monitor performance trends at the conversion metric level.

>[!MORELIKETHIS]
>
>* [Run or rerun a simulation](simulation-create.md)
>* [View simulation details](simulation-view.md)
>* [Download simulations](simulation-download.md)
