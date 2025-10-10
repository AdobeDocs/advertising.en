---
title: About simulations
description: Learn about portfolio simulations.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: yes
exl-id: 2fbefee2-f8f7-4b3d-a039-e1ca0236c61a
---
# About simulations

*Beta feature*

Simulation reports show the estimated marginal cost-to-objective value, cost, number of clicks, and objective value that you can expect for a portfolio at various levels of spending (cost) and the corresponding daily budgets or other targets. You can optionally customize the view<!-- add link --> to see additional traffic metrics, simulation settings, and only a specific simulation type ([!UICONTROL Weekly] or [!UICONTROL Custom]).

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Types of simulations

* Automated weekly simulations

* Custom, user-generated simulations 

### Automated weekly simulations

Simulation reports are run automatically each week using the current portfolio settings. Automated weekly simulations are available only for periods in which the portfolio is [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

#### Downloaded weekly simulations

Each downloaded weekly simulation consists of one workbook. Each workbook includes the target for each of 20 step levels and the projected cost, clicks, weighted revenue (objective value), and conversion metrics included in the objective, based on the corresponding target. For the first 20 data rows, constraints weren't applied; for the remaining data rows, constraints were applied.

#### On-screen weekly simulation details



### Simulation details

Click any simulation name to see the simulated performance in graph and table views.

#### Graph view

The graph view shows cost data based on a specified metric ([!UICONTROL Y-Axis Metric]). For example, you can see cost per objective value. The target midpoint is identified. Hold the cursor over any point in the graph to see the data for that point.

When the simulation was built taking constraints into consideration, the applied constraints are identified, and you can view the data with and without constraints applied, with constraints applied, and without constraints applied.

target midpoint

#### Table view







### Custom, user-generated simulations

You can create a custom simulation report for a single [optimized or active](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) portfolio using the current portfolio settings or using custom portfolio settings to see the results that those settings would produce without actually changing them. For example, you could create a custom simulation to see the effect of using a different spending strategy or learning budget<!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. You can view estimated performance at the portfolio, campaign, bid unit, and device levels. Custom simulations inherit the constraints spending setting from the portfolio.

>[!NOTE]
>
> The new custom simulation form uses the same settings as the legacy form, except that it inherits the bid unit constraints information from the portfolio settings. You don't have the option to ignore bid unit constraints, like you did in the old custom simulation settings page.

#### Downloaded custom simulations

Each downloaded custom simulation consists of one workbook. Each workbook includes one worksheet for each specified entity level of simulation (portfolios, campaigns, ad groups, bid units) when data is available for that level. When you specify device-level data, each worksheet includes a [!UICONTROL Device] column. Each worksheet includes one row with data for each applicable entity and (when specified for the report) and device type for each of 20 steps (for example, one row per campaign). The data in each row includes the projected marginal cost-to-revenue, cost, clicks, weighted revenue (objective value), the device type, and conversion metrics included in the objective, based on the corresponding target. The portfolio-level worksheet also includes the target for the step levels, and the entity-level worksheet includes the ad network, account, campaign, and (when applicable) the ad group.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

#### On-screen custom simulation details

<!-- same as for weekly simulations -->







## The [!UICONTROL Simulations] view

The [!UICONTROL Simulations] view lists weekly simulations and custom simulations. Administrator and some other user types<!-- Verify which --> can see custom simulations created by other users. All other users can see only the custom simulations they create.

The data table includes the progress of each simulation; a [!UICONTROL Target Midpoint] column populated for each row; and columns for cost/impression/click/objective value predictions, actual values, and accuracy. You can optionally add additional custom columns (including lift metrics, such as actual objective value divided by cost).

### Available actions {#simulations-actions}

* [Customize the view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) to include additional metrics, including the estimated impressions; the actual cost, clicks, impressions, and objective value; the cost-to-objective value; the cost accuracy, click accuracy, and objective value accuracy; and the difference (delta) between the predicted and actual objective value and cost-to-objective value. You can also include columns for most of the simulation settings and the simulation type ([!UICONTROL Custom] or [!UICONTROL Weekly]).

* [Generate or rerun a custom simulation](simulation-create.md) for a single portfolio. You can either create a new simulation or regenerate an existing simulation in the list.

* View a weekly or custom simulation in-screen.<!-- Create procedure and add link. Call this "simulation details" or just "in-screen simulation?" -->







* [Download weekly and custom simulations](simulation-download.md) as [!DNL Microsoft Excel] workbooks in ZIP files.

* Using the [!UICONTROL Spend Planner] button, open the legacy Spend Recommendation tool, which helps you to identify the optimal spend distribution across portfolios.

## Best practices

Monitor simulation reports in the following situations:

* Before you launch a portfolio to estimate the performance you can expect with the corresponding portfolio settings; use at least two weeks of data. If the simulation results indicate lower performance than you would expect based on historical data for the included campaigns, investigate and resolve the issues before launching the portfolio.

* After any major change to a portfolio, such as adding a campaign or changing the objective. If you make changes to the portfolio's modeling start date, the weight of a conversion metric, or the click value of an objective, then wait until after 17:00 PST the next day to run the simulation, when updated cost and revenue models are available.

* Periodically to monitor performance trends at the conversion metric level.

>[!MORELIKETHIS]
>
>* [Run or rerun a simulation](simulation-create.md)
>* [Download simulations](simulation-download.md)
