---
title: Dynamic creative settings
description: Reference the settings for dynamic creatives.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
---
# Dynamic creative settings

<!-- add a description -->

## Dynamic ad settings<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Basic Details

**[!UICONTROL Creative Type]:** Whether the creative is a *[!UICONTROL Display]* ad (HTML5) or a *[!UICONTROL Video]* ad.

**[!UICONTROL Dynamic Display Ad Name]** or **[!UICONTROL Dynamic Video Ad Name]:** A unique name for the creative.

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads. If you're creating the ads from within [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], then the advertiser is already selected and read-only.

**[!UICONTROL Library]:** The creative library in which to create the ads. If you're creating the ads from within [!UICONTROL Creatives] > [!UICONTROL Creative Libraries], then the library name is already selected and read-only.

## Ad Template

**[!UICONTROL Ad Template]:** The ad template from which to create the ads. Select an existing ad template, or upload a new ad template and select the template type (*Static* or *Dynamic*). The template must be in ZIP format and contain:<!-- Need to add more specs for templates -->

* Display creatives: HTML5 files with the desired ad format and (dynamic HTML5 ads only) a file with the ad attributes (.tdf)

* Video creatives: A .scene file with the desired ad format. The ZIP file can be a maximum of 512 MB.

To continue, click **[!UICONTROL Select Ad Template]**. 

**[!UICONTROL Size]:** (Dynamic display ads only; read-only) The [ad dimensions](/help/creative/creative-libraries/creative-sizes.md) for the selected ad template, which is used to create the ads.

**[!UICONTROL Card Count (Max 50)]:** (Display ads only) The number of products to show in a carousel.

**[!UICONTROL Duration]:** (Video ads only; read-only) The video duration derived from the selected ad template. Each video's duration must be between 1-90 seconds.

## Catalogs

**\[Catalogs\]**: One or more catalogs from which to generate ads. Select an existing catalog, or create a new catalog by downloading an existing feed template and creating and uploading the new catalog. Click **[!UICONTROL Select Catalog]**.

Uploaded catalogs must be in ZIP format and contain the following:

* (Dynamic display and video ads) One or more feed files in CSV, TSV, or Microsoft Excel spreadsheet (XLSX) format. The maximum file size is 512 MB.<!-- Need to add more specs for the feed files -->

* (Display ads) Image assets in GIF, JPEG, JPG, or PNG format

* (Video ads) Video assets in MP4, MOV, or WEBM format. Supported ad templates include start card, end card, top overlay, bottom overlay, or L-shaped. Each video's duration must be between 1-90 seconds.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->The types of columns in the feed file for which values must be present to create ads: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Note:** These settings work independently from the advanced settings in ad experience settings.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Map each attribute (dynamic ad field) in the specified ad template to a column in the specified catalog (catalog label) or enter a static value.

>[!MORELIKETHIS]
>
>* [Add dynamic creatives to a creative library](creative-add-dynamic.md)
>* [Edit dynamic creatives in a creative library](creative-edit-dynamic.md)
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
