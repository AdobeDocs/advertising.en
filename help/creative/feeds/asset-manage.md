---
title: Manage asset files
description: Learn how to upload and manage asset file for an advertiser.
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
---
# Manage asset files

* Dynamic HTML5 ads require a feed file in Microsoft Excel spreadsheet (XLSX) format and the actual image assets that are referenced in the spreadsheet.

* Static HTML5 ads require only a single image asset per ad.

* Video ads require a feed file in Microsoft Excel spreadsheet (XLSX) format and the actual video assets that are referenced in the spreadsheet.

>[!NOTE]
>
> You can use each feed file for only one catalog.

## File requirements

* Dynamic HTML5 ads:

  * A feed file in CSV, TSV, or Microsoft Excel spreadsheet (XLSX) format, with one header row and one data row for each ad variation. Include an image name in each row using the format `images/image_name` (such as `images/300x250_acme_logo.png`).

    The advertiser-specific field names must map to the [available fields for dynamic ad feed files](/help/creative/appendix-available-feed-fields.md).

  * The associated image assets in GIF, JPEG, JPG, or PNG format.<!-- Is this true: The maximum file size is two (2) MB. --> See the [supported creative sizes](/help/creative/creative-libraries/creative-sizes.md).

  You can upload a single XLSX file, a single image file, or a single ZIP file containing any combination of XLSX and image files.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Static HTML5 ads:

  * One image asset per ad in GIF, JPG, JPEG, or PNG format.

    You can upload either a single image or multiple images in a ZIP file.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Dynamic video ads:

  * A feed file in CSV, TSV, or Microsoft Excel spreadsheet (XLSX) format, with one header row and one data row for each ad variation. Include a video name in each row using the format `videos/image_name` (such as `videos/300x250_acme_logo.png`). The ZIP file can be a maximum of 512 MB with a maximum of 500 rows.

    The advertiser-specific field names must map to the [available fields for dynamic ad feed files](/help/creative/appendix-available-feed-fields.md).

  * The associated video assets in MP4, MOV, or WEBM format. Supported ad formats include start card, end card, top overlay, bottom overlay, or L-shaped. Each video's duration must be between 1-90 seconds. See the [supported creative sizes](/help/creative/creative-libraries/creative-sizes.md).

  You can upload a single XLSX file, a single image file, or a single ZIP file containing any combination of XLSX and video files.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Upload an asset file

>[!NOTE]
>
>Instead of uploading asset files, you can also directly upload a catalog when you [add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md). Any catalogs you create there become available within the [!UICONTROL Catalogs] view for future use.

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
>* [Available fields for dynamic ad feed files](/help/creative/appendix-available-feed-fields.md)
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Manage feed templates](/help/creative/feeds/feed-template-manage.md)
>* [Manage catalogs](/help/creative/feeds/catalog-manage.md)
>* [Manage dynamic ad templates](/help/creative/ad-templates/ad-template-manage.md)
>* [Add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md)
