---
title: Assign classification values to account components from campaign management views
description: Learn how to assign classification values to account components.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
---
# Assign classification values to account components from campaign management views

You can assign and remove classification values for the following search entities from the campaign management views:  campaign, ad group, keyword, ad, placement, unit-level product group, and dynamic search target. If necessary, you can create classifications and classification values during the assignment process. Each label classification can have up to 2000 values.

Each entity can have one label value per classification. For example, Shoes_Campaign can have a Color value of "red" and a Geo value of "Los Angeles," but it can't have multiple values for Color or Geo. 

Label values are inherited by child entities, so don't enter values for child entities unless you want to override the inherited values.

>[!NOTE]
>
>Your keywords and ad copy for some ad networks and campaign types are [non-mutable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), which means that editing them deletes the existing entity and creates a new one. When an existing entity is deleted in this way, the label classification isn't assigned to the new entity.

1. Click **[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**, and then select the account component view.

1. Do either of the following:
   
   * (To assign values to a single entity) Hold the cursor over the entity name, click ![Menu button](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menu button"), and then select **[!UICONTROL Classification]**.
   
   * (To assign values to one or more entities) Do the following:

     * Select the check box next to each relevant row.
       
       For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
    
     * In the toolbar above the data table, click ![More](/help/search-social-commerce/assets/more.png "More"), and then click **[!UICONTROL Classification]**.

1. In the [!UICONTROL Assignment Details], do any of the following:

   * To change any existing classifications values to new values, select **[!UICONTROL Set To]**.
     
     The maximum length for each value is 100 characters, and it can include ASCII and non-ASCII characters.
   
   * To assign specified classification values without removing existing values, select **[!UICONTROL Assign]**.
   
   * To remove specific, currently-assigned classification values, select **[!UICONTROL Remove]**.
     
     When you remove a classification value, report data for the value is no longer available for the specified account components. 
   
   * To delete specified classification values, select **[!UICONTROL Delete]**.

     Deleting a classification value makes it unavailable for future use, and report data is no longer available for the value. All assignments between the values and specific account components are removed, but the account components aren't deleted.

1. For each applicable classification value, do the following:

   1. In the **[!UICONTROL Classification]** column, specify the classification name:
     
      * To use an existing classification, click the classification name to expand it.
     
      * To create a classification, click [!UICONTROL +]. In the input field, enter the classification name, and then click ![Save](/help/search-social-commerce/assets/select.png "Save") to immediately save the classification.
        
        The name must consist of [ASCII characters 32-126](https://www.asciitable.com/), and the maximum length is 27 single-byte characters.
   
   1. In the **[!UICONTROL Value Name]** column, specify the name of the value:
   
      * To use an existing value, click the value name to select it.
      
      * To create a value, click [!UICONTROL +]. In the input field, enter the value, and then click ![Save](/help/search-social-commerce/assets/select.png "Save") to immediately save the value.

        The maximum length is 100 characters, and it can include ASCII and non-ASCII characters.

1. (Optional) Enter additional details:
   
   1. Next to **[!UICONTROL Additional Details]**, click ![Open](/help/search-social-commerce/assets/chevron-up.png "Open") to expand the details.
   
   1. Enter an optional **[!UICONTROL Project Name]** and/or optional **[!UICONTROL Description]**.

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [About label classifications](classification-about.md)
>* [Create a label classification](classification-create.md)
>* [Assign classification values to account components using bulksheets](classification-values-assign-bulksheets.md)
>* [Remove label classification values from account components](classification-values-remove.md)
>* [Delete label classification values](classification-values-delete.md)
>* [Delete label classifications](classification-delete.md)
