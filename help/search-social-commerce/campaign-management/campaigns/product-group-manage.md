---
title: Manage shopping product groups
description: Learn how to create and manage shopping product groups in shopping campaigns.
exl-id: 25912abd-1ddb-443f-a16d-7efe57093677
---
# Manage shopping product groups

*[!DNL Google Ads] and [!DNL Microsoft Advertising] shopping campaigns only*

You can create and edit product groups, and delete product groups and their child product groups, in the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] view.

## Create an "[!UICONTROL All Products]" product group

Before you can create product groups with specific attributes, you must first create an all-inclusive product group called "[!UICONTROL All Products]." Each ad group can have only one "[!UICONTROL All Products]" group.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live] > [!UICONTROL Product Groups]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, campaign, and ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [[!DNL Google Ads] product group settings](product-group-settings-google.md) or [[!DNL Microsoft Advertising] product group settings](product-group-settings-microsoft.md).

1. Click **[!UICONTROL Post]**.

## Create a child product group node in an existing product group

Once you've create at least an all-inclusive "[!UICONTROL All Products]" group for an ad group, you can create child product group nodes for subsets of products to include or exclude from bidding, with one or more product groups targeting the same attribute in each level (for example, [!UICONTROL Brand]=Acme for one product group and [!UICONTROL Brand]=AcmePlus for another at the same level. You can create up to seven levels of child product group nodes, not including "[!UICONTROL All Products]".

>[!NOTE]
>
>You can't create a child product group for an "[!UICONTROL Everything Else]" product group.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live] > [!UICONTROL Product Groups]**.

1. (Optional) To view a product group and its child product group nodes in Tree View, hold the cursor over the product group name, click ![Menu icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu icon"), and then select **[!UICONTROL Tree View]**.

1. Hold the cursor over the product group name, click ![Arrow Dropdown Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Arrow Dropdown Menu"), and then select **[!UICONTROL + Add Node]**.

1. Specify the [[!DNL Google Ads] product group settings](product-group-settings-google.md) or [[!DNL Microsoft Advertising] product group settings](product-group-settings-microsoft.md), including the product dimension and attribute.

1. Click **[!UICONTROL Post]**.

## Edit product group node settings

You can edit the bid and tracking template for unit product group nodes (product groups without child product group nodes) that are included for an ad group. You can't edit any information for excluded unit product groups or for included or excluded sub-division nodes, which are product groups with child product group nodes.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live] > [!UICONTROL Product Groups]**.

1. (Optional) To view a product group and its child product group nodes in Tree View, hold the cursor over the product group name, click ![Menu icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu icon"), and then select **[!UICONTROL Tree View]**.

1. Do either of the following:

   1. (To edit settings for a single product group node) Hold the cursor over the product group name, click ![Menu icon](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu icon"), and then select **[!UICONTROL + Edit Node]**.

   1. (To edit settings for one or more ad groups) Do the following:

      1. Select the check box next to each node.

         For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

      1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Edit the [[!DNL Google Ads] product group settings](product-group-settings-google.md) or [[!DNL Microsoft Advertising] product group settings](product-group-settings-microsoft.md).

   For multiple nodes, your changes are applied to all of the selected nodes. For the [!UICONTROL Bid] field, you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit. For the [!UICONTROL Tracking Template] field, you can change existing values to a specified value, replace an existing string with a specified string, add a specified prefix to the beginning of each value, or append a suffix to the end of each value.

1. (Optional) Click **[!UICONTROL Additional Details]** and optionally enter a project name and description.

1. Click **[!UICONTROL Post]**.

## Delete product group nodes

You can delete any product group &mdash; except an "Everything Else" group when other product groups exist at the same level &mdash; that is used to determine which products in your merchant center account are included in the shopping ads for the ad group. Deleting a product group deletes all child product groups.

1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenu, click **[!UICONTROL Live] > [!UICONTROL Product Groups]**.

1. (Optional) Filter the list to include specific product groups.

1. Do either of the following:

   * To delete one product group, click in the **[!UICONTROL Status]** column and select **[!UICONTROL Delete]**.

   * To delete one or more product groups, do the following:

     1. Select the check box next to each product group you want to delete.

        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.

     1. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About shopping product groups](product-group-about.md)
>* [[!DNL Google Ads] product group settings](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] product group settings](product-group-settings-microsoft.md)
