---
title: About shopping product groups
description: Learn about shopping product groups in shopping campaigns.
exl-id: c91e6fb5-3be1-4d21-b508-09f974058fc7
---
# About shopping product groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] shopping campaigns only*

In shopping campaigns, your product groups &mdash; not keywords &mdash; determine the products in your merchant center account for which shopping ads are displayed. Each product group is based on a single product attribute (such as category, product type, brand, condition, product ID, or custom labels) and uses the same bid for all matching products. You can include or exclude bids for the products in each group.

You configure product groups at the ad group level to determine which products in your merchant center accounts appear in the shopping ads for the ad group. Even if the ad group doesn't include ad entities, the ad network still displays ads for the products.

When the same product is included in more than one campaign, the ad network first uses the campaign priority to determine which campaign (and associated bid) is eligible for the ad auction. When all of the campaigns have the same priority, the campaign with the highest bid is eligible.

For more information about [!DNL Google] shopping campaigns and ads, see "[Implement [!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)" and the [Google Ads documentation](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). For more information about Microsoft shopping campaigns, see "[Implement [!DNL Microsoft® Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)" and the [Microsoft Advertising documentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Support isn't available for [!DNL Google Ads] listing groups in performance max campaigns, which are replacing smart shopping campaigns. To manage and view data for listing groups, use the [!DNL Google Ads] editor.

## Product group hierarchy

Before you can create product groups with specific attributes for an ad group, you must first create an all-inclusive product group called "[!UICONTROL All Products]." From this parent product group, you can create child product groups for subsets of products, and you can create grandchildren from the child product groups. Once you create the first child product group for an ad group, another product group called "[!UICONTROL Everything Else]" is automatically created using the default ad group bid. As you add more product groups, the "[!UICONTROL Everything Else]" group is adjusted accordingly so that it constitutes all products that aren't in another product group.

Within an ad group, you can create up to seven levels of product groups (not including "[!UICONTROL All Products]") to include or exclude from bidding, with one or more product groups targeting the same attribute in each level (for example, [!UICONTROL Brand]=Acme for one product group and [!UICONTROL Brand]=AcmePlus for another at the same level). Parent product groups are called subdivisions, and the lowest level of subdivision is known as a unit. You can set bids and tracking templates, or completely exclude bidding, at the unit level. The entire set of active product groups for an ad group is applied hierarchically to determine the eligible products. For example, if you subdivide [!UICONTROL All Products] into [!UICONTROL Brand]=AcmeBasic and [!UICONTROL Brand]=AcmePlus, and then you further subdivide each of those product groups into [!UICONTROL Condition]=New and set bids, then only new products with the AcmeBasic and AcmePlus brands may be advertised or excluded from ads.

![Example of a product group set](/help/search-social-commerce/assets/product-group-list.png "Example of a product group set")

![Example product group hierarchy](/help/search-social-commerce/assets/product-group-tree.png "Example product group hierarchy")
 
## The [!UICONTROL Product Groups] view

You can create and edit product groups, and delete product groups and their child product groups, in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] view.

## Tracking and performance data for shopping product groups

(Accounts/campaigns with the "[!UICONTROL EF Redirect]" tracking option) To allow Search, Social, & Commerce to track conversions for product groups, [generate tracking URLs for product groups using the Tracking URLs tool](/help/search-social-commerce/tools/click-tracking-url-generate.md), and then do one of the following:

* (Required for [!DNL Google Ads]; best practice for [!DNL Microsoft Advertising]) Add the tracking URL to the [!DNL Tracking Template] field in the account, campaign, or product group setting. For easier maintenance, add them at the highest level possible. Any append parameters specified for the account or campaign aren't included. 
 
  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Use this option only when you don't include Search, Social, & Commerce tracking URLs in a custom column within the product feed. If you do both, the URLs will include two redirects and will cause broken links.

* ([!DNL Microsoft Advertising] only) Add the tracking URL to the product data within the [!DNL Microsoft Merchant Center] account. To do so, include the tracking URL, together with the value in the `link` or `mobile_link` field, as appropriate, in a custom column called [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) within the product feed. URLs generated using this method don't include any tracking parameters specified in the account or campaign settings within Search, Social, & Commerce.

You can view data about product groups in [the [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Manage shopping product groups](product-group-manage.md)
>* [[!DNL Google Ads] product group settings](product-group-settings-google.md)
>* [Implement [!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] product group settings](product-group-settings-microsoft.md)
>* [Implement [!DNL Microsoft® Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
