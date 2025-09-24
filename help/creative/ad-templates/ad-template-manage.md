---
title: Manage dynamic ad templates
description: Learn about xxxx.
feature: Creative Templates
---
# Manage dynamic ad templates

Create a separate ad template for each combination of ad type (static HTML5 or dynamic HTML5) and ad size. For dynamic HTML5 ads, you also specify the ad attributes.

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Create a dynamic ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. In the upper right, click **[!UICONTROL Create Ad Template]**

1. Specify the [ad template settings](#ad-template-settings)

1. Click **[!UICONTROL Create]**.

## Edit a dynamic ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Hold the cursor over the ad template row and click **[!UICONTROL Edit]**.

1. Edit the [ad template settings](#ad-template-settings).

1. Click **[!UICONTROL Save]**.

## Download a dynamic ad template

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Hold the cursor over the ad template row and click **[!UICONTROL Download]**.

   The file is downloaded according to your browser's normal procedure.

## Delete a dynamic ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Hold the cursor over the ad template row and click **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.<!-- Confirm -->

## Create dynamic ads from an ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

1. Hold the cursor over the ad template row and click **[!UICONTROL Create Dynamic Ad]**.

   In the [!UICONTROL New Dynamic Ad] screen, the [!UICONTROL Ad Template Size], [!UICONTROL Ad Template Type], and [!UICONTROL Ad Template] fields are automatically selected and read-only.

1. Specify the dynamic ad settings to [create the dynamic ads](/help/creative/creative-libraries/creative-add-dynamic.md).

## Ad template settings {#ad-template-settings}

### Ad template details

**[!UICONTROL Advertiser]**: (Read-only for existing templates) The advertiser for which ads will be generated.

**[!UICONTROL Ad Template Name]**: A unique ad template name for the advertiser.

**[!UICONTROL Ad Template Type]**: (Read-only for existing templates) The ad template format: *Static HTML5* or *Dynamic HTML5*.

**[!UICONTROL Ad Template Size]**: (Read-only for existing templates) The dimensions of the ads created by the template.

**[!UICONTROL Description]**: (Optional) Information that's helpful to anyone using the ad template.

### (Static HTML5 templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.<!-- Is this a variable name, and the feed file includes landing page URL for specific variables? -->

### HTML5 zip

<!-- EXPLAIN: The file that contains the XXXXXXXXXXXXXXXXXXXXXX. -->If you already uploaded a file, the filename is listed.

See the [HTML5 creative specification](/help/creative/creative-libraries/html5-creative-specification.md).

To upload a file:

1. Click **[!UICONTROL Upload HTML5 zip]**.

1. Locate the file on your device or network.

### (Dynamic ad templates) Attributes file

<!-- EXPLAIN: The file that contains the XXXXXXXXXXXXXXXXXXXXXX. -->If you already uploaded a file, the filename is listed.

<!-- Add specs for this file type -->

To upload a file:

1. Click **[!UICONTROL Upload Attributes File]**.

1. Locate the file on your device or network.
