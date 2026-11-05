---
title: Edit and quality-check dynamic creatives
description: Learn how to edit dynamic creative settings and quality-check catalog content in a creative library.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Edit and quality-check dynamic creatives

Edit creative settings to change the creative's configuration, such as its name, catalogs, and attribute mapping. Use the QA Agent to review the resulting ads and correct catalog values.

## Edit creative settings {#edit-creative-settings}

### From the new UI {#from-the-new-ui}

1. Open the creative settings:

   * From a creative library:
   
     1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.
     
     1. Open the library in either of the following ways:
     
        * Click the library name.
        
        * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL ...]** next to the creative name, and then click **[!UICONTROL Edit]**.

   * From [!UICONTROL Creative Studio]:
   
     1. In the main menu, click **[!UICONTROL Creative] > [!UICONTROL Creative Studio]**.
     
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

### From the legacy UI {#from-the-legacy-ui}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click **[!UICONTROL Switch to classic UI]**.

1. Click the library name.

1. Hold the cursor over the creative row and click **[!UICONTROL Edit]**.

1. Edit the [dynamic ad settings](creative-settings-dynamic.md).

1. Click **[!UICONTROL Continue]** to preview the creatives to generate. You can do any of the following within the preview:

   * To filter the creatives by catalog, filter value<!-- explain more-->, and ad size, use the filters above the preview area.
   
   * To search for a product by its unique ID in the search field below the preview area.
   
   * To change the columns that are displayed, click ![Column Filter](/help/creative/assets/custom-columns.png "Column Filter") below the preview area.
   
   * To preview a specific creative, select the check box for the row.
   
   * Change the content:
   
     * (Display ads only) To edit the value of a cell within the table, click inside the cell and edit the value. Click outside of the cell or press the **[!DNL Enter]** key to save your changes.
     
     * To mark a single product as the default<!--Explain what this means. -->, hold the curser over the row and click **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.
     
     * (When the ad includes more than one offer) To mark multiple products as the default, select the rows (up to the number of offers) and click **[!UICONTROL Set as Default]** in the bulk actions toolbar.
     
     * To delete a product from the catalog, hold the curser over the row and click **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.
     
     * (When the ad includes more than one offer) To delete multiple products from the catalog, select the rows (up to the number of offers) and click **[!UICONTROL Delete Row]** in the bulk actions toolbar.

1. Save the creatives:

   * To save the ads and add them to a [creative bundle](bundle-manage.md) in the library:
   
     1. Click **[!UICONTROL Save and Attach to Bundle]**.

     1. Click **[!UICONTROL Save]** to save the ads.

     1. Select the bundles, and then click **[!UICONTROL Attach Creative to Bundles]**.

   * To save the ads and exit the setup, click **[!UICONTROL Save]**, and then click **[!UICONTROL Save]** again.

## Quality-check a dynamic creative (new UI only) {#qa-dynamic-creative}

Use the QA Agent in the new UI to analyze catalog rows against a dynamic creative's template, preview the resulting ads, and identify potential content issues. You can filter and group ads using the **[!UICONTROL AI Assistant]**, review catalog alerts, and manually correct catalog values before publishing the changes.

>[!NOTE]
>
>You can quality-check dynamic creatives from either [!UICONTROL Creative Libraries] or [!UICONTROL Creative Studio]. See "[Quality-check a dynamic creative from Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)" for the other entry point.

The QA Agent is available only for dynamic display creatives based on dynamic templates, not standard creatives or dynamic video creatives.

### Open the QA Agent {#open-qa-agent}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Open the library in either of the following ways:

   * Click the library name.
   * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL ...]** next to the dynamic creative name, and then click **[!UICONTROL QA Agent]**.

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

* To save the existing dynamic creative and publish any catalog edits:

  1. Click **[!UICONTROL Save Dynamic Creative]** in the header.

  1. In the **[!UICONTROL Update Dynamic Creative]** confirmation dialog, click **[!UICONTROL Update]**.

     You return to the creative library.

* To leave without publishing pending catalog edits, click **[!UICONTROL Cancel]** in the page header.

>[!MORELIKETHIS]
>
>* [Dynamic creative settings](creative-settings-dynamic.md)
>* [Add dynamic creatives to a creative library](creative-add-dynamic.md)
>* [View the change log for a creative](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Workflows for dynamic ads](/help/creative/introduction/workflow-dynamic-ads.md)
