---
title: Manage dynamic creatives in Creative Studio
description: Learn how to build, quality-check, edit, duplicate, and delete catalog-driven dynamic creatives in Adobe Advertising Creative Studio.
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

The **[!UICONTROL Creatives]** tab in [!UICONTROL Creative Studio] lists your dynamic creatives by library. From here you can build new catalog-driven dynamic creatives, quality-check creatives with AI, edit the details and attribute mapping of existing creatives, view change logs, duplicate creatives, and delete creatives.

## Build a dynamic creative {#build-dynamic-creative}

Use this workflow to create catalog-driven dynamic creatives. A four-step guided wizard walks you through selecting a template, connecting a catalog, and mapping catalog fields to template elements. After setup, the [!UICONTROL AI Assistant] helps you to preview and quality-check each ad combination generated from the catalog data.

Dynamic creatives differ from standard ads in a key way: the AI agent can't modify catalog-sourced content. It can filter, analyze, and flag issues &mdash; but to change ad content you must update catalog values manually, either from the QA screen or in the source catalog.

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

   If you continue to QA, the **[!UICONTROL Dynamic Creative QA]** screen opens with a preview canvas and the **[!UICONTROL AI Assistant]** chat panel.

1. If you continue to QA, follow the procedures in "[Quality-check a dynamic creative](#qa-dynamic-creative)" to [analyze and filter ads](#analyze-ads), [review previews and alerts](#review-previews), and optionally [correct catalog values](#correct-catalog-values). When you're finished, [save the dynamic creative](#save-or-exit).

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

## Quality-check a dynamic creative {#qa-dynamic-creative}

Use the QA Agent to analyze catalog rows against a dynamic creative's template, preview the resulting ads, and identify potential content issues. You can filter and group ads using the **[!UICONTROL AI Assistant]**, review catalog alerts, and manually correct catalog values before publishing the changes.

The agent opens the **[!UICONTROL Dynamic Creative QA]** screen from either [!UICONTROL Creative Libraries] or [!UICONTROL Creative Studio]. Although the menu labels differ, both entry points provide the same QA functionality. The analysis depends on the selected creative, catalog, and request.

>[!NOTE]
>
>The QA Agent is available for dynamic display creatives, not standard creatives or dynamic video creatives. In [!UICONTROL Creative Libraries], the action is available only for dynamic creatives based on dynamic templates.

### Open the QA Agent {#open-qa-agent}

1. Open a saved dynamic creative for QA in either of the following ways:

   * **From [!UICONTROL Creative Libraries]:**

     1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Click the library name to open the library.

     1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL ...]** next to the dynamic creative name, and then click **[!UICONTROL QA Agent]**.

   * **From [!UICONTROL Creative Studio]:**

     1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

     1. On the **[!UICONTROL Creatives]** tab, locate the dynamic creative in its creative library below the [!UICONTROL Generate or Build Creatives] section.

     1. Hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   The **[!UICONTROL Dynamic Creative QA]** screen opens with a preview canvas and the **[!UICONTROL AI Assistant]** chat panel.

1. If the creative uses multiple catalogs, select the catalog to review from **[!UICONTROL Catalog]** in the header.

   The assistant analyzes the selected catalog. The catalog selector is disabled when the creative uses only one catalog.

### Analyze and filter ads with AI {#analyze-ads}

1. In the **[!UICONTROL AI Assistant]** panel, type a request in **[!UICONTROL Ask anything]** and press **[!UICONTROL Enter]**, or click one of the suggested prompts:

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   The assistant responds in the chat panel and displays matching catalog rows as ad previews on the canvas. Until you submit a request, the canvas prompts you to ask the assistant to analyze the catalog.

1. Continue refining the review with follow-up requests. The assistant can help you:

   * Filter ads by audience segment, language, geography, or zip code.
   * Check character lengths using a threshold that you specify.
   * Check for feed errors, missing content, and suspicious content.
   * Review translation status.
   * Compare A/B test variants.
   * Group ads for review, such as by product or issue.

   Verify the assistant's responses and inspect the previews before saving changes.

### Review previews and alerts {#review-previews}

* Use the canvas toolbar to:

  * Adjust the zoom.
  * Switch between **[!UICONTROL Thumbnail view]** and **[!UICONTROL Actual size]**.
  * Click **[!UICONTROL Replay animations]** to replay the previews.
  * Select the number of rows per page, select a page number, or use **[!UICONTROL Previous page]** and **[!UICONTROL Next page]**.

* When the assistant groups results, click the link to view all creatives in a group. Use **[!UICONTROL Back to groups]** to return to the grouped results, or **[!UICONTROL Catalog Rows]** to leave the grouped view.

* When a preview shows **[!UICONTROL Issues detected]**, hold the cursor over the indicator to view the issue details.

* When catalog alerts are available, click **[!UICONTROL View Alerts]**. The **[!UICONTROL Alerts]** dialog lists the catalog, row number, column, and error message for each issue. Click **[!UICONTROL Close]** to return to the canvas.

### Correct catalog values {#correct-catalog-values}

You can manually edit catalog values from an ad preview without leaving the QA screen.

1. On the preview that you want to correct, click **[!UICONTROL Edit]**.

1. In the edit dialog, select the columns to change under **[!UICONTROL Catalog columns to edit]**. To find a column, use **[!UICONTROL Search columns]**.

1. Under **[!UICONTROL Columns content]**, update the selected field values.

1. Click **[!UICONTROL Update]**.

   The preview refreshes to reflect the updated values. The catalog changes aren't published until you save the dynamic creative.

>[!IMPORTANT]
>
>These edits update catalog data, not just the ad preview. Review the values before publishing them.

### Save changes or exit {#save-or-exit}

* To save the dynamic creative and publish any catalog edits:

  1. Click **[!UICONTROL Save Dynamic Creative]** in the header.

  1. Confirm the save:

     * For a new creative, in the **[!UICONTROL Create Dynamic Creative]** confirmation dialog, click **[!UICONTROL Create]**.
     * For an existing creative, in the **[!UICONTROL Update Dynamic Creative]** confirmation dialog, click **[!UICONTROL Update]**.

     You return to the creative library or [!UICONTROL Creative Studio], depending on where you opened the QA screen.

* To leave without publishing pending catalog edits, click **[!UICONTROL Cancel]** in the page header.

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
