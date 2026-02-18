---
title: Add dynamic creatives to a creative library
description: Learn how to add dynamic creatives to a creative library.
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
---
# Add dynamic creatives to a creative library

Add dynamic creatives to your [creative libraries](creative-library-manage.md) to use with dynamic [ad experiences](/help/creative/experiences/experience-about.md). You can create either a single static HTML5 ad or dynamic HTML5 ads from a single ad template. For dynamic HTML5 ads, use assets in specified catalogs that were created from feed files.

>[!PREREQUISITES]
>
>Before you can add dynamic creatives to a creative library, you must complete other steps &mdash; including creating the ad template, uploading assets, and (dynamic HTML5 ads) creating a feed template and catalog. See "[Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)."

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## Add dynamic creatives using a dynamic HTML5 ad template

1. Do either of the following:

   * From a creative library:

     1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.
     
     1. Click the library name.
     
     1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

   * From an ad template:

     1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.
     
     1. Hold the cursor over the ad template row and click **[!UICONTROL Create Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md):

   1. Specify the basic ad details, including the creative type.
   
   1. Select the ad template to use for the creatives.

      Use an HTML5 ad template for display ads and a video ad template for video ads.
   
   1. Select the catalog from which to build the ads.

   1. Select the criteria for which catalog rows to use to create ads.
   
   1. Map each attribute (dynamic ad field) in the specified ad template to a column in the specified feed file (catalog label), or enter static values.

   1. Click **[!UICONTROL Continue]** to preview the creatives to generate. You can do any of the following within the preview:

      * To filter the creatives by catalog, filter value<!-- explain more-->, and ad size, use the filters above the preview area.
      
      * To search for a product by its unique ID in the search field below the preview area.
      
      * To change the columns that are displayed, click ![Column Filter](/help/creative/assets/custom-columns.png "Column Filter") below the preview area.

      * To preview a specific creative, select the check box for the row.

      * Change the content:
      
        * To edit the value of a cell within the table, click inside the cell and edit the value. Click outside of the cell or press the **[!DNL Enter]** key to save your changes.

        * To mark a single product as the default<!--Explain what this means. -->, hold the curser over the row and click **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.
        
        * (When the ad includes more than one offer) To mark multiple products as the default, select the rows (up to the number of offers) and click **[!UICONTROL Set as Default]** in the bulk actions toolbar.

      * To delete a product from the catalog, hold the curser over the row and click **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.
      
      * (When the ad includes more than one offer) To delete multiple products from the catalog, select the rows (up to the number of offers) and click **[!UICONTROL Delete Row]** in the bulk actions toolbar.

1. Save the creatives:

   * To save the ads and add them to a [creative bundle](/help/creative/creative-libraries/bundle-manage.md) in the library:
   
     1. Click **[!UICONTROL Save and Attach to Bundle]**.

     1. Click **[!UICONTROL Save]** to save the ads.

     1. Select the bundles, and then click **[!UICONTROL Attach Creative to Bundles]**.

   * To save the ads and exit the setup, click **[!UICONTROL Save]**, and then click **[!UICONTROL Save]** again.

>[!MORELIKETHIS]
>
>* [Dynamic creative settings](creative-settings-dynamic.md)
>* [Edit a dynamic creative in a creative library](creative-edit-dynamic.md)
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
