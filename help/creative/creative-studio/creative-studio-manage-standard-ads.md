---
title: Manage standard ads in Creative Studio
description: Learn how to create, edit, duplicate, download, and delete standard display and video ads in the Creative Studio creatives library.
feature: Creative Studio
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# Manage standard ads in [!UICONTROL Creative Studio]

The **[!UICONTROL Creatives]** tab in [!UICONTROL Creative Studio] is your library of standard display and video ads generated from templates. From here you can create ads using the [!UICONTROL Ad Variations Generator], edit saved ads, generate new variations from an existing ad, view the change log, duplicate, download, and delete.

## Create standard ads {#create-standard-ads}

Use the [!UICONTROL Ad Variations Generator] to generate display or video ad content from a template. The AI assistant generates and refines headlines, CTAs, images, colors, and more, and can create new size variants in a single session.

### Prerequisites

At least one ad template must exist in your template library.

### Generate standard ads

1. Open the [!UICONTROL Ad Variations Generator] in either of the following ways:

   * **From the [!UICONTROL Creatives] tab:**

     1. In the main menu, click **[!UICONTROL Creative Studio]**.

     1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Generate]** in the **[!UICONTROL Generate standard ads from templates]** quick action card.

     1. In the template selection dialog, click a template to select it, then click **[!UICONTROL Next]**.

   * **From the [!UICONTROL Templates] tab:**

     1. In the main menu, click **[!UICONTROL Creative Studio]**.

     1. Click the **[!UICONTROL Templates]** tab.

     1. Hold the cursor over a template card and click **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   The [!UICONTROL Ad Variations Generator] opens. The canvas shows the **[!UICONTROL Template Sizes]** section with the template's available ad formats and an **[!UICONTROL Ad Concepts]** section where generated content will appear.

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
      >The AI assistant can generate and modify text (headlines, subheadlines, CTAs, body copy), swap background images, apply brand colors, switch logo versions, and create new size templates. It cannot change template structure: element positions, layout, spacing, padding, font family, font size, or borders. Make structural changes in the template editor before starting the session. See [Edit a template](creative-studio-manage-templates.md#edit-template).

   1. (Optional) To include a visual reference in a request, click the **[!UICONTROL +]** button in the chat input area. In the **[!UICONTROL Select from Asset Library]** dialog:
   
      * To use an asset in your asset library, click th asset, and then click **[!UICONTROL Add to chat]**. Submit your message to include the asset as context.

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

1. When you are satisfied with the generated concepts, click **[!UICONTROL Save Standard Ads]** in the header.

   The button is disabled until at least one concept exists.

1. In the **[!UICONTROL Save Standard Ads]** dialog, specify the [save settings](#save-settings), then click **[!UICONTROL Save Standard Ads]**.

   A confirmation notification appears when the creatives are created.

### Save Standard Ads settings {#save-settings}

**[!UICONTROL Advertiser]:** (Required) The advertiser to save the creatives under.

**[!UICONTROL Creative Library]:** (Required) The creative library to save the creatives to. The library picker is enabled after you select an advertiser.

**[!UICONTROL Attach to Bundles]:** (Optional) When enabled, the saved creatives are attached to a bundle.

## Edit a standard ad {#edit-standard-ad}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   A full-screen editor opens with a live ad preview on the left and a settings panel on the right.

1. Edit the ad settings using the **[!UICONTROL Details]** and **[!UICONTROL Attributes]** tabs:

   **[!UICONTROL Details]** tab:

   * **[!UICONTROL Creative Name]:** (Required) The display name for the creative.
   * **[!UICONTROL Language]:** (Required) The language of the ad content.
   * **[!UICONTROL Creative Size]:** (Read-only) The ad dimensions.
   * **Click tags:** If the template defines click tags, each appears as a required field labeled with the tag name. Enter the click-through destination URL for each tag.
   * **[!UICONTROL Label]:** Optional labels for organizing creatives. Select existing labels or type to create new ones.

   **[!UICONTROL Attributes]** tab:

   The live preview updates in real time as you edit. The **[!UICONTROL Attributes]** tab is unavailable while the preview is loading.

   * **Text attributes:** Enter the text value for each editable text layer defined in the template.
   * **Image attributes:** Shows a thumbnail of the current image. Click **[!UICONTROL Replace Image]** to upload a replacement (PNG, JPEG, GIF, WebP, or SVG).

1. Click **[!UICONTROL Update Creative]**.

## Generate ad variations for a standard ad {#generate-ad-variations}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   The [!UICONTROL Ad Variations Generator] opens with the selected ad pre-loaded.

1. Use the AI chat interface to generate and refine additional variations. See [Create standard ads](#create-standard-ads) for the complete workflow.

## Duplicate a standard ad {#duplicate-standard-ad}

Duplicate a standard ad to add a new creative with the same settings to the library. You can later rename the new creative and edit the settings as needed.

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   The new creative is named `<original name> (copy)`.

## View the change log for a standard ad {#view-change-log}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   A dialog opens showing a table of changes to the ad.

## Download a standard ad {#download-standard-ad}

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   The creative downloads according to your browser's normal procedure.

## Delete a standard ad {#delete-standard-ad}

>[!NOTE]
>
>This action cannot be undone.

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. On the **[!UICONTROL Creatives]** tab, hold the cursor over the creative card and click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Manage dynamic creatives in Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Manage templates in Creative Studio](creative-studio-manage-templates.md)
>* [About brand profiles in Advertising Creative](/help/creative/brands/brands-about.md)
