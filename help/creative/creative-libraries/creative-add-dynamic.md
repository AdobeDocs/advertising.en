---
title: Add dynamic creatives to a creative library
description: Learn how to add dynamic creatives to a creative library.
feature: Creative Dynamic Creatives
---
# Add dynamic creatives to a creative library

Add dynamic creatives to your [creative libraries](creative-library-manage.md) to use with dynamic [ad experiences](/help/creative/experiences/experience-about.md). You can create either a single static HTML5 ad or dynamic HTML5 ads from a single ad template. For dynamic HTML5 ads, use assets in specified catalogs that were created from feed files.

>[!PREREQUISITES]
>
>Before you can add dynamic creatives to a creative library, you must complete other steps &mdash; including creating the ad template, uploading assets, and (dynamic HTML5 ads) creating a feed template and catalog. See "[Workflow for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)."

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

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md):

   1. Specify the basic ad details.
   
   1. Select the ad template to use for the creatives.
   
   1. Select the catalog from which to build the ads.

   1. Select the criteria for which catalog rows to use to create ads.
   
   1. Map each attribute (dynamic ad field) in the specified ad template to a column in the specified feed file (catalog label).

   1. Click **[!UICONTROL Continue]** to preview the creatives to generate.

      To preview a specific creative, select the check box for the row. Filter the creatives by catalog, filter value<!-- explain more-->, and ad size as needed.

1. Save the creatives:

   * To save the ads and add them to a [creative bundle](/help/creative/creative-libraries/bundle-manage.md) in the library:
   
     1. Click **[!UICONTROL Save and Attach to Bundle]**.

     1. Click **[!UICONTROL Save]** to save the ads.

     1. Select the bundles, and then click **[!UICONTROL Attach Creative to Bundles]**.

   * To just save the ads, click **[!UICONTROL Save]**, and then click **[!UICONTROL Save]** again.

>[!MORELIKETHIS]
>
>* [Dynamic creative settings](creative-settings-dynamic.md)
>* [Edit a dynamic creative in a creative library](creative-edit-dynamic.md)
>* [Workflow for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
