---
title: Manage asset files
description: Learn how to upload and manage asset file for an advertiser.
feature: Creative Dynamic Creatives
---
# Manage asset files

Dynamic HTML5 ads require both a feed file in Microsoft Excel spreadsheet (XLSX) format and the image assets referenced in the spreadsheet (except for Adobe Experience Manager asset references). Static HTML5 ads require only a single image asset per ad.

>[!NOTE]
>
> You can use each feed file for only one catalog.

## File requirements

* Dynamic HTML5 ads:

  * A feed file in Microsoft Excel spreadsheet (XLSX) format, with one header row and one data row for each ad variation. Include an image name or a reference to an Adobe Experience Manager in each row.<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

    For images you'll upload, reference the image using the format `images/image_name` (such as `images/300x250_acme_logo.png`.)<!-- Verify.  Also need to include the spec for how to reference images in AEM -->

  * The associated image assets in JPEG, JPG, or PNG format.<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. --> See the [supported creative sizes](/help/creative/creative-libraries/creative-sizes.md).

  You can upload a single XLSX file, a single image file, or a single ZIP file containing any combination of XLSX and image files.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Static HTML5 ads:

  * One image asset per ad in JPG, JPEG, or PNG format.

    You can upload either a single image or multiple images in a ZIP file.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Upload an asset file

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Assets]** tab.

1. In the upper right, click  **[!UICONTROL Create]** >  **[!UICONTROL Asset]**.

1. Configure the asset file:

   1. Select the advertiser who can access the asset file.

   1. Specify the asset file in either of the following ways:

      * Drag and drop a file on your device or network into the box.
      
      * Click **[!UICONTROL Select a file]** to locate the file on your device or network.

   1. Click **[!UICONTROL Upload]**.

All ZIP files are decompressed automatically. When you upload a spreadsheet file, the file is listed on the [!UICONTROL Feeds] subtab. When you upload an image file, the image file is listed on the [!UICONTROL Images] subtab.

## Download an asset file

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Assets]** tab.

1. Hold the cursor over the asset row and click **[!UICONTROL Download]**.

   The file is downloaded according to your browser's normal procedure.

## Delete an asset file

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Assets]** tab.

1. Hold the cursor over the asset row and click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Workflow for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Manage feed templates](/help/creative/feeds/feed-template-manage.md)
>* [Manage catalogs](/help/creative/feeds/catalog-manage.md)
>* [Manage dynamic ad templates](/help/creative/ad-templates/ad-template-manage.md)
>* [Add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md)
