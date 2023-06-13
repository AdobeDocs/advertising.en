---
title: Assign classification values to account components using bulksheets
description: Learn how to use bulksheets to assign classification values to account components.
exl-id: 9bb38f28-d6bc-41f4-9c28-b391d9b9e412
---
# Assign classification values to account components using bulksheets

You can associate label classifications with values for the following search entities using bulksheets: campaign, ad group, keyword, ad, placement, unit-level product group, and dynamic search target. Each label classification can have up to 2000 values.

Each entity can have one label value per classification. For example, Shoes_Campaign can have a Color value of "red" and a Geo value of "Los Angeles," but it can't have multiple values for Color or Geo.

Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

>[!NOTE]
>
>Your keywords and ad copy for some ad networks and campaign types are [non-mutable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), which means that editing them deletes the existing entity and creates a new one. When an existing entity is deleted in this way, the label classification isn't assigned to the new entity. 

1. [Download a bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) that includes the entities to which you want to assign label classification values:
   
   * On the [!UICONTROL Rows and Columns] tab, expand the [!UICONTROL Campaign] list in the [!UICONTROL Bulksheet Columns] pane.
   
   * Expand the [!UICONTROL Label Classification] list.
   
   * Select each classification for which you want to include a column in the bulksheet file.
     
     For example, if you include the label classifications "Color" and "Geo," then the bulksheet includes "Color" and "Geo" columns.

1. Open the file in an editor, and add label values to the label classification columns for the entities with which to associate them. The maximum length for each value is 100 characters, and it can include ASCII and non-ASCII characters.

   See the example values in the next section.
   
   Besides adding values, you can also delete existing values by removing them from the relevant rows. To remove values from both a parent entity and its child entities, either a) include only the parent entity row and remove the existing classification value or b) include both the parent entity and its child entities, and remove the existing classification value from all of the parent and child rows.

1. [Upload the file](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) to create the associations.

The uploaded label values are visible in the relevant entity views.

## Example of label classification values to upload in bulksheets

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

>[!MORELIKETHIS]
>
>* [About label classifications](classification-about.md)
>* [Create a label classification](classification-create.md)
>* [Assign classification values to account components from campaign management views](classification-values-assign-campaign-management.md)
>* [Remove label classification values from account components](classification-values-remove.md)
>* [Delete label classification values](classification-values-delete.md)
>* [Delete label classifications](classification-delete.md)
