---
title: Manage dynamic creatives in Creative Studio
description: Learn how to build, edit, duplicate, and delete catalog-driven dynamic creatives in Adobe Advertising Creative Studio.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage dynamic creatives in [!UICONTROL Creative Studio]

The **[!UICONTROL Creatives]** tab in [!UICONTROL Creative Studio] lists your dynamic creatives by library. From here you can build new catalog-driven dynamic creatives, edit the details and attribute mapping of existing creatives, view change logs, duplicate creatives, and delete creatives.

## Build a dynamic creative {#build-dynamic-creative}

Use this workflow to create catalog-driven dynamic creatives. A four-step guided wizard walks you through selecting a template, connecting a catalog, and mapping catalog fields to template elements. After setup, the [!UICONTROL AI Assistant] helps you to preview and quality-check each ad combination generated from the catalog data.

Dynamic creatives differ from standard ads in a key way: the AI agent can't modify catalog-sourced content. It can filter, analyze, and flag issues &mdash; but to change ad content you must update the source catalog.

### Prerequisites

* At least one user-created display ad template (not a system template) must exist in your template library.
* A product or content catalog (feed) is available in your account.

### Step 1: Open the [!UICONTROL Build Dynamic Creative] wizard {#open-wizard}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Build]** in the **[!UICONTROL Build dynamic creatives from catalog data]** quick action card.

   The four-step **[!UICONTROL Build Dynamic Creative]** dialog opens.

### Step 2: Select a template {#select-template}

>[!NOTE]
>
>The template gallery lists only display ad templates that you created. System templates and video ad templates aren't available as a starting point for dynamic creatives.

1. In the template gallery, click a template to select it.

   The **[!UICONTROL Next]** button is disabled until a template is selected.

1. Click **[!UICONTROL Use this template]**.

### Step 3: Select a catalog {#select-catalog}

1. Configure the creative settings:

   * **[!UICONTROL Ad Library]:** Select the creative library in which to save the creative.
   * **[!UICONTROL Dynamic creative name]:** Enter a name for the dynamic creative.
   * **[!UICONTROL Number of cards]:** Enter the number of catalog offers to include in each ad combination (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (Optional) When enabled, the saved creatives are attached to a bundle. Select a bundle from the library.

1. Select one or more catalogs:

   1. (Optional) Use **[!UICONTROL Catalog template]** to filter the catalog list to a specific template family. To optionally download the template file to review it, click **[!UICONTROL Download feed template]**.

   1. Search for and select catalogs from the list. All selected catalogs must belong to the same catalog template family; a warning appears if you attempt to mix families.

   1. (Optional) To upload a new catalog file, drag and drop the file onto the upload area or click **[!UICONTROL Browse Files]**. Supported formats: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, and MP4. Maximum file size: 25 MB. You can upload one file at a time. Uploaded catalogs appear in the chip list labeled **(uploaded)**.

1. Click **[!UICONTROL Continue]**.

### Step 4: Map catalog fields to template elements {#attribute-mapping}

Map each catalog field to the corresponding element in your template. For example, map the catalog's product name field to the template's headline element, and the product image field to the background image element.

1. Under **[!UICONTROL Targeting]**, select at least one data source for personalizing the creative: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]**, or **[!UICONTROL Audience Segment]**.

1. For each template element, select the matching catalog field from the dropdown.

1. Click **[!UICONTROL Continue]**.

### Step 5: Preview and QA with AI {#qa}

1. Choose whether to *[!UICONTROL Save Dynamic Creative & Skip QA]* or to *[!UICONTROL Continue to QA]*.

   If you continue to QA, the canvas shows all ad combinations generated from the catalog, displayed as rows with a preview of each catalog entry rendered in the template.

1. If you continue to QA:

   1. Do any of the following:

      * Use the **[!UICONTROL Zoom in]** and **[!UICONTROL Zoom out]** controls to adjust the canvas view.
   
      * Use the pagination controls (**X-Y of Z**) to page through catalog rows.

      * To edit an ad combination:
   
        1. Hold the cursor over the catalog row and click **[!UICONTROL Edit]**.
     
        1. In the **[!UICONTROL Edit Row]** dialog, update the field values.
     
        1. Click **[!UICONTROL Save]**.
     
          The canvas refreshes to reflect the updated values.

      * Use the **[!UICONTROL AI Assistant]** chat panel to analyze and filter catalog combinations. Type your request in the **[!UICONTROL Ask anything]** field, or click one of the suggested prompts:

        * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
        * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
        * **[!UICONTROL Show me all ads for millennial women in urban markets]**
     
        The AI agent can:
     
        * Filter the canvas to show ads that match a specific audience segment, geography, language, category, or other catalog field.
        * Check for quality issues such as character-limit overruns, content overflow or bleed, broken image links, and disclaimer visibility.
        * Compare ad combinations for A/B testing analysis.
        * Organize ads into groups for side-by-side review.
     
        The AI agent can't modify catalog-sourced content. To change ad content, update the source catalog.

   1. Save **[!UICONTROL Save Dynamic Creative]** in the header.
   
   1. In the confirmation message, click **[!UICONTROL Create]**.

## Edit a dynamic creative {#edit-dynamic-creative}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   A full-screen editor opens with an ad preview on the left and a settings panel on the right.

1. Edit the creative settings using the **[!UICONTROL Details]** and **[!UICONTROL Attribute Mapping]** tabs:

   **[!UICONTROL Details]** tab:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]**, and **[!UICONTROL Ad template]** are read-only.
   * **[!UICONTROL Dynamic creative name]:** The display name for the creative.
   * **[!UICONTROL Number of cards]:** The number of catalog offers included in each ad combination (1-50).
   * (Optional) Under **[!UICONTROL Catalogs]**, update the catalog selection:
     * Use **[!UICONTROL Catalog template]** to filter available catalogs. To optionally download the template file, click **[!UICONTROL Download feed template]**.
     * Search and select catalogs from the list, or upload a new catalog file by dragging it to the upload area or clicking **[!UICONTROL Browse Files]** (supported formats: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; maximum 25 MB; one file at a time). Uploaded catalogs are labeled **(uploaded)** in the chip list.
     
     All catalogs must belong to the same catalog template family.

   **[!UICONTROL Attribute Mapping]** tab:

   * Under **[!UICONTROL Targeting]**, select at least one data source: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]**, or **[!UICONTROL Audience Segment]**.
   * Under **[!UICONTROL Attribute Mapping]**, update the mapping from each template layer name to the corresponding catalog column label.

1. Click **[!UICONTROL Update Creative]**.

## Re-open the QA assistant for a dynamic creative {#qa-dynamic-creative}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   The QA screen opens. See "[Step 5: Preview and QA with AI](#qa)" for the available canvas controls and AI assistant capabilities.

## View the change log for a dynamic creative {#view-change-log}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Duplicate a dynamic creative {#duplicate-dynamic-creative}

Duplicate a dynamic creative to add a new creative with the same settings to the library. You can later rename the new creative and edit the settings as needed.

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   The new creative is named `<original name> (copy)`.

## Delete a dynamic creative {#delete-dynamic-creative}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Manage templates in Creative Studio](creative-studio-manage-templates.md)
