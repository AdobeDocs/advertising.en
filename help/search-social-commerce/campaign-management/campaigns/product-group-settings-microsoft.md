---
title: '[!DNL Microsoft® Advertising] product group settings'
description: Reference the settings for [!DNL Microsoft® Advertising] shopping product groups.
exl-id: a34511ef-f5bc-4d93-a56e-90348f670ad6
feature: Search Campaign Management
---
# [!DNL Microsoft® Advertising] product group settings

## "All Product" product groups

**[!UICONTROL Condition]:** (Read-only) All Products

**[!UICONTROL Bid]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

This template overrides templates at higher levels and is used only for units without child product groups.

## All other product groups

**[!UICONTROL Condition/Value]:** (Read-only for existing product groups) The product dimensions to target. For new product groups, enter the dimension by which to target products and the qualifying attribute for the selected information category (such as "Acme" when you are targeting by brand, or "New" when you are targeting by condition).

Once you create a product group for specific product dimensions (that is, not "All Products"), Search, Social, & Commerce automatically creates a product group for "Everything Else."

For a list of available product dimensions, see "[Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)." Your list of dimensions may be limited based on the campaign's [!UICONTROL Inventory Filter] setting.

**[!UICONTROL Excluded]:** (Optional for new product groups; read-only for existing product groups) Excludes bids on ads for matching products.

**[!UICONTROL Bid]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

This template overrides templates at higher levels and is used only for units without child product groups.

>[!MORELIKETHIS]
>
>* [About shopping product groups](product-group-about.md)
>* [Manage shopping product groups](product-group-manage.md)
>* [Shopping campaign product filters](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implement [!DNL Microsoft® Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
