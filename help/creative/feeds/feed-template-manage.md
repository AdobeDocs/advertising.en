---
title: Manage feed templates
description: Learn how to manage feed templates.
feature: Creative Dynamic Creatives
exl-id: 63f8af87-639c-45c8-b17f-99ce19594d35
---
# Manage feed templates

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Feed templates map fields in your feed files/catalogs with fields on the Advertising Creative backend. Dynamic HTML5 and video ads, but not static HTML5 ads, require a feed template to create dynamic ads. You can optionally download and populate master feed templates ([!UICONTROL Retail] and [!UICONTROL Adobe Creative Template]).

You can use a feed template with multiple ad templates.

>[!TIP]
>
>For all accounts with dynamic videos, the best practice is to [download the master feed template [!UICONTROL Adobe Creative Template]](feed-template-manage.md), map each field in the asset file to a field on the Advertising Creative backend, and then rename and upload the feed template. Use the new feed template, along with the asset file, to [create a catalog](catalog-manage.md).

## Create a feed template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. In the upper right, click  **[!UICONTROL Create]** >  **[!UICONTROL Template]**.

1. Specify the [feed template settings](#feed-template-settings).

1. Click **[!UICONTROL Save]**.

## Edit a feed template

**Note:** You can edit only feed templates that you created.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Duplicate]**.

1. Edit the [feed template settings](#feed-template-settings) as needed.

1. Click **[!UICONTROL Save]**.

## View a feed template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL View]**.

## Duplicate a feed template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Duplicate]**.

1. In the [!UICONTROL Duplicate Template] screen, enter a unique **[!UICONTROL Template Name]**. If you're duplicating a template created by someone else, select the **[!UICONTROL Advertiser]**. Optionally edit other [feed template settings](#feed-template-settings) as needed.

1. Click **[!UICONTROL Save]**.

## Download a feed template

Downloaded feed templates are in zipped Microsoft Excel spreadsheet (XLSX) format.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template row and click **[!UICONTROL Download]**.

   The file is downloaded according to your browser's normal procedure.

## Feed template settings {#feed-template-settings}

### [!UICONTROL General] settings

**[!UICONTROL Template Name]:** A unique template name for the specified advertiser.

**[!UICONTROL Advertiser]:** The advertiser who can use the template.

**[!UICONTROL Description]:** (Optional) Information that's helpful to anyone using the feed template.

### [!UICONTROL Field Mapping] settings

Map each field in the feed file to a field on the Advertising Creative backend. See "[Available fields for dynamic ad feed files](/help/creative/appendix-available-feed-fields.md)" for a list of the backend fields and their required attributes.<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

At least one feed file field must be marked as "[!UICONTROL Is Unique]." To add a field mapping, click **[!UICONTROL +]**. To remove the last field mapping, click **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** The field in the feed file.

**[!UICONTROL Description]:** (Optional) Information that's helpful for anyone using the feed template.

**[!UICONTROL Is Unique]:** Indicates that the field is a unique ID (key). At least one field per feed template must be unique. To select this option, click the button to move it to the right.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** The [field on the Advertising Creative backend](/help/creative/appendix-available-feed-fields.md) that maps to the specified [!UICONTROL Field Name] in the feed file.

>[!MORELIKETHIS]
>
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Manage asset files](/help/creative/feeds/asset-manage.md)
>* [Manage catalogs](/help/creative/feeds/catalog-manage.md)
>* [Track the status of catalog processing jobs](/help/creative/feeds/job-status-track.md)
>* [Manage dynamic ad templates](/help/creative/ad-templates/ad-template-manage.md)
>* [Add dynamic creatives to a creative library](/help/creative/creative-libraries/creative-add-dynamic.md)
