---
title: (New UI) Advertising insights
description: Learn how to configure and view advertising insight dashboards for model accuracy, performance, simulations, budget caps, and conversions.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# (New UI) Advertising insights

Advertising insights present visual, actionable data to help you evaluate portfolio performance, identify optimization issues, and compare conversion data. Each insight is generated on demand and displayed as an on-screen dashboard.

The **[!UICONTROL Reports] > [!UICONTROL Insights]** view displays the available insights under **[!UICONTROL Dashboards]**. The page heading is **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>This page describes the insight dashboards in the beta new user interface. Availability depends on your access and the insights available for the selected advertiser. The [legacy Advertising Insights](/help/search-social-commerce/legacy-ui/advertising-insights/insight-about.md) include a different set of analyses and procedures for generated files.

## Types of insights {#insight-types}

| Insight | Description |
| --- | --- |
| [!UICONTROL Model Accuracy] | Identifies how well Search, Social, & Commerce predicts cost and revenue for a portfolio. You can review model accuracy at the portfolio, ad network, and campaign levels. |
| [!UICONTROL Performance Insights] | Compares portfolio performance before and after an optimization status change, objective change, or specified date. The dashboard includes performance summaries, an audit of changes affecting optimization, campaign comparisons, trends, and objective value analysis. |
| [!UICONTROL Portfolio Simulation Analysis] | Compares an existing custom simulation with actual performance. You can review portfolio and campaign data, analyze simulation accuracy, and explore estimated performance at different target spend levels. |
| [!UICONTROL Campaign Budget Cap Analysis] | Indicates whether a portfolio's spend was limited by campaign budget caps. The dashboard includes capped spend, affected campaigns, estimated lost impressions, daily and day-of-week trends, and recommendations for portfolio settings. |
| [!UICONTROL Modeled Conversions] | Compares Adobe conversion values with values reported by the ad network, including modeled data. You can analyze accounts, portfolios, or campaigns and compare both Adobe-measured and Adobe-measured-and-modeled values with publisher-reported values. |
| [!UICONTROL Delayed Revenue Analysis] | Measures conversion lag (the time elapsed between an ad click or view-through and a subsequent conversion) and shows its impact on objective value, return on investment (ROI), and model accuracy. The analysis is available only for portfolios with click-based or view-through revenue attribution. |

## Generate an insight {#insight-generate}

1. In the main menu, click **[!UICONTROL Reports] > [!UICONTROL Insights]**.

1. Click the insight that you want to generate.

1. In the **[!UICONTROL Configure]** panel, specify the [insight settings](#insight-settings).

1. Click **[!UICONTROL Generate Insight]**.

   The configuration panel closes, and the dashboard displays the analysis.

1. Review the [insight results](#insight-results).

To change the settings, click **[!UICONTROL Configure]**, change the values, and click **[!UICONTROL Generate Insight]** again. To return to the insight list, click **[!UICONTROL Analysis List]** in the breadcrumb.

## Insight settings {#insight-settings}

### Model Accuracy {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** Select one portfolio.

* **[!UICONTROL Choose Revenue Type]:** Select **[!UICONTROL Actual Revenue]** (the default) or **[!UICONTROL Delayed Revenue]**.

* **[!UICONTROL Date Range]:** Select the dates to analyze. See [Date range settings](#date-range-settings).

### Performance Insights {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** Select one portfolio.

* **[!UICONTROL Revenue Type]:** Select **[!UICONTROL Actual Revenue]** (the default) or **[!UICONTROL Delayed Revenue]**.

* **Event date:** Select the type of date around which to compare performance:

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (the default): Select an available optimization status change date for the portfolio.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Select an available objective change date for the portfolio.

  * **[!UICONTROL Specific Date]:** Specify a date using the date picker.

  Select the event date before configuring the comparison periods. If no event dates are available for the selected portfolio, you can use **[!UICONTROL Specific Date]**.

* **[!UICONTROL Pre Days]:** Specify the period before the event date:

  * Select **[!UICONTROL 7]** (the default), **[!UICONTROL 14]**, or **[!UICONTROL 30]**.

  * Select **[!UICONTROL Pre Start Date]** and specify the **[!UICONTROL Custom Pre Date]**.

  * Select **[!UICONTROL Custom Pre Days]** and enter a positive number of days.

* **[!UICONTROL Post Days]:** Specify the period after the event date:

  * Select **[!UICONTROL 7]** (the default), **[!UICONTROL 14]**, or **[!UICONTROL 30]**.

  * Select **[!UICONTROL Post End Date]** and specify the **[!UICONTROL Custom Post Date]**.

  * Select **[!UICONTROL Custom Post Days]** and enter a positive number of days.

  The event date itself isn't included in either comparison period.

* **[!UICONTROL Date Exclusion]:** (Optional) Exclude dates from the analysis:

  1. Click **[!UICONTROL Select Dates]**.

  1. Select the dates to exclude:

     * Click individual dates to select or deselect them.

     * Hold **[!UICONTROL Shift]** while clicking to select a range.

     * To remove all exclusions, click **[!UICONTROL Clear All]**.

  1. Click **[!UICONTROL Done]** when you're finished.

### Portfolio Simulation Analysis {#simulation-settings}

* **[!UICONTROL Portfolios]:** Select one portfolio with an existing custom simulation.

* **[!UICONTROL Simulation Date]:** Select the date of the simulation to analyze. If multiple simulations are available for that date, also select the simulation by name.

  If no custom simulations are available, [generate a custom simulation](/help/search-social-commerce/manage/portfolios/portfolio-create-simulation.md) before using this insight.

* **[!UICONTROL Actual Days]:** Select **[!UICONTROL 7]** (the default), **[!UICONTROL 14]**, or **[!UICONTROL 30]** days of actual performance data. To specify another number, select **[!UICONTROL Enter Actual Days]** and enter a value from 1-90.

* **[!UICONTROL Type]:** Select **[!UICONTROL Transaction Date]** (the default) or **[!UICONTROL Click Date]** for conversion attribution.

### Campaign Budget Cap Analysis {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** Select one portfolio.

* **[!UICONTROL Date Range]:** Select the dates to analyze. See [Date range settings](#date-range-settings).

### Modeled Conversions {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** Select **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (the default), or **[!UICONTROL Campaign]**.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]**, or **[!UICONTROL Campaigns]:** Select the applicable entities for the analysis level. You can select multiple entities.

* **[!UICONTROL Date Range]:** Select the dates to analyze. See [Date range settings](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Select the Adobe conversion property to compare.

* **[!UICONTROL Publisher Conversion]:** Select the publisher conversion property to compare.

  The available conversion properties depend on the analysis level, selected entities, and date range. Both conversion properties are required for the comparison.

### Delayed Revenue Analysis {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** Select one portfolio with click-based or view-through revenue attribution.

* **[!UICONTROL Date Range]:** Select the dates to analyze. See [Date range settings](#date-range-settings).

### Date range settings {#date-range-settings}

For insights with a **[!UICONTROL Date Range]** setting, select **[!UICONTROL Last 7 days]** (the default), **[!UICONTROL Last 14 days]**, or **[!UICONTROL Last 30 days]**.

To specify another period, select **[!UICONTROL Custom Date]** and enter the **[!UICONTROL Start Date]** and **[!UICONTROL End Date]**. You can select dates within the last 90 days, through the current date.

## View insight results {#insight-results}

### Model Accuracy {#model-accuracy-results}

Review the portfolio details and use the following tabs:

* **[!UICONTROL Portfolio]:** Review portfolio-level model accuracy and budget comparisons.

* **[!UICONTROL Ad Network]:** Review model accuracy and budget comparisons by ad network.

* **[!UICONTROL Campaigns]:** Review campaign-level model accuracy and target versus actual performance.

* **[!UICONTROL Playground Beta]:** Compare model accuracy for multiple campaigns.

For campaign accuracy charts, select the **[!UICONTROL Comparison Options]** and **[!UICONTROL Campaign]**. In **[!UICONTROL Playground Beta]**, you can select multiple campaigns. Click **[!UICONTROL Table View]** to switch between a chart and its underlying data.

### Performance Insights {#performance-insights-results}

The dashboard shows the **[!UICONTROL Pre Period]** and **[!UICONTROL Post Period]**, aggregated performance metrics for both periods, and portfolio details.

The **[!UICONTROL Audit Trail]** summarizes changes to factors affecting optimization, including portfolio budget, spend strategy, minimum campaign spend, and spend limit multiple. When changes have details available, click **[!UICONTROL View Details]** to inspect them.

Use the **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]**, and **[!UICONTROL Objective Value And Analysis]** tabs to explore the comparison.

### Portfolio Simulation Analysis {#simulation-results}

Review the simulation details and use the following tabs:

* **[!UICONTROL Portfolio]:** Review portfolio-level simulation data. Within this tab:

  * **[!UICONTROL Simulation Data]** shows simulation metrics and target spend performance.

  * **[!UICONTROL Simulation Vs Actual]** compares simulated and actual performance.

  * **[!UICONTROL Try New Target]** lets you enter a target spend in **[!UICONTROL Explore Target Spend]** to view estimated clicks, cost, and revenue. This is an analysis of estimated performance; it doesn't change the portfolio's spend target.

* **[!UICONTROL Campaigns]:** Review campaign-level simulation comparisons.

* **[!UICONTROL Accuracy Analysis]:** Review simulation accuracy.

### Campaign Budget Cap Analysis {#budget-cap-results}

Review the portfolio details and summary metrics:

* **[!UICONTROL Total Capped Spend]:** The percentage of spend on days when campaign budgets were hit.

* **[!UICONTROL Capped Campaigns]:** The number of campaigns that hit their budgets at least once.

* **[!UICONTROL Est. Lost Impressions]:** Estimated impressions missed because of budget caps.

* **[!UICONTROL Peak Capping Day]:** The day of the week with the most capped spend.

The **[!UICONTROL Spend on Capped Campaigns by Day]** and **[!UICONTROL Capped Spend by Weekday]** charts show capping trends. Review **[!UICONTROL Capped Campaign Performance]** for campaign details and **[!UICONTROL Portfolio Settings Recommendations]** for suggested settings changes.

### Modeled Conversions {#modeled-conversions-results}

Review the following tables for the selected entities and date range:

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** Compares conversion values measured directly by Adobe with publisher-reported values, which include measured and modeled data.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** Compares Adobe-measured-and-modeled conversion values with publisher-reported values.

Both tables include the entity name and ID, Adobe value, publisher-reported value, absolute difference, and percentage difference.

If no data is available, verify that you selected both conversion properties and that data exists for the selected entities and date range.

### Delayed Revenue Analysis {#delayed-revenue-results}

The **[!UICONTROL Key Insights Summary]** shows expected weighted revenue (now called "[objective value](/help/search-social-commerce/glossary.md#o-p)"), ROI, and model accuracy information.

The **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** section shows the percentage of conversions realized on day 0 and by days 3, 7, 14, and 28 for each revenue property.

In **[!UICONTROL Performance Over Time]**, select **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]**, or **[!UICONTROL Model Accuracy]** to compare click-date, transaction-date, and expected performance. Click **[!UICONTROL Table View]** to switch between the chart and its underlying data.

In **[!UICONTROL Metrics Definitions]**, click **[!UICONTROL Show]** for explanations of the dates and metrics used in the analysis, or **[!UICONTROL Hide]** to collapse them.

If the analysis isn't applicable, select a portfolio with click-based or view-through revenue attribution. If no data is available, verify that data exists for the selected portfolio and date range.
