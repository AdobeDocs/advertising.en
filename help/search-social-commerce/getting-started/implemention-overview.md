---
title: Overview of implementing Search, Social, & Commerce
description: Learn about the general workflow to launch and maintain a portfolio.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
---
# Overview of implementing Search, Social, & Commerce

[!DNL Adobe] or one of its affiliate agencies works with each advertiser to launch its online advertising portfolios and to track any additional ad campaigns. After the initial launch, additional ongoing tasks ensure that the advertiser's goals will continue to be met.

The following is the general workflow for implementing and using Search, Social, & Commerce.

## Initial Launch

[!DNL Adobe] and/or your agency work with you do the following:

1. Evaluate your high-level business goals and devise strategies to achieve them:

   1. Identify your business model and marketing objectives.
  
   1. Identify your conversion tracking requirements
  
   1. Analyze your existing online ad account structures.
  
   1. Identify metrics for portfolio optimization and reporting.

1. (Administrator or account manager users) Set up administrative accounts:

   1. Set up the advertiser's account. If an agency manages the advertiser's data, then the advertiser's account must be associated with the agency account.
  
   1. (If necessary) Create user accounts for the advertiser to view and manage its campaign data and to generate reports.

   Work with your administrator to configure access using Adobe Admin Console and the appropriate product profiles. See "[User administration for Search, Social, & Commerce](/help/search-social-commerce/user-administration.md)."

1. Synchronize with, or create, campaigns for each of your ad network accounts:

   * For API-connected accounts, [create the account details](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account) in [!UICONTROL Manage] > [!UICONTROL Accounts], complete the network-specific authentication, configure tracking options, and enable the account.

   * For accounts without API support, follow the [data upload](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md) or [tracking-only account](/help/search-social-commerce/manage/accounts/template-account-manage.md) workflow, as applicable. These accounts don't synchronize with the ad network or support portfolio optimization.
  
   * If the accounts don't already contain campaign data, then add campaigns, ad groups, keywords, ads, and placements from within Search, Social, & Commerce or from within the ad network.
   
     For the detailed setup checklist, see "[Set up ad network accounts and campaigns](campaign-implementation-overview.md)." For supported campaign types, use [!UICONTROL Manage] > [!UICONTROL Campaigns] to [create and manage campaigns](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Set up tracking for all ads for which you want Adobe Advertising to track conversions:

   1. (If necessary) [Set up click tracking](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) for ads, and optionally for keywords, [!DNL Google Ads] placements, and [!DNL Google Ads] extensions by generating and uploading click-tracking URLs.
   
      Click tracking URLs for advertisers with the Adobe Advertising pixel-based conversion tracking service include a redirect to [!DNL Adobe] servers.
  
   1. [Set up conversion tracking](/help/search-social-commerce/tracking/conversion-tracking-about.md). Depending on the implementation, this may involve adding conversion tracking tags to the appropriate webpages and/or setting up a daily feed drop for conversion data that you've collected using your own method. You can [generate Adobe Advertising conversion-tracking tags](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) from [!UICONTROL Goals] > [!UICONTROL Conversions].
   
      For more information, see "[About tracking for Search, Social, & Commerce](/help/search-social-commerce/tracking/tracking-about.md)."

1. Set up integrations with additional products:

    1. (Advertisers with Adobe Analytics and/or Adobe Audience Manager) Set up integrations between the various accounts so that Adobe Advertising can exchange data with them.
    
       See the guide on "[Integrations with CX Enterprise](/help/integrations/home.md)."
    
    1. (Advertisers with [!DNL Google Analytics]) Sync conversion metrics for a [!DNL Google Analytics] account, property, and view combination for optimization and reporting.
    
       This configuration uses the legacy user interface. See "[About syncing [!DNL Google Analytics] conversion metrics](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)" and, when needed, [switch to the legacy interface](ui-switch.md).

1. (Optional) Set up and launch portfolios:

   1. In [!UICONTROL Goals] > [!UICONTROL Conversions], [review the conversion metrics and make the required metrics visible](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). In [!UICONTROL Goals] > [!UICONTROL Objectives], [create or select an objective](/help/search-social-commerce/goals/objectives/objective-about.md) for optimization.

   1. In [!UICONTROL Manage] > [!UICONTROL Portfolios], [create portfolios](/help/search-social-commerce/manage/portfolios/portfolio-create.md) configured to meet your objective and business goals, with the appropriate [eligible campaigns](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). [Activate the portfolios](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) to gather and model data. The implementation team then gathers and validates click and revenue data for at least 14 days and validates the portfolio settings.
   
      >[!NOTE]
      >
      >Search, Social, & Commerce still tracks and reports data for campaigns that aren't assigned to portfolios, but it doesn't provide optimization for them.

   1. After enough data is available to create a baseline, the team can [change the portfolio status to optimized](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) &mdash; allowing Search, Social, & Commerce to optimize bids, budgets, and/or bid strategy targets for the portfolio, based on the portfolio type and campaign bid strategies.
   
   See "[About portfolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md)" for optimization support and portfolio statuses.

1. Monitor your portfolios' performance:

   1. Use [!UICONTROL Dashboard] > [!UICONTROL Overview] to [review portfolio trends](/help/search-social-commerce/dashboard/dashboard-overview.md), and [view portfolio performance details](/help/search-social-commerce/manage/portfolios/portfolio-details.md) to investigate results and model accuracy.
  
   1. [Set up custom alerts](/help/search-social-commerce/common-tasks/alerts-manage.md) and [generate customized reports](/help/search-social-commerce/reports/management/report-manage.md) for performance monitoring. When needed, automate reporting using [report templates](/help/search-social-commerce/reports/report-templates-manage.md) and [spreadsheet feeds](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).
   
   For more information, see "[Monitor campaign and portfolio performance](/help/search-social-commerce/manage/manage-about.md#monitor-performance)."

1.  (Optional) Configure your [performance data views](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) to show the data that you want to see.

## Ongoing Tasks

After the initial launch, the following ongoing tasks are required. Depending on your terms of engagement, either [!DNL Adobe], an affiliate agency, or the advertiser performs these tasks:

* Continue to monitor and analyze the performance of each portfolio by viewing alerts, performance data for each portfolio and its component campaigns, customizable reports, and (some roles) simulations.

* Adjust the various strategies and settings that you use to manage the portfolio set, as necessary, based on the portfolio's actual and predicted performance and opportunities for growth:

  * Adjust the portfolio budgets, objectives, and other settings.
  
  * Adjust account/campaign structures to accommodate changes in marketing strategy.
  
  * Add/pause/delete campaign components. This may include expanding keyword sets based on search term analysis, and testing ad copy and landing pages.
  
  * Update geographical- and site-targeting strategies based on advanced performance reports.
  
  * (Optional) Add bidding constraints to individual search keywords or to all keywords in an ad group, campaign, or portfolio.
  
  * Add new portfolios.
  
For instructions on monitoring campaigns and portfolios and adjusting their settings, see "[About managing campaigns and portfolios](/help/search-social-commerce/manage/manage-about.md)" and "[Edit portfolio details](/help/search-social-commerce/manage/portfolios/portfolio-edit.md)."
