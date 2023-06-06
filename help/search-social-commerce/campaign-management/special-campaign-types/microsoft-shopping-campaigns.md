---
title: Implement [!DNL Microsoft® Advertising] shopping campaigns
description: Learn about the workflow for setting up [!DNL Microsoft® Advertising] shopping campaigns.
---
# Implement [!DNL Microsoft® Advertising] shopping campaigns

Ads in shopping campaigns use data about products in your existing [!DNL Microsoft® Merchant Center] product feed, instead of keywords, to decide how and where to show your ads.

[!DNL Microsoft®] shopping campaigns target the [!DNL Microsoft® Advertising Shopping Network]. The settings for shopping campaigns include a specified country in which the products are sold and a priority ([!DNL High], [!DNL Medium], or [!DNL Low]). You can optionally filter your inventory to advertise products with specific attributes, and target or exclude specific locations and device types.

You can control which products are shown with your shopping ads by setting up multi-level *[product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* at the ad group level. Product groups are based on any product attributes (category, product type, brand, condition, product ID, and custom labels), and you can create up to seven levels of product groups to include or exclude from bidding, not including "[!DNL Add Products]." You can set bids at the lowest level of product groups, using the same bid for all matching products. When the same product is included in more than one campaign, [!DNL Microsoft® Advertising] uses the campaign-level priority first to determine which campaign (and associated bid) is eligible for the ad auction. When all of the campaigns have the same priority, the campaign with the highest bid is eligible.

## Steps to set up [!DNL Microsoft® Advertising] shopping campaigns

You can set up shopping campaigns by using [inventory feed templates](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for [!DNL Microsoft® Advertising], by using [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md), or individually. The following instructions include links to creating individual entities.

1. Set up your [!DNL Microsoft® Merchant Center] account and populate it with product data.

1. [Allow Search, Social, & Commerce to download data from the [!DNL Microsoft® Merchant Center] account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [Create a campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) on the shopping network.

1. [Create an ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) within the campaign, and set the default bid for all ads.

  You can override the default bid for individual product groups.

1. Create product groups for the ad group:

   1. [Create an "All Products" product group](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).
   
   1. (Optional) [Create child product groups](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. Create [product ads](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) with [promotion lines to potentially include in each shopping ad](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) within the ad group.

      Microsoft® Advertising dynamically generates the ad copy and the landing page URL for each ad.

      >[!NOTE]
      >
      >Even if the ad group doesn't include ad entities, [!DNL Microsoft® Advertising] still displays ads for the products.

1. (Optional) To track clicks on the ad, [generate a tracking URL using the Tracking URLs tool](/help/search-social-commerce/tools/click-tracking-url-generate.md). The best practice is to add the tracking URL to the [!UICONTROL Tracking Template] field in the account, campaign, or product group settings. For easier maintenance, add it at the highest level possible.

   Alternately, you can add the tracking URL to the product data within the [!DNL Microsoft® Merchant Center] account. To do so, include the tracking URL, together with the value in the "link" or "mobile_link" field, as appropriate, in a custom column "[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)" within the product feed. The value in the "bingads_redirect" field replaces the values in the "link" and "mobile_link" fields. URLs generated using this method don't include any tracking parameters specified in the Search, Social, & Commerce account or campaign settings.

1. Monitor performance by [generating the [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. As necessary:

   1. [Edit the campaign settings](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) to adjust the campaign budget.
   
      If the campaign is part of a portfolio, then the portfolio setting "[!UICONTROL Auto adjust campaign budget limits]" allows Search, Social, & Commerce to optimize the budgets for all campaigns in the portfolio.

   1. Adjust the maximum bid for existing product groups, delete product groups for which you no longer want to create ads, or add a new "all products" product group or new child product groups to create ads for additional products.

>[!NOTE]
>
>* See the required fields for managing [!DNL Microsoft® Shopping] campaigns and product groups using [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) and [inventory feed templates](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* For more information about [!DNL Microsoft® Shopping] campaigns, see the [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/50903).
