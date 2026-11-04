---
title: Quality-check dynamic creatives
description: Learn how to use the QA Agent to analyze, preview, and correct catalog-driven dynamic creatives in Adobe Advertising Creative.
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
# Quality-check dynamic creatives

Use the QA Agent to analyze catalog rows against a dynamic creative's template, preview the resulting ads, and identify potential content issues. You can filter and group ads using the **[!UICONTROL AI Assistant]**, review catalog alerts, and manually correct catalog values before publishing the changes.

The agent opens the **[!UICONTROL Dynamic Creative QA]** screen from either [!UICONTROL Creative Libraries] or [!UICONTROL Creative Studio].

>[!NOTE]
>
>The QA Agent is available for dynamic display creatives, not standard creatives or dynamic video creatives. In [!UICONTROL Creative Libraries], the action is available only for dynamic creatives based on dynamic templates.

## Open the QA Agent {#open-qa-agent}

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

## Analyze and filter ads with AI {#analyze-ads}

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

## Review previews and alerts {#review-previews}

* Use the canvas toolbar to:

  * Adjust the zoom.
  * Switch between **[!UICONTROL Thumbnail view]** and **[!UICONTROL Actual size]**.
  * Click **[!UICONTROL Replay animations]** to replay the previews.
  * Select the number of rows per page, select a page number, or use **[!UICONTROL Previous page]** and **[!UICONTROL Next page]**.

* When the assistant groups results, click the link to view all creatives in a group. Use **[!UICONTROL Back to groups]** to return to the grouped results, or **[!UICONTROL Catalog Rows]** to leave the grouped view.

* When a preview shows **[!UICONTROL Issues detected]**, hold the cursor over the indicator to view the issue details.

* When catalog alerts are available, click **[!UICONTROL View Alerts]**. The **[!UICONTROL Alerts]** dialog lists the catalog, row number, column, and error message for each issue. Click **[!UICONTROL Close]** to return to the canvas.

## Correct catalog values {#correct-catalog-values}

You can manually edit catalog values from an ad preview without leaving the QA screen.

1. On the preview that you want to correct, click **[!UICONTROL Edit]**.

1. In the edit dialog, select the columns to change under **[!UICONTROL Catalog columns to edit]**. To find a column, use **[!UICONTROL Search columns]**.

1. Under **[!UICONTROL Columns content]**, update the selected field values.

1. Click **[!UICONTROL Update]**.

   The preview refreshes to reflect the updated values. The catalog changes aren't published until you save the dynamic creative.

>[!IMPORTANT]
>
>These edits update catalog data, not just the ad preview. Review the values before publishing them.

## Save changes or exit {#save-or-exit}

* To save the existing dynamic creative and publish any catalog edits:

  1. Click **[!UICONTROL Save Dynamic Creative]** in the header.

  1. In the **[!UICONTROL Update Dynamic Creative]** confirmation dialog, click **[!UICONTROL Update]**.

     You return to the creative library or [!UICONTROL Creative Studio], depending on where you opened the QA screen.

* To leave without publishing pending catalog edits, click **[!UICONTROL Cancel]** in the page header.

>[!MORELIKETHIS]
>
>* [Manage dynamic creatives in Creative Studio](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md)
>* [Preview a creative](/help/creative/creative-libraries/creative-preview.md)
>* [Manage your creative libraries](/help/creative/creative-libraries/creative-library-manage.md)
