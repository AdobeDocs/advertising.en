---
title: Manage feed templates
description: Learn how to manage feed templates to XXXX
feature: Creative Dynamic Creatives
---
# Manage feed templates files

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Adk product :  Are these templates typically created by some admin, not the user  (or maybe they were in the past)?  -->

You can use a feed template with multiple ad templates.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Click the **[!UICONTROL Templates]** tab.

1. In the upper right, click  **[!UICONTROL Create]** >  **[!UICONTROL Template]**.

1. Specify the [feed template settings](#feed-template-settings).

1. Click **[!UICONTROL Save]**.

## Edit a feed template

**Note:** You can edit only feed templates that you created.<!-- verify -->

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

1. In the [!UICONTROL Duplicate Template] screen, enter a unique **[!UICONTROL Template Name]** and (if you're duplicating a template created by someone else<!-- verify -->) select the **[!UICONTROL Advertiser]**. Optionally edit other settings as needed.

1. Click **[!UICONTROL Save]**.

## Download a feed template

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

Map each field in the asset file to a field on the Advertising Creative backend.<!-- Check w/product: What is displayed where in the UI/reports and published ads? --> You must include at least one asset file field that is marked as "[!UICONTROL Is Unique]". To add a field mapping, click **[!UICONTROL +]**. To remove the last field mapping, click **[!UICONTROL +]**.

**[!UICONTROL Field Name]:** The field in the asset file.

**[!UICONTROL Description]:** (Optional) Information that's helpful for anyone using the feed template.

**[!UICONTROL Is Unique]:** Indicates the field is a unique ID (key). At least one field per feed template must be unique. To select this option, click the button to move it to the right.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** The field on the Advertising Creative backend that maps to the specified [!UICONTROL Field Name] in the asset file.
