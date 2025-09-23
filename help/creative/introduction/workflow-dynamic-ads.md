---
title: Workflow for dynamic ads
description: Learn about the workflow for managing dynamic ads.
feature: Creative Dynamic Creatives
---
# Workflow for dynamic ads

1. Collect your organization's assets into a feed file.

1. Create an ad template for your dynamic ads based on the assets available.

1. Create catalogs of your assets:

   1. Upload the assets.

      You need to upload both spreadsheet files and image assets to create a feed template, but you can subsequently upload a new spreadsheet file without image assets.<!-- Usually do the file types (xls and image) separately. Vverify this, and what you even do with the image files -- I don't see a mapping of images to a XLSX file -- any image in the assets is used for the xls referece. And is it possible to include actual images -- not just paths/links ot images -- in a spreadsheet? --><!-- xls can include links to AEM assets -- need to --><!-- jpg, jpeg, png -->
   
   1. Create a feed template to map the fields in your asset file (spreadsheet) to fields in the Advertising Creative backend.<!-- clarify this. And does this mean that we have a finite set of supported fields? If so, then I need to doc them. -->

   1. <!-- What is this, and when/how do you use it? And is it specifically for Advertising DSP users?--> Upload mappings of site IDs or placement IDs.

   1. Create a catalog from a specified asset file and a specified feed template, and <!-- manually -->process the catalog.

      You can track the status of catalog processing jobs<!-- only this type of job? --> on the [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] tab.

1. [Create dynamic creatives] for a creative library using a specified ad template and specified catalogs.

1. Create dynamic ad experiences.

1. Create dynamic ad bundles and assign them to your dynamic ad experiences. <!-- order may be off -->

1. Generate and implement ad experience tags.

   To use an ad experience as an ad in Adobe Advertising DSP, upload the ad experience tag to an Advertising DSP campaign. To use an ad experience as an ad in a different DSP, implement the ad experience tag in that DSP.
