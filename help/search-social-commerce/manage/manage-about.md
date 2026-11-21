---
title: About managing campaigns and portfolios
description: Learn how ad network accounts, campaigns, tracking, and portfolio optimization work together, and how to monitor and improve performance.
feature: Search Campaign Management, Search Portfolios
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# About managing campaigns and portfolios

*Beta feature*

Search, Social, & Commerce brings campaign management, performance reporting, and portfolio optimization into one interface. Depending on the ad network and campaign type, you can synchronize campaign data, create and edit campaign components, track conversions, and optimize bids, budgets, or bid strategy targets. See [supported inventory](/help/search-social-commerce/introduction/supported-inventory.md) for the functionality available for each ad network.

The [!UICONTROL Manage] menu provides access to your accounts, campaigns, ad groups, ads, keywords, product groups, and portfolios. Your permissions determine which views and actions are available. For the complete menu organization, see "[How the user interface is organized](/help/search-social-commerce/getting-started/user-interface.md)."

## How accounts, campaigns, and portfolios fit together

* **Ad network accounts** connect your advertiser's data to Search, Social, & Commerce. [Account types](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) include accounts synchronized through an API connection, accounts for which you upload data, and template-based tracking-only accounts. The account type determines whether you can synchronize data, manage campaigns, or use portfolio optimization.

* **Campaigns** contain the ads and other components used to deliver your advertising. For supported campaign types, you can [create and manage campaigns](/help/search-social-commerce/manage/campaigns/campaign-manage.md) and their components from the [!UICONTROL Manage] views. You can also use [bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) for supported bulk operations.

* **Portfolios** group eligible campaigns to optimize them toward a common business objective and budget or performance target. A campaign can belong to only one portfolio, and all campaigns in a portfolio must use the same currency. See "[About portfolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md)."

Portfolio assignment is optional. You can track and report on campaigns without assigning them to a portfolio. Not all ad networks, campaign types, or bid strategies support portfolio optimization.

## Synchronize campaign data

For accounts connected through an API, Search, Social, & Commerce retrieves supported campaign structure and performance data from the ad network. Changes that you make to supported campaign components in Search, Social, & Commerce are sent to the ad network.

When necessary, you can [request a manual sync](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md). If an account stops synchronizing, review its [authentication and access status](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status).

Data upload accounts and tracking-only accounts don't synchronize with the ad network. Follow the workflow for the [account type](/help/search-social-commerce/manage/accounts/ad-network-account-about.md) to provide campaign and performance data.

## Set up tracking and optimization

[Tracking](/help/search-social-commerce/tracking/tracking-about.md) connects campaign activity to the conversions that matter to your business. Depending on your implementation, conversion data may come from Adobe Advertising tags, an Adobe Analytics integration, ad network tracking, or data feeds. Configure click tracking and conversion tracking as required for your implementation, and validate the data before using it for optimization.

In [!UICONTROL Goals] > [!UICONTROL Conversions], you can [review the conversion metrics tracked for the advertiser and control their visibility](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md). Use the appropriate metrics in your [objectives](/help/search-social-commerce/goals/objectives/objective-about.md).

To enable portfolio optimization, [create a portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md), assign an objective and eligible campaigns, and configure its spending and optimization settings. An active portfolio gathers and models performance data. When the data and settings are ready, [change the portfolio status to optimized](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) to begin optimization. The actions performed depend on the portfolio type and the [campaign bid strategies](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

For the detailed setup sequence, see "[Set up ad network accounts and campaigns](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)."

## Monitor campaign and portfolio performance {#monitor-performance}

The account team, agency, or advertiser is responsible for monitoring performance and making adjustments, according to the terms of the service agreement. Routinely:

* Review campaign and account performance in the [!UICONTROL Manage] views. [Customize columns, filters, and date ranges](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) to focus on the metrics and entities that matter.

* Use [!UICONTROL Dashboard] > [!UICONTROL Overview] to [monitor portfolio trends and changes in performance](/help/search-social-commerce/dashboard/dashboard-overview.md).

* Review [custom alerts](/help/search-social-commerce/common-tasks/alerts-manage.md) for conditions that require investigation.

* [Generate reports](/help/search-social-commerce/reports/management/report-manage.md) for campaign, keyword, ad, and portfolio performance. For portfolios, [review performance details](/help/search-social-commerce/manage/portfolios/portfolio-details.md), including actual performance and model accuracy.

* Use [simulations](/help/search-social-commerce/plan/simulations/simulation-about.md), when available, to evaluate the predicted effects of different spending levels.

* Investigate differences between your reported conversions and source data. See the guidance for [!DNL Google Ads] and [!DNL Microsoft Advertising] conversion data in the related links.

## Adjust campaigns and portfolios

Based on performance and changes in your business goals, you may need to:

* Edit campaign settings, create or pause campaign components, refine keyword sets, or test different ads. Available actions depend on the ad network and campaign type.

* Review geographical, audience, and placement targeting using the relevant management views and reports.

* [Change campaign assignments](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio) when a campaign should be optimized with a different portfolio. Assigning a campaign to another portfolio removes it from its previous portfolio.

* [Edit portfolio settings](/help/search-social-commerce/manage/portfolios/portfolio-edit.md), including the objective, spending strategy, constraints, or optimization controls, as permitted by your product profile.

* Review [change history](/help/search-social-commerce/reports/history-logs.md) when investigating performance changes.

>[!MORELIKETHIS]
>
>* [Set up ad network accounts and campaigns](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [Supported inventory](/help/search-social-commerce/introduction/supported-inventory.md)
>* [[!DNL Google Ads] conversion data in Search, Social, & Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] conversion data in Search, Social, & Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
