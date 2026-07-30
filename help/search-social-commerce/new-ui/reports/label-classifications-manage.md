---
title: Manage label classifications
description: Learn about using label classifications to group your account components.
feature: Search Label Classifications
---
# Manage label classifications

Label classifications help you group your account components into meaningful sets. For example, you can create a parent label classification called "Geo," create a different label value for each geographical region (such as "United Kingdom" and "Japan") within the classification, and then assign the label values to your [bid units](/help/search-social-commerce/glossary.md#a-b) or parent campaigns. You can then include any label value as a separate column in your views and reports, and subpivot your reports on different classification groups and values.

## Components of label classifications

### Label classifications

Each advertiser can have up to 30 label classifications, which are top-level categories. Once you create a label classification, you can create specific label values for the classification.

### Label values

Each label classification can have up to 2000 values. Once you create specific label values for a classification, you can assign them to campaigns, ad groups, keywords, ads, placements, and product groups [from the campaign management views](#classification-values-assign-campaign-management) or [using bulksheets](#classification-values-assign-bulksheets).

Each eligible entity can have label values for multiple classifications but only one label value per classification. Label values are inherited by child entities but can be overridden. The value assigned at the lowest level always overrides values assigned at parent levels.

## The Labels Classifications view

The [!UICONTROL Reports] > [!UICONTROL Labels Classifications] view includes [!UICONTROL Classifications] and [!UICONTROL Label Values] subviews. By default, data is shown for your keyword-level label classifications and values, but you can optionally view data for your ad-level classifications and values.

## Available actions

* View data for your label classifications.

* View data for your label classification values.

* [Create a label classification](#classification-create).

* Assign classification values to account components [from campaign management views](#classification-values-assign-campaign-management) or [using bulksheets](#classification-values-assign-bulksheets).

* [Remove label classification values from account components](#classification-values-remove).

* [Delete label classification values](#classification-values-delete).

* [Delete label classifications](#classification-delete).

## Create a label classification {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Click **[!UICONTROL Reports] > [!UICONTROL Label Classifications]**.

1. In the upper right, click **[!UICONTROL Create Classification]**.

1. Enter a unique label classification name, and then click **[!UICONTROL Create]**.

   The name must be unique for the advertiser account and consist of [ASCII characters 32-126](https://www.asciitable.com/), and the maximum length is 27 single-byte characters. The name can't be identical to the name of an existing report column or an existing bulksheet column. See the names of bulksheet columns for [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [LY Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Display Network](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), and [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Assign classification values to account components from campaign management views {#classification-values-assign-campaign-management}

You can assign and remove classification values for the following search entities from the campaign management views: campaign, ad group, keyword, ad, placement, unit-level product group, and dynamic search target. If necessary, you can create classifications and classification values during the assignment process. Each label classification can have up to 2000 values.

Each entity can have one label value per classification. For example, Shoes_Campaign can have a Color value of "red" and a Geo value of "Los Angeles," but it can't have multiple values for Color or Geo. 

Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

>[!NOTE]
>
>Your keywords and ad copy for some ad networks and campaign types are [non-mutable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), which means that editing them deletes the existing entity and creates a new one. When an existing entity is deleted in this way, the label classification isn't assigned to the new entity.

1. Open the entity view from the **[!UICONTROL Manage]** or **[!UICONTROL Target]** menu.

1. Select the check box next to each relevant row.

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

## Assign classification values to account components using bulksheets {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

You can associate label classifications with values for the following search entities using bulksheets: campaign, ad group, keyword, ad, placement, unit-level product group, and dynamic search target. Each label classification can have up to 2000 values.

Each entity can have one label value per classification. For example, Shoes_Campaign can have a Color value of "red" and a Geo value of "Los Angeles," but it can't have multiple values for Color or Geo.

Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

>[!NOTE]
>
>Your keywords and ad copy for some ad networks and campaign types are [non-mutable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), which means that editing them deletes the existing entity and creates a new one. When an existing entity is deleted in this way, the label classification isn't assigned to the new entity. 

1. [Download a bulksheet](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md) that includes the entities to which you want to assign label classification values:
   
   * On the [!UICONTROL Rows and Columns] tab, expand the [!UICONTROL Campaign] list in the [!UICONTROL Bulksheet Columns] pane.
   
   * Expand the [!UICONTROL Label Classification] list.
   
   * Select each classification for which you want to include a column in the bulksheet file.
     
     For example, if you include the label classifications "Color" and "Geo," then the bulksheet includes "Color" and "Geo" columns.

1. Open the file in an editor, and add label values to the label classification columns for the entities with which to associate them. The maximum length for each value is 100 characters, and it can include ASCII and non-ASCII characters.

   See the example values in the next section.
   
   Besides adding values, you can also delete existing values by removing them from the relevant rows. To remove values from both a parent entity and its child entities, either a) include only the parent entity row and remove the existing classification value or b) include both the parent entity and its child entities, and remove the existing classification value from all of the parent and child rows.

1. [Upload the file](/help/search-social-commerce/new-ui/set-up/bulksheets/upload.md) to create the associations.

The uploaded label values are visible in the relevant entity views.

### Example of label classification values to upload in bulksheets

This example includes columns for label classifications "Color" and "Geo." For your own bulksheets, substitute columns for your own label classification names.

| Account | Campaign | Ad Group | Keyword | Ad | Placement | Labels | Color | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | Green | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | UK |
| Acct1 | C1 | AG1 | K2 | | | | Red | AU |
| Acct1 | C1 | AG1 | K3 | | | | Blue | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | Red | |
| Acct1 | C1 | AG1 | | | P1 | |Red | AU |
| Acct1 | C1 | AG1 | | | P2 | | Blue | DE |

## Remove label classification values from account components {#classification-values-remove}

Removing a classification value removes the association with the account component and all of its child components. Report data for the classification value is no longer available for those components. Removing a classification value doesn't delete the value nor the account components.

>[!NOTE]
>
>To delete a value from a label classification, see "[Delete label classification values](#classification-values-delete)."

1. Open the entity view from the **[!UICONTROL Manage]** or **[!UICONTROL Target]** menu.

1. Select the check box next to each relevant row.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Select the check box next to each classification value to remove from the selected entities.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   To select all assigned values, click **[!UICONTROL Select All]**. To deselect all assigned valued, click **[!UICONTROL Deselect All]**.

1. Click **[!UICONTROL Unassign Selected]**.

## Delete label classification values {#classification-values-delete}

Deleting label classification values makes them unavailable for future use, and report data is no longer available for the values. All assignments between the values and their parent label classifications and specific account components are removed, but the parent label classifications and the campaign components aren't deleted.

>[!NOTE]
>
>To simply disassociate a classification value from an account component, see "[Remove label classification values from account components](#classification-values-remove)."

1. Click **[!UICONTROL Reports] > [!UICONTROL Label Classifications]**.

1. Click the **[!UICONTROL Label Values]** tab.

1. (Optional) Filter the list to include specific label values.

1. Select the check box next to each label value to delete.
   
   You can delete up to 200 rows at a time.
   
   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Delete label classifications

Deleting a classification removes all associations between its child values and account components. A deleted classification and its values are unavailable for future use. Report data for the classification values is longer available.

>[!NOTE]
>
>To simply disassociate a classification value from an account component, see "[Remove label classification values from account components](#classification-values-remove)."

1. Click **[!UICONTROL Reports] > [!UICONTROL Label Classifications]**.

1. (Optional) Filter the list to include specific label classifications.

1. Select the check box next to each label classification to delete.

   You can delete up to 200 rows at a time.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the bulk actions toolbar, click ![Delete](/help/search-social-commerce/assets/delete.png "Delete").

1. In the confirmation message, click **[!UICONTROL Confirm]**.
