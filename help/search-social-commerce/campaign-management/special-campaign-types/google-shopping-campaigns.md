---
title: Implement [!DNL Google Ads] shopping campaigns
description: Learn about the workflow for setting up [!DNL Google Ads] shopping campaigns.
exl-id: aab61d94-861f-4072-b044-f9ae6759e028
---
# Implement [!DNL Google Ads] shopping campaigns

Ads in shopping campaigns use data about products in your existing [!DNL Google Merchant Center] product feed, instead of keywords, to decide how and where to show your ads.

[!DNL Google Ads] campaigns can target the [!DNL Google Shopping Network] using the [!UICONTROL Campaign Type] "[!UICONTROL Shopping Network]." The settings for [!DNL Google Shopping] campaigns include a priority ([!UICONTROL High], [!UICONTROL Medium], or [!UICONTROL Low]). You can optionally show your local inventory information in your shopping ads using a campaign-level setting.

You can control which products are shown with your shopping ads by setting up multi-level *[product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* at the ad group level. Product groups are based on any product attributes (category, product type, brand, condition, product ID, and custom labels), and you can create up to seven levels of product groups to include or exclude from bidding. You can set bids at the lowest level of product groups, using the same bid for all matching products. When the same product is included in more than one campaign, [!DNL Google Ads] uses the campaign-level priority first to determine which campaign (and associated bid) is eligible for the ad auction. When all of the campaigns have the same priority, the campaign with the highest bid is eligible.

## Steps to set up [!DNL Google Ads] shopping campaigns

You can set up shopping campaigns by using [inventory feed templates](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Google Shopping], by using [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), or individually. The following instructions include links to creating individual entities.

1. Set up your [!DNL Google Merchant Center] account and populate it with product data.

1. [Allow Search, Social, & Commerce to download data from the [!DNL Google Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Create a campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) on the shopping network.

1. [Create an ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) within the campaign, and set the default bid for all ads.

  You can override the default bid for individual product groups.

1. Create product groups for the ad group:

   1. [Create an "All Products" product group](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).
   
   1. (Optional) [Create child product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   >[!NOTE]
   >You don't need to create shopping ads. Even if the ad group doesn't include ad entities, [!DNL Google Ads] still displays ads for the products.

1. (Optional) To track clicks on the ad, [generate a tracking URL using the Tracking URLs tool](/help/search-social-commerce/tools/click-tracking-url-generate.md), and then add it to the account, campaign, or product group settings.

1. Monitor performance by [generating the [!UICONTROL AdWords Shopping Performance Report]](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md) and [the [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. As necessary:

   1. [Edit the campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) to adjust the campaign budget.
   
      If the campaign is part of a portfolio, then the portfolio setting "[!UICONTROL Auto adjust campaign budget limits]" allows Search, Social, & Commerce to optimize the budgets for all campaigns in the portfolio.

   1. [Adjust the maximum bid for existing product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md), [delete product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) for which you no longer want to create ads, or add a [new "all products" product group](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)) or [new child product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md) to create ads for additional products.

>[!NOTE]
>
>* See the required fields for managing [!DNL Google Shopping] campaigns and product groups using [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md) and [inventory feed templates](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md).
>* For more information about [!DNL Google Shopping] campaigns, see the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2454022).
