---
title: Workflows for dynamic ads
description: Learn about the workflows for managing dynamic ads.
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
---
# Workflows for dynamic ads

*Users with permissions to create dynamic ads*

You can set up dynamic ads in either of two ways:

* Workflow 1: Upload an ad template and ad variation catalog directly within the dynamic ad settings when you add dynamic ads to a creative library. You can download an existing feed template to create the catalog.

  Use this workflow when the same person can provide all of the information (except for the feed template) to create the ads. The uploaded files remain available for future use.

* Workflow 2: Set up an ad template and ad variation catalogs within separate views, and then separately add dynamic ads to a creative using the already-available ad template and catalogs.

  Use this workflow when different people will complete different tasks or when you want to complete only one task at a time.

## Workflow 1

>[!PREREQUISITES]
>
>* Ad templates: A display ad template (a ZIP file with HTML5 files) or a video ad template (a ZIP file with a .scene file and an attribute file (.tdf))
>* Product catalogs in CSV, TSV, or Microsoft Excel spreadsheet (XLSX) format

1. [Create dynamic creatives](/help/creative/creative-libraries/creative-add-dynamic.md) for a creative library. For dynamic HTML5 and video ads, upload or select an existing ad template and catalog.

1. Use the dynamic creatives for ad experiences:

   1. [Create dynamic ad bundles](/help/creative/creative-libraries/bundle-manage.md) that you can attach all at once to an ad experience.
   
   1. Create dynamic ad experiences [with targeting](/help/creative/experiences/experience-create-targeting.md) or [without targeting](/help/creative/experiences/experience-create-no-targeting.md) and [assign the creative bundles to the experiences](/help/creative/experiences/experience-assign-creative-bundles.md).
   
   1. [Generate and implement ad experience tags](/help/creative/experiences/experience-tag-export.md) to run them as ads in your DSP.

      To use an ad experience as an ad in Adobe Advertising DSP, upload the ad experience tag to an Advertising DSP campaign. To use an ad experience as an ad in a different DSP, implement the ad experience tag in that DSP.

## Workflow 2

1. [Create an ad template](/help/creative/ad-templates/ad-template-manage.md) for your dynamic ads based on the assets available. The ad template must be in ZIP format and contain:<!-- Need to add more specs for templates -->

* Display creatives: HTML5 files with the desired ad format and (dynamic HTML5 ads only) a file with the ad attributes (.tdf)

* Video creatives: A .scene file with the desired ad format and a file with the ad attributes (.tdf)

1. Set up your ad elements:

   * (For single static HTML5 ads) Collect and [upload the image assets](/help/creative/feeds/asset-manage.md) for your ads.

   * (For dynamic HTML5 and video ads) Create catalogs of your ad elements:

     1. Create a feed file in Microsoft Excel spreadsheet (XLSX) format, with one row for each ad variation. Include an image or video name in each row. Separately collect the associated image and video assets.

     1. [Upload the feed file and assets](/help/creative/feeds/asset-manage.md).
   
     1. [Create a feed template](/help/creative/feeds/feed-template-manage.md) to map the fields in your feed file (spreadsheet) to fields in the Advertising Creative backend.

     1. [Create a catalog](/help/creative/feeds/catalog-manage.md#feed-catalog-create) from a specified feed file and a specified feed template, and then [process the catalog](/help/creative/feeds/catalog-manage.md#feed-catalog-process) to see the ad variations that can be created from it.

        You can use each feed file for only one catalog.

        You can [track the status of catalog processing jobs](/help/creative/feeds/job-status-track.md) on the [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] tab.

1. [Create dynamic creatives](/help/creative/creative-libraries/creative-add-dynamic.md) for a creative library. For dynamic HTML5 ads, use a specified ad template and specified catalogs.

1. Use the dynamic creatives for ad experiences:

   1. [Create dynamic ad bundles](/help/creative/creative-libraries/bundle-manage.md) that you can attach all at once to an ad experience.
   
   1. Create dynamic ad experiences [with targeting](/help/creative/experiences/experience-create-targeting.md) or [without targeting](/help/creative/experiences/experience-create-no-targeting.md) and [assign the creative bundles to the experiences](/help/creative/experiences/experience-assign-creative-bundles.md).
   
   1. [Generate and implement ad experience tags](/help/creative/experiences/experience-tag-export.md) to run them as ads in your DSP.

      To use an ad experience as an ad in Adobe Advertising DSP, upload the ad experience tag to an Advertising DSP campaign. To use an ad experience as an ad in a different DSP, implement the ad experience tag in that DSP.
