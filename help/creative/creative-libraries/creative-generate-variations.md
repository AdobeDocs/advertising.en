---
title: Generate variations of flexible HTML5 creatives
description: Learn how to generate and save AI-assisted variations of flexible HTML5 creatives from a creative library.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Generate variations of flexible HTML5 creatives

Use the [!UICONTROL Ad Variations Generator] to create new variations of an existing flexible HTML5 creative. The AI assistant generates and refines headlines, CTAs, images, colors, and more, and can create new size variants in a single session. Save the resulting variations as new standard ads in the creative library.

>[!NOTE]
>
>You can also generate ad variations from [!UICONTROL Creative Studio]. Both entry points open the same [!UICONTROL Ad Variations Generator]. See "[Generate ad variations for a standard ad in Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)" for the other entry point.

## Availability {#availability}

The **[!UICONTROL Generate Variations]** action is available for flexible HTML5 creatives, including those based on system templates, in the new [!UICONTROL Creative Libraries] UI. It isn't available for other creative types, including dynamic creatives.

The action is disabled when the creative doesn't have the internal parent ad-template reference required by the generator. This reference isn't a setting that you can edit; uploading or replacing a file on the creative's **[!UICONTROL Template]** tab doesn't explicitly set it.

## Open the Ad Variations Generator {#open-generator}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Open the library in either of the following ways:

   * Click the library name.
   * Next to the library name, click **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL ...]** next to the flexible HTML5 creative name, and then click **[!UICONTROL Generate Variations]**.

   The [!UICONTROL Ad Variations Generator] opens with the selected creative's content. The canvas shows the **[!UICONTROL Template Sizes]** section with the template's available ad formats and an **[!UICONTROL Ad Concepts]** section where generated content will appear.

## Generate and refine variations {#generate-variations}

1. (Optional) To apply a brand profile to the ads, select a **[!UICONTROL Brand Profile]** in the canvas toolbar.

   The AI assistant uses your brand's logo, color palette, voice guidelines, image standards, and channel guidelines when generating content.

1. Build ad variations using the [!UICONTROL AI Assistant]:

   1. In the **[!UICONTROL Ask AI to generate ad variations…]** field, type a request and press **[!UICONTROL Enter]**, or click one of the featured prompts:

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      The AI generates results on the canvas and organizes them into *concepts*, each representing a distinct content variation. The concept counter in the **[!UICONTROL Ad Concepts]** section tracks how many concepts exist (for example, **(2/10)**). Up to 10 concepts are allowed per session.

   1. Continue refining by sending follow-up messages. Examples:

      * "Make all the copy more playful and less corporate."
      * "Change the logo to the white version."
      * "Set the CTA to 'Shop Now' on all concepts."
      * "Resize this ad to all 6 IAB standard display sizes."
      * "Give me 3 different headline concepts with a matching background image for each."

      >[!NOTE]
      >
      >The AI assistant can generate and modify text (headlines, subheadlines, CTAs, body copy), swap background images, apply brand colors, switch logo versions, and create new size templates. It can't change template structure: element positions, layout, spacing, padding, font family, font size, or borders. Make structural changes in the template editor before starting the session. See [Edit a template](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

   1. (Optional) To include a visual reference in a request, click the **[!UICONTROL +]** button in the chat input area. In the **[!UICONTROL Select from Asset Library]** dialog:

      * To use an asset in your asset library, click the asset, and then click **[!UICONTROL Add to chat]**. Submit your message to include the asset as context.

      * To upload one or more assets, click **[!UICONTROL Upload Assets]** and select the files on your device or network.

1. (Optional) Use the canvas toolbar to review the generated ads:

   * **[!UICONTROL Brand]:** Select or change the brand profile applied to the session.
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]:** Adjust the canvas zoom level.
   * **[!UICONTROL Fit to screen]:** Reset the view to show all sizes.
   * **[!UICONTROL Replay animations]:** Replay template animations.

   When the AI creates a new size, **[!UICONTROL Adjust]**, **[!UICONTROL Keep]**, and delete controls appear on the new size card. Click **[!UICONTROL Keep]** to accept the size as-is, click **[!UICONTROL Adjust]** to open the template in the display editor where you can make structural changes and then click **[!UICONTROL Update Ad Format]** to save, or click the delete icon to remove the new size.

1. (Optional) Manage concepts and variations:

   * To manage a concept, hold the cursor over the concept label (for example, **[!UICONTROL Concept 3]**) and click **[!UICONTROL ...]**, then select an option:

     * **[!UICONTROL Add to chat]:** References the concept in your next prompt.
     * **[!UICONTROL Delete]:** Removes the concept.

   * To manage an individual variation, hold the cursor over the variation card and click **[!UICONTROL ...]**, then select an option:

     * **[!UICONTROL Add to Chat]:** References the variation in your next prompt. You can also click directly on the variation card body to toggle the mention.
     * **[!UICONTROL Edit Data]:** Opens a dialog where you can update the variation **[!UICONTROL Name]** and the click-through URL for each click tag defined in the template. Click **[!UICONTROL Save]** to apply.
     * **[!UICONTROL Delete]:** Removes the variation.

## Save the variations {#save-variations}

1. When you are satisfied with the generated concepts, click **[!UICONTROL Save Standard Ads]** in the header.

   The button is disabled until at least one concept exists.

1. In the **[!UICONTROL Save Standard Ads]** dialog, review the following settings, then click **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** The advertiser associated with the source creative library. You can't change this value.

   **[!UICONTROL Creative Library]:** The source creative library in which the new ads are saved. You can't change this value.

   **[!UICONTROL Attach to Bundles]:** (Optional) When enabled, the saved creatives are attached to one or more bundles. For each ad variation, select a bundle, or enter a new bundle name.

   **\[Settings for each ad\]:** For each ad variation, you can view and optionally change the **[!UICONTROL Name]**, **[!UICONTROL Language]**, and click-through URL for each click tag.

   You return to the creative library.

>[!MORELIKETHIS]
>
>* [Edit standard creatives](creative-edit-standard.md)
>* [Manage standard ads in Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Manage brand profiles in Advertising Creative](/help/creative/brands/brand-manage.md)
>* [C2PA metadata in [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
