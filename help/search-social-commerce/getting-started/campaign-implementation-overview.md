---
title: Set up ad network accounts and campaigns
description: Follow the setup workflow for ad network connections, campaigns, tracking, conversion metrics, and optional portfolio optimization.
feature: Search Getting Started, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Set up ad network accounts and campaigns

*Beta feature*

[!DNL Adobe] and your agency work with you to connect your ad network accounts, prepare campaigns, configure tracking, and validate performance data. If you want Search, Social, & Commerce to optimize eligible campaigns, the workflow also includes portfolio setup.

This checklist provides the account and campaign details for the broader [implementation workflow](implemention-overview.md). The tasks you can perform depend on your permissions and the [functionality supported for each ad network and campaign type](/help/search-social-commerce/introduction/supported-inventory.md).

## Setup workflow

1. **Confirm access and account requirements.**

   Work with your administrator to confirm access to the appropriate advertiser and the permissions required for your tasks. See "[User administration for Search, Social, & Commerce](/help/search-social-commerce/user-administration.md)."

   If necessary, create the actual ad network account on the ad network's website. Creating an account record in Search, Social, & Commerce doesn't create an account on the ad network.

1. **Connect or register each ad network account.**

   In [!UICONTROL Manage] > [!UICONTROL Accounts], use the workflow for the [account type](/help/search-social-commerce/manage/accounts/ad-network-account-about.md):

   * **API connection:** [Create the account details](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account), complete the network-specific authentication, configure tracking options, and enable the account. Verify its [authentication and access status](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#authentication-status); successful authentication doesn't necessarily mean all required permissions were granted.

   * **Data upload:** [Create the account details and upload campaign and performance data](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md). These accounts don't synchronize with the ad network or support portfolio optimization.

   * **[!DNL Naver] tracking-only:** Follow the [tracking-only account workflow](/help/search-social-commerce/manage/accounts/template-account-manage.md). Use bulksheets to generate tracking URLs and apply them in the ad network's editor; the account doesn't synchronize or support portfolio optimization.

1. **Review or create campaign structure.**

   For API-connected accounts, review the synchronized campaigns and their components. [Request a manual sync](/help/search-social-commerce/manage/accounts/api-accounts/sync-api-accounts.md) when necessary.

   For supported campaign types, use [!UICONTROL Manage] > [!UICONTROL Campaigns] to [create or edit campaigns](/help/search-social-commerce/manage/campaigns/campaign-manage.md). Create the required [ad groups](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md), [ads](/help/search-social-commerce/manage/ads/ad-manage.md), and other supported components. You can also use [bulksheets](/help/search-social-commerce/set-up/bulksheets/about.md) for supported bulk operations.

   Complete any required network-specific setup before activating the campaigns. Manage unsupported components in the ad network's own interface.

1. **Configure and validate tracking before launch.**

   Select the [conversion tracking method](/help/search-social-commerce/tracking/conversion-tracking-about.md) that matches your implementation. When required, [generate and apply click-tracking URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) and [generate conversion-tracking tags](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md).

   Configure any required [integrations](/help/integrations/home.md) or [conversion feeds](/help/search-social-commerce/tracking/tracking-about.md), and validate that conversions can be attributed as expected. For tracking-only campaigns, apply the generated tracking URLs in the ad network's editor.

1. **Review conversion metrics.**

   In [!UICONTROL Goals] > [!UICONTROL Conversions], [review the tracked metrics and make the required metrics visible](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available) for management views, reports, and objectives. Change display names when needed to distinguish metrics.

1. **(Optional) Prepare portfolio optimization.**

   Confirm that the campaigns and their bid strategies are [eligible for portfolio optimization](/help/search-social-commerce/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

   [Create or select an objective](/help/search-social-commerce/goals/objectives/objective-about.md) that uses the appropriate conversion metrics. In [!UICONTROL Manage] > [!UICONTROL Portfolios], [create a portfolio](/help/search-social-commerce/manage/portfolios/portfolio-create.md) or [edit an existing portfolio](/help/search-social-commerce/manage/portfolios/portfolio-edit.md) with the required objective, spending strategy, and optimization settings.

   [Assign the campaigns to the portfolio](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). Each campaign can belong to only one portfolio, and all campaigns in a portfolio must use the same currency.

1. **Validate campaign data and establish a performance baseline.**

   Confirm that cost, click, and conversion data is available for each campaign. Compare conversion data with the appropriate source, including [!DNL Google Ads] and [!DNL Microsoft Advertising] when applicable. Use consistent date ranges and attribution settings when comparing reports.

   For a new portfolio, [activate it](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) to gather and model data. Validate the data and portfolio settings before enabling optimization.

1. **(Optional) Launch portfolio optimization.**

   When the portfolio is ready, [change its status to optimized](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md), reviewing the prerequisites and confirmation messages. Search, Social, & Commerce then optimizes the portfolio according to its settings and the supported campaign bid strategies.

1. **Configure ongoing monitoring and reporting.**

   [Customize your data views](/help/search-social-commerce/common-tasks/data-views/data-views-about.md), [set up custom alerts](/help/search-social-commerce/common-tasks/alerts-manage.md), and [generate scheduled reports](/help/search-social-commerce/reports/management/report-manage.md). When needed, automate reporting using [report templates](/help/search-social-commerce/reports/report-templates-manage.md) and [spreadsheet feeds](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Continue to [monitor and adjust campaigns and portfolios](/help/search-social-commerce/manage/manage-about.md#monitor-performance) after launch.

>[!MORELIKETHIS]
>
>* [Overview of implementing Search, Social, & Commerce](implemention-overview.md)
>* [About managing campaigns and portfolios](/help/search-social-commerce/manage/manage-about.md)
>* [[!DNL Google Ads] conversion data in Search, Social, & Commerce](/help/search-social-commerce/tracking/google-conversion-data.md)
>* [[!DNL Microsoft Advertising] conversion data in Search, Social, & Commerce](/help/search-social-commerce/tracking/microsoft-conversion-data.md)
