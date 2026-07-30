---
title: Manage shopping product groups
description: Learn about, create, edit, and delete shopping product groups, and reference the product group settings for Google Ads and Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---

# Manage shopping product groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] shopping campaigns only*

You can create and nmanage product groups in the [!UICONTROL Product Groups] view at [!UICONTROL Assets] > [!UICONTROL Shopping].

You can view data about product groups in [the [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md).

## What are product groups?

In shopping campaigns, your product groups &mdash; not keywords &mdash; determine the products in your merchant center account for which shopping ads are displayed. Each product group is based on a single product attribute (such as category, product type, brand, condition, product ID, or custom labels) and uses the same bid for all matching products. You can include or exclude bids for the products in each group.

You configure product groups at the ad group level to determine which products in your merchant center accounts appear in the shopping ads for the ad group. Even if the ad group doesn't include ad entities, the ad network still displays ads for the products.

When the same product is included in more than one campaign, the ad network first uses the campaign priority to determine which campaign (and associated bid) is eligible for the ad auction. When all campaigns have the same priority, the campaign with the highest bid is eligible.

For more information about [!DNL Google] shopping campaigns and ads, see "[Implement [!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)" and the [Google Ads documentation](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). For more information about [!DNL Microsoft] shopping campaigns, see "[Implement [!DNL Microsoft Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)" and the [[!DNL Microsoft Advertising] documentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Support isn't available for [!DNL Google Ads] listing groups in performance max campaigns. To manage and view data for listing groups, use the [!DNL Google Ads] editor.

### Product group hierarchy

Before you can create product groups with specific attributes for an ad group, you must first create an all-inclusive product group called "[!UICONTROL All Products]." From this parent product group, you can create child product groups for subsets of products, and you can create grandchildren from the child product groups. Once you create the first child product group for an ad group, another product group called "[!UICONTROL Everything Else]" is automatically created using the default ad group bid. As you add more product groups, the "[!UICONTROL Everything Else]" group is adjusted accordingly so that it constitutes all products that aren't in another product group.

Within an ad group, you can create up to seven levels of product groups (not including "[!UICONTROL All Products]") to include or exclude from bidding, with one or more product groups targeting the same attribute in each level (for example, [!UICONTROL Brand]=Acme for one product group and [!UICONTROL Brand]=AcmePlus for another at the same level). Parent product groups are called subdivisions, and the lowest level of subdivision is known as a unit. You can set bids and tracking templates, or completely exclude bidding, at the unit level. The entire set of active product groups for an ad group is applied hierarchically to determine the eligible products. For example, if you subdivide [!UICONTROL All Products] into [!UICONTROL Brand]=AcmeBasic and [!UICONTROL Brand]=AcmePlus, and then you further subdivide each of those product groups into [!UICONTROL Condition]=New and set bids, then only new products with the AcmeBasic and AcmePlus brands may be advertised or excluded from ads.

![Example of a product group set](/help/search-social-commerce/assets/product-group-list-new.png "Example of a product group set")

![Example product group hierarchy](/help/search-social-commerce/assets/product-group-tree-new.png "Example product group hierarchy")

### Product filters {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

See also the [!DNL Google Ads] help "[Manage a shopping campaign with product groups](https://support.google.com/google-ads/answer/6275317)" and the [!DNL Microsoft Advertising] help "[Understand and use product groups](https://help.ads.microsoft.com/#apex/bae/en/56782)."

| Shopping Network | Product Dimension | Attributes | Notes |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] to [!UICONTROL Category 5=] | \[The category ID\] | &mdash; |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[The brand\] | &mdash; |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[The item ID\] | &mdash; |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | &mdash; |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] to [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[The product type\] | &mdash; |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] to [!UICONTROL Custom Label 4=] | \[The attribute for the custom label\] | &mdash; |
| [!DNL Google Ads] | Channel= | [!UICONTROL Local], [!UICONTROL Online] | To show ads for local products or online products only.<br><br><b>Note:</b> To create ads for local products, the &quot;Local Inventory Ads&quot; option must be enabled, and you must be participating in the local shopping program with [!DNL Google Merchant Center]. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Whether to show ads for products that are available only for a single channel (either only local or only online) or are available for multiple channels (both local and online). |

## The [!UICONTROL Product Groups] view

The [!UICONTROL Product Groups] view at [!UICONTROL Assets] > [!UICONTROL Shopping] view lists all product groups in the filtered view for the selected advertiser account. You can also create and manage product groups.

### Available actions <!-- Go through all -->

* [Create an "[!UICONTROL All Products]" product group](#product-group-create-all-products)

* [Create a child product group node in an existing product group](#node-add)

* Edit settings for a product group node:

  * [Edit any settings](#node-edit)

  * [Edit only the [!UICONTROL Tracking Template]](#node-edit-tracking-template)

  * [Edit only the [!UICONTROL Max CPC]](#node-edit-maxcpc)

* [Delete a product group node](#node-delete)

* [Assign constraints](#constraint-assign) to product groups, and [remove constraints](#constraint-unassign) from product groups

* [Assign label classifications](#classification-values-assign) to product groups, and [remove label classifications](#classification-values-remove) from product groups

>[!NOTE]
>
>You can create and edit large amounts of product group data (including labels and constraint assignments) at once by uploading [bulksheet files](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) and posting them to the ad network.

## Create an "[!UICONTROL All Products]" product group {#product-group-create-all-products}

Before you can create product groups with specific attributes, you must first create an all-inclusive product group called "[!UICONTROL All Products]." Each ad group can have only one "[!UICONTROL All Products]" group.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. In the toolbar above the data table, click **[!UICONTROL Create Product Group]**.

1. Select the ad network, the account, campaign, and ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [Google Ads product group settings](#google-ads-product-group-settings) or [Microsoft Advertising product group settings](#microsoft-advertising-product-group-settings).

1. Click **[!UICONTROL Review and Save]**.

1. If necessary, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit") and change the [Google Ads product group settings](#google-ads-product-group-settings) or [Microsoft Advertising product group settings](#microsoft-advertising-product-group-settings).

1. Click **[!UICONTROL Create]**.

## Create a child product group node in an existing product group {#product-group-create-child}

Once you've create at least an all-inclusive "[!UICONTROL All Products]" group for an ad group, you can create child product group nodes for subsets of products to include or exclude from bidding, with one or more product groups targeting the same attribute in each level (for example, [!UICONTROL Brand]=Acme for one product group and [!UICONTROL Brand]=AcmePlus for another at the same level. You can create up to seven levels of child product group nodes, not including "[!UICONTROL All Products]".

>[!NOTE]
>
>You can't create a child product group for an "[!UICONTROL Everything Else]" product group.

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. (Optional) To view a product group and its child product group nodes in Tree View, hold the cursor over the product group name, click **[!UICONTROL ...] > [!UICONTROL Tree View]**.

1. Hold the cursor over the product group name, and click **[!UICONTROL ...] > [!UICONTROL + Add Node]**.

1. Specify the [Google Ads product group settings](#google-ads-product-group-settings) or [Microsoft Advertising product group settings](#microsoft-advertising-product-group-settings).

1. Click **[!UICONTROL Center]**.

## Edit any settings for a product group node {#node-edit}

You can edit the bid and tracking template for unit product group nodes (product groups without child product group nodes) that are included for an ad group. You can't edit any information for excluded unit product groups or for included or excluded sub-division nodes, which are product groups with child product group nodes.

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. (Optional) To view a product group and its child product group nodes in Tree View, hold the cursor over the product group name, click **[!UICONTROL ...] > [!UICONTROL Tree View]**.

1. Hold the cursor over the product group name, and click **[!UICONTROL ...] > [!UICONTROL + Edit Node]**.

1. Edit the [Google Ads product group settings](#google-ads-product-group-settings) or [Microsoft Advertising product group settings](#microsoft-advertising-product-group-settings).

1. Click **[!UICONTROL Update]**.

## Edit only the [!UICONTROL Tracking Template] for a product group node {#node-edit-tracking-template}

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Hold the cursor over the product group name, and click **[!UICONTROL ...] > [!UICONTROL Tree View]** to view the product group and its child product group nodes in Tree View.

1. In the **[!UICONTROL Tracking Template]** column, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit").

1. Change the **[!UICONTROL Tracking Template]** value, and then click **[!UICONTROL Save]**.

## Edit only the [!UICONTROL Max CPC] for a product group node {#node-edit-maxcpc}

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Hold the cursor over the product group name, and click **[!UICONTROL ...] > [!UICONTROL Tree View]** to view the product group and its child product group nodes in Tree View.

1. In the **[!UICONTROL Max CPC]** column, click ![Edit](/help/search-social-commerce/assets/edit-new.png "Edit").

1. Change the **[!UICONTROL Max CPC]** value, and then click **[!UICONTROL Save]**.

## Delete a product group node {#node-delete}

You can delete any product group &mdash; except an "Everything Else" group when other product groups exist at the same level &mdash; that is used to determine which products in your merchant center account are included in the shopping ads for the ad group. Deleting a product group deletes all child product groups.

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Hold the cursor over the product group name, and click **[!UICONTROL ...] > [!UICONTROL Tree View]** to view the product group and its child product group nodes in Tree View.

1. Click in the **[!UICONTROL Status]** column and select **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## Assign a constraint to selected product groups {#constraint-assign}

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Select the check box next to each product group to which you'll assign a single constraint.

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Select the constraint.

1. Click **[!UICONTROL Assign Now]**.

## Remove constraints from selected product groups {#constraint-unassign} 

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Select the check box next to each product group from which you'll unassign constraints.

1. In the bulk actions toolbar, click **- [!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Click **[!UICONTROL Confirm]**.

## Assign classification values to product groups {#classification-values-assign}

>[!NOTE]
>
>Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Select the check box next to each product group to which you'll assign a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **+ [!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. For each applicable classification value, do the following:

   1. In the **[!UICONTROL Classifications]** column, specify the classification:
     
      * To use an existing classification, click the classification name to expand it.
     
      * To create a classification, click [!UICONTROL +] in the column heading. In the input field, enter the classification name, and then click ![Save](/help/search-social-commerce/assets/save-checkmark.png "Save") to immediately save the classification. To use the new classification, click the classification name to expand it.
        
        The name must consist of [ASCII characters 32-126](https://www.asciitable.com/), and the maximum length is 27 single-byte characters.
   
   1. In the **[!UICONTROL Value Name]** column, specify the value for the selected classification:
   
      * To use an existing value, select the value.
      
      * To create a value, click [!UICONTROL +] in the column heading. In the input field, enter the value, and then click ![Save](/help/search-social-commerce/assets/save-checkmark.png "Save") to immediately save the value and select it by default.

        The maximum length is 100 characters, and it can include ASCII and non-ASCII characters.

1. Click **+ [!UICONTROL Assign Now]**.

## Remove label classification values from product groups {#classification-values-remove}

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

1. In the main menu, click **[!UICONTROL Assets] > [!UICONTROL Shopping]**.

1. Select the check box next to each product group from which you'll remove a label value.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned valued, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] product group settings {#google-ads-product-group-settings}

### "All Product" product groups

**[!UICONTROL Network]:** (New product groups only) The ad network.

**[!UICONTROL Account]:** (New product groups only) The ad network account name.

**[!UICONTROL Campaign]:** (New product groups only) The campaign.

**[!UICONTROL Ad Group]:** (New product groups only) The ad group.

**[!UICONTROL Condition]** or **[!UICONTROL Condition Type]:** (Read-only) All Products

**[!UICONTROL Condition Value]:** (Existing product groups only) &nbsp;

**[!UICONTROL Bid]** or **[!UICONTROL Max CPC]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

{{$include /help/_includes/tracking-template-google.md}}

This template overrides templates at higher levels and is used only for units without child product groups. Any append parameters specified for the account or campaign aren't included. Any append parameters specified for the account or campaign aren't included.

### All other product groups

**[!UICONTROL Condition Type]** and **[!UICONTROL Condition Value]:** (Read-only for existing product groups) The product dimensions to target. For new product groups, enter the dimension by which to target products, and the qualifying attribute for the selected information category (such as "Acme" when you are targeting by brand, or "New" when you are targeting by condition).

Once you create a product group for specific product dimensions (that is, not "All Products"), Search, Social, & Commerce automatically creates a product group for "Everything Else."

For a list of available product dimensions, see "[Product filters](#product-filters)." Your list of dimensions may be limited based on the campaign's [!UICONTROL Inventory Filter] setting.

**[!UICONTROL Excluded]:** (Optional for new product groups; read-only for existing product groups) Excludes bids on ads for matching products.

**[!UICONTROL Max CPC]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

This template overrides templates at higher levels and is used only for units without child product groups.

## [!DNL Microsoft Advertising] product group settings {#microsoft-advertising-product-group-settings}

### "All Product" product groups

**[!UICONTROL Network]:** (New product groups only) The ad network.

**[!UICONTROL Account]:** (New product groups only) The ad network account name.

**[!UICONTROL Campaign]:** (New product groups only) The campaign.

**[!UICONTROL Ad Group]:** (New product groups only) The ad group.

**[!UICONTROL Condition]** or **[!UICONTROL Condition Type]:** (Read-only) All Products

**[!UICONTROL Condition Value]:** (Existing product groups only) &nbsp;

**[!UICONTROL Bid]** or **[!UICONTROL Max CPC]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

**[!UICONTROL Base URL]:** (New product groups only) Not used<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

This template overrides templates at higher levels and is used only for units without child product groups.

### All other product groups

**[!UICONTROL Condition Type]** and **[!UICONTROL Condition Value]:** (Read-only for existing product groups) The product dimensions to target. For new product groups, enter the dimension by which to target products and the qualifying attribute for the selected information category (such as "Acme" when you are targeting by brand, or "New" when you are targeting by condition).

Once you create a product group for specific product dimensions (that is, not "All Products"), Search, Social, & Commerce automatically creates a product group for "Everything Else."

For a list of available product dimensions, see "[Product filters](#product-filters)." Your list of dimensions may be limited based on the campaign's [!UICONTROL Inventory Filter] setting.

**[!UICONTROL Excluded]:** (Optional for new product groups; read-only for existing product groups) Excludes bids on ads for matching products.

**[!UICONTROL Max CPC]:** (Included product groups only) The maximum cost per click (CPC), which is the highest amount to pay for an ad click. This value is used only for units without child product groups, and it's used instead of the ad group-level value.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

This template overrides templates at higher levels and is used only for units without child product groups.

>[!MORELIKETHIS]
>
>* [Implement [!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implement [!DNL Microsoft Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [The [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
