---
title: (New UI) About portfolios
description: Learn about portfolios.
feature: Search Portfolios, Search Optimization
hide: yes
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
---
# (New UI) About portfolios

*Beta feature*

You can manage your ad campaigns collectively using portfolios (similar to investment portfolios). A portfolio is a set of ad campaigns or ad sets, including their associated keywords and ads, that are optimized to a single business objective. An objective may include multiple weighted conversions and a single budget or performance target (such as a monthly budget or a target ROI). Because individual campaigns/ad sets, keywords, and ads may perform differently from each other (for example, they may spend different amounts or achieve different ROIs), the optimization capability uses AI-driven models to steer the entire portfolio to collectively achieve the target. All campaigns in a portfolio use the same currency.

Some user roles can create and configure portfolios. Depending on the portfolio type, the portfolio settings may include the portfolio objective, the assigned campaigns, the spending strategy, any portfolio-level bidding constraints, and the modeling and optimization parameters. When you are ready for Search, Social, & Commerce to begin optimization for a portfolio, change the status to "optimized."

You can optionally group portfolios into portfolio groups so you can view composite click and revenue data for the entire group. Create portfolio groups from the [legacy UI](/help/search-social-commerce/getting-started/ui-switch.md).

Depending on your role, you may be able to generate performance simulations, which use predictive modeling to identify your optimal spend point and detailed forecast accuracy reports.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Optimization support by bid strategy {#optimization-by-bid-strategy}

Campaigns are eligible for optimization based on the campaign or ad group bid strategy.

>[!NOTE]
>
>"Smart bidding" and "automated bidding" often are used interchangeably, but they’re not the same thing. Smart bidding refers only to [!DNL Google Ads] and [!DNL Microsoft Advertising] automated bidding strategies that use auction-time bidding, which means that the ad network optimizes for conversions or conversion values at the time of each auction.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Bid Strategy | Smart Bidding? | Keyword-/Product Group-Level Bid? | Support Level | Objective Type | Bid Unit | What Does Adobe Set? | What Does the Ad Network Set? |
|---|---|---|---|---|---|---|---|
| Manual CPC ([!DNL Google Ads]-only option) | &mdash; | Yes | Create, Edit, Optimize | Single or multi-property objective with any weight value | Keyword + Match Type + Campaign | Keyword bid, campaign budget, bid adjustment values | n/a |
| ECPC (Enhanced CPC) | Yes | Yes | Create, Edit, Optimize | Single or multi-property objective with any weight value | Keyword + Match Type + Campaign | Keyword bid, campaign budget | Adjusts bids in real time |
| Maximize Clicks[^1] | &mdash; | &mdash; | Create, Edit, Optimize | None; optimizes towards clicks only | Campaign | Campaign budget | Adjusts bid in real time to maximize clicks within the budget |
| Maximize Conversions<br>(with or without TCPA) | Yes | &mdash; | Create, Edit, Optimize | Single-property objective using a weight of 1 | Campaign or ad group ([!DNL Google Ads])<br>Campaign only ([!DNL Microsoft Advertising]) | Campaign budget, Target CPA when set<br>TCPA can be a standalone bid strategy in [!DNL Microsoft Advertising]) | Adjusts bid in real time to maximize orders/leads within the budget, meeting a CPA goal when the target is set |
| Maximize Conversion Value<br>(with or without TROAS) | Yes | &mdash; | Create, Edit, Optimize | Multi-property objective with any weight value, or single-property objective with a weight value greater than 1 (to represent a monetary value) | Campaign or ad group ([!DNL Google Ads])<br>Campaign only ([!DNL Microsoft Advertising]) | Campaign budget, Target ROAS when set<br>TROAS can be a standalone bid strategy in [!DNL Microsoft Advertising]) | Adjusts bids in real time to maximize revenue/profit within the budget, meeting an ROAS goal when the target is set |
| Target Impression Share | &mdash; | &mdash; | Create, Edit | n/a | n/a | n/a - can't be assigned to a portfolio | Adjusts bids in real time to meet an impression share goal |

[^1]: The [!UICONTROL Maximize Clicks] bid strategy setting on the ad network isn't the same as the Search, Social, & Commerce objective [!UICONTROL Maximize Clicks]. If the bid strategy is [!UICONTROL Maximize Clicks], then you should assign it only to a portfolio with campaign-level or ad group-level optimization, not a portfolio with keyword-level optimization.

## Portfolio statuses {#portfolio-status}

A portfolio can have the following statuses:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## The [!UICONTROL Portfolios] view

The [!UICONTROL Portfolios] view lists your existing portfolios, with customizable performance data. You can [customize the columns within the view](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) and filter data to include specific portfolios [from the toolbar](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) or from the [column heading](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Available actions

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Create a portfolio](portfolio-create.md)

* [Duplicate a portfolio](portfolio-duplicate.md)

* [Edit portfolio settings](portfolio-edit.md)

* [Bulk edit portfolio settings using bulksheet files](portfolio-bulksheets.md)

* [View portfolio performance details](portfolio-details.md)

* [Download data in the [!UICONTROL Portfolios] view](portfolio-view-report.md) 

>[!MORELIKETHIS]
>
>* [Create a portfolio](portfolio-create.md)
>* [Duplicate a portfolio](portfolio-duplicate.md)
>* [Edit a portfolio](portfolio-edit.md)
>* [Manage data view reports from the [!UICONTROL Portfolios] view](portfolio-view-report.md)
