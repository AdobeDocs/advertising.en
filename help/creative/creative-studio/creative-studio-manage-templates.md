---
title: Manage ad templates in Creative Studio
description: Learn how to create, import, organize, and manage ad templates in the Creative Studio Templates tab in Adobe Advertising Creative.
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
# Manage ad templates in [!UICONTROL Creative Studio]

Create, import, and manage display and video ad templates for use in ad generation sessions.

## The [!UICONTROL Creative Studio] > [!UICONTROL Templates] view

The **[!UICONTROL Templates]** tab provides quick actions to create or import new ad templates.

The tab also lists your existing ad templates at the bottom of the page <!-- Only in the Templates tab -->as [individual cards (the default) or as tables/lists](/help/creative/introduction/customize-data-views.md). The ad template list includes tabs for [!UICONTROL All], [!UICONTROL System Templates] (which are uploaded to your account by your Adobe Account Team), and [!UICONTROL User Templates]. By default, ad templates for all of your advertisers are shown. To view only ad templates for a specific advertiser, select from the advertiser list at the top of the page. 

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Available actions

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Creation:

* [Generate an ad template using AI](#template-generate)

* [Create an ad template manually](#template-create)

* [Import HTML5 ad templates](#templates-import)

Actions on your existing templates:

* [Generate ad variations from a display ad template](#ad-variations-generate)

* [Edit an ad template](#template-edit)

* [Add or remove labels for an ad template](#template-labels)

* [Preview an ad template](#template-preview)

* [Download an ad template](#template-download)

* [Add or remove an ad template as a favorite](#template-favorite)

* [Delete an ad template](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Generate an ad template using AI {#template-generate}

*Beta feature*

Use AI in [!UICONTROL Creative Studio] to convert an existing static display ad image into an editable display ad template. A three-step wizard helps you generate and review the template, request changes using natural language, and open the template editor to make manual changes and save the template.

### Prerequisites

You need a static image ad in a Creative Library. This workflow selects ads from your libraries; it doesn't upload a new image directly in the generation dialog.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Step 1: Generate and review the template

1. In the main menu, click **[!UICONTROL Creative Studio]**.

1. Click the **[!UICONTROL Templates]** tab.

1. (Optional) Select an advertiser from the advertiser list at the top of the page to view that advertiser's libraries.

1. In the **[!UICONTROL Use AI to Generate a New Display Ad Template]** box, click **[!UICONTROL Generate]**.

1. In the **[!UICONTROL Generate New Ad Template]** dialog, select **[!UICONTROL Generate from Existing Standard Ad Image]** if it isn't already selected.

1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

   Generation begins automatically, using the selected ad's width and height.

<!-- Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Review and refine the generated template](#template-review).

### Step 2: Review and refine the template {#template-review}

1. Wait for generation to finish, and then review the template preview and the **[!UICONTROL Layers]** panel, when available.

   Check the text, images, and layout before using the template. The layers shown here are for review; make manual changes in the template editor.

1. (Optional) Request changes to the generated template:

   1. In the **[!UICONTROL Ask the AI for any changes]** field, describe the changes you want. For example, enter `Change the headline to "Limited Time Offer" and the button text to "Shop Now"`.

   1. Click **[!UICONTROL Regenerate]**.

   1. Review the updated preview. Repeat as needed.

1. When you're ready to continue, click **[!UICONTROL Use this Ad Template]**.

   The generated template opens in the display template editor.

### Step 3: Edit and save the template {#template-save}

1. In the template editor, review the generated elements and make any remaining changes using the [template editor controls](#template-controls).

1. Click **[!UICONTROL Save]**.

1. In the **[!UICONTROL Update Template]** dialog, enter or update the **[!UICONTROL Template name]**, select the **[!UICONTROL Advertiser]**, and optionally add tags.

1. Click **[!UICONTROL Update]** to save the template and return to the **[!UICONTROL Templates]** view.

   To save a separate copy instead, click **[!UICONTROL Save As New]**.

You can then use the template to [generate ad variations](#ad-variations-generate).

### If you can't generate a template {#troubleshooting}

| Issue | What to do |
| --- | --- |
| No libraries or image ads are listed when generating from an image | Check the selected advertiser and **[!UICONTROL Ad Library]**. If the library has no standard ad images, select another library containing an existing static image ad. |
| Image-based generation fails or the image can't be converted | Review the displayed message, click **[!UICONTROL Back to library]**, and select an image ad to try again. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## Create an ad template manually {#template-create}

Create a blank display or video template using the template editor.

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. In the **[!UICONTROL Create New Ad Template]** box, click **[!UICONTROL Create]**, and then select **[!UICONTROL Display Ad Template]** or **[!UICONTROL Video Ad Template]**.

1. (Display ads) Select the ad template size, and then click **[!UICONTROL Continue]**.

1. Configure the template settings using the [controls in the template editor](#template-controls).

1. (Optional) To download a copy of the template as defined, click **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   The file is downloaded according to your browser's normal procedure.

1. Save the template:

   1. Do either of the following:
   
      * Click **[!UICONTROL Save]**.

      * To save the template as a draft, click **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Enter the **[!UICONTROL Template name]**, select the **[!UICONTROL Advertiser]**, optionally select existing tags or add new tags to the template, and then click **[!UICONTROL Save]**.

## Import HTML5 ad templates {#templates-import}

Upload one or more pre-built HTML5 templates that are packaged as ZIP files. Templates are validated on import; import fails if the HTML exceeds 200,000 characters, the CSS exceeds 60,000 characters, the template contains more than 5,000 DOM elements, or the template includes unsupported script tags.

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Select the advertiser at the top of the page.

1. Click the **[!UICONTROL Templates]** tab.

1. In the **[!UICONTROL Upload HTML5 Templates]** box, click **[!UICONTROL Upload]**, and then select **[!UICONTROL Display Ad Template]** or **[!UICONTROL Video Ad Template]**.

1. Select one or more ZIP files from your device or network.

1. In the **[!UICONTROL Import Templates]** dialog:

   1. Select an **[!UICONTROL Advertiser]**.

      If you already selected a specific advertiser at the top of the page, that advertiser is preselected.

   1. (Optional) For each file, edit the **[!UICONTROL Template Name]**.

      The file name is used by default.

   1. (Optional) To add more files, click **[!UICONTROL Add more]** and select additional ZIP files. Specify the **[!UICONTROL Template Name]** for each additional file. 

1. Click **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>If import fails, simplify the template or contact your Adobe Account Team.

## Edit an ad template {#template-edit}

*Display ad templates only.*

>[!IMPORTANT]
>
>The AI agent can't change the template layout, element positions, spacing, or typography. Make any structural changes in the template editor before you generate content.

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Edit the template layout or elements using the [controls in the template editor](#template-controls).

1. (Optional) To download a copy of the template as defined, click **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   The file is downloaded according to your browser's normal procedure.

1. Save the template:

   * Click **[!UICONTROL Save]**.

   * To save the template as a draft, click **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Enter the **[!UICONTROL Template name]**, select the **[!UICONTROL Advertiser]**, optionally select existing tags or add new tags to the template, and then click **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Generate ad variations from a display ad template {#ad-variations-generate}

*Display ad templates only.*

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   The [!UICONTROL Ad Variations Generator] opens with the template pre-loaded.

1. Use the AI chat interface to generate and refine ad content. See "[Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)" for the complete workflow.

## Add or remove labels for an ad template {#template-labels}

*Display ad templates only.*

Labels help you organize and filter user templates. You can't add labels to system templates.

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. In the **[!UICONTROL Edit Labels]** dialog:

   * To add a label, either select an existing label or enter a name in the input field and click **[!UICONTROL Add Tag]**.

   * To remove a label, click **[!UICONTROL X]** next to the label tag.

1. Click **[!UICONTROL Save]**.

## Preview an ad template {#template-preview}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card.

1. Do either of the following:

   * (Card view) Click the **[!UICONTROL Preview template]** icon, or click **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Table view) Click **[!UICONTROL ...]** > **[!UICONTROL Preview]**.
   
1. For video templates, click ![Play](/help/creative/assets/play.png "Play").

## Download an ad template {#template-download}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   The template downloads as a ZIP file according to your browser's normal procedure.

## Add or remove an ad template as a favorite {#template-favorite}

*Card view only*

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card.

1. Do either of the following:

   * To add a template as a favorite, click ![Favorite](/help/creative/assets/favorite-null.png "Favorite").

   * To remove a template as a favorite, click ![Favorite](/help/creative/assets/favorite.png "Favorite").

## Delete an ad template {#template-delete}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

## Template editor controls {#template-controls}

Both the display and video template editors provide a toolbar above the canvas to undo changes and adjust the view, panels on the left to add assets and elements, and a [!UICONTROL Layers] panel on the right to manage layers. The tools for editing selected elements and controlling timing and playback differ between display and video templates.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Undo changes and adjust the canvas view

The general actions toolbar sits above the editing canvas in the ad template editor and is split into two parts (left and right).

#### Display ad templates

| Control | Description |
| --- | --- |
| **[!UICONTROL Undo]** | Undoes the last action. |
| ![Redo](/help/creative/assets/cs-icon-redo.png "Redo") **[!UICONTROL Redo]** | Redoes the last undone action. |
| **[!UICONTROL Links]** | Opens a panel to manage the click-through URLs attached to elements in the template. |
| Zoom controls | Click **[!UICONTROL Zoom out]** or **[!UICONTROL Zoom in]** to adjust the canvas magnification (10%-150%, in 10% increments). Click the zoom level label &mdash; which shows **[!UICONTROL Auto]** when the canvas fits automatically, or a percentage when set manually &mdash; to open a menu with options: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]**, and **[!UICONTROL Zoom Out]**. |
| Ad size | Shows the current ad dimensions (for example, 300 × 250). Click to open the size picker, which offers six commonly used IAB standard sizes as cards, plus a dropdown with all 19 standard IAB display ad sizes. The default size for new templates is 300 × 250 (Medium Rectangle). |
| ![Open Layers panel](/help/creative/assets/layers-panel-open.png "Open Layers panel") | Opens the [!UICONTROL Layers] panel. Appears only when the [!UICONTROL Layers] panel is closed. |

#### Video ad templates

| Control | Description |
| --- | --- |
| **[!UICONTROL Undo]** / ![Redo](/help/creative/assets/cs-icon-redo.png "Redo") **[!UICONTROL Redo]** | Undoes or redoes the last action. |
| Zoom controls | Click **[!UICONTROL Zoom out]** or **[!UICONTROL Zoom in]** to adjust the canvas magnification. Click the zoom level to open a menu with options: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]**, and **[!UICONTROL Zoom Out]**. |
| ![Open Layers panel](/help/creative/assets/layers-panel-open.png "Open Layers panel") | Opens the [!UICONTROL Layers] panel. Appears only when the [!UICONTROL Layers] panel is closed. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Add assets and elements

The left panel allows you to add ad assets and elements to the template. Click an icon to open its content panel; click the same icon again to close it.

#### Display ad templates

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Search across all asset types in your library. |
| **[!UICONTROL Upload]** | Upload images or font files into the editor for use in the current template. You can upload up to 20 files at a time. |
| **[!UICONTROL Templates]** | Browse ad templates from your Creative Studio library to use as a base layer or reference element. |
| **[!UICONTROL My Assets]** | Browse all assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Images]** | Browse only the image assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Text]** | Add a text element to the canvas, including any custom fonts you've uploaded. |
| **[!UICONTROL Elements]** | Add shapes and layout elements such as buttons and rectangles. |

You can drag an item from any panel directly onto the canvas, or click it to place it at a default position.

#### Video ad templates

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Search across all asset types in your library. |
| **[!UICONTROL Upload]** | Upload image, video, audio, or font files (TTF, OTF, WOFF, WOFF2) into the editor for use in the current template. You can upload up to 20 files at a time. |
| **[!UICONTROL Templates]** | Browse ad templates from your Creative Studio library. |
| **[!UICONTROL My Assets]** | Browse all assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Images]** | Browse only the image assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Video]** | Browse only the video assets you've uploaded in the Creative Studio Assets tab.. |
| **[!UICONTROL Audio]** | Browse only the audio assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Text]** | Add a text element to the canvas, including any custom fonts you've uploaded. |
| **[!UICONTROL Elements]** | Add shapes and vector elements. |

You can drag an item from any panel directly onto the canvas, or click it to place it at a default position.

### Edit selected elements

Click an element on the editing canvas to select it. Depending on the template type, one or more toolbars appear with controls for that element.

The controls vary by element type.

<!-- From inspectorbar.ts -->

#### Display template editing toolbar

| Control | Element types | Description |
| --- | --- | --- |
| **[!UICONTROL Properties]** | All | Opens a panel to edit the layer name; mark the layer as dynamic (swappable during ad generation); and set a click-through URL (links only). Below that, choose a **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]**, or **[!UICONTROL Focus]** state to style the element for that interaction state, then adjust styling &mdash; typography (text and links only), decorations (fill, border, corner radius), dimensions, position &mdash; based on the element type. |
| **[!UICONTROL Effects]** | All | Opens a panel where you choose a **[!UICONTROL Default]**, **[!UICONTROL Hover]**, **[!UICONTROL Click]**, or **[!UICONTROL Focus]** state to apply effects to for that interaction state, then adjust **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]**, and **[!UICONTROL Cursor]** sections. Text elements also include a **[!UICONTROL Text Shadow]** section. |
| **[!UICONTROL Animations]** | All | Opens a panel to set the layer's enter and exit time on the timeline, and to configure **[!UICONTROL Entrance Animation]**, **[!UICONTROL Loop Animation]**, and **[!UICONTROL Exit Animation]** presets with duration and easing. Includes **[!UICONTROL Copy]**, **[!UICONTROL Paste]**, and **[!UICONTROL Reset]** actions. |
| **[!UICONTROL Crop]** | Images | Opens a toolbar to crop the image. Select an **[!UICONTROL Aspect Ratio]** preset (or **[!UICONTROL Free]**), then click **[!UICONTROL Apply]** or **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | All | Opens a menu with **[!UICONTROL Move]** options (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** options (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**), and, for non-image elements, **[!UICONTROL Layer Level Alignment]** options (the same six alignment options, plus **[!UICONTROL Fit to Content]**). |

#### Video template editing toolbar

| Control | Element types | Description |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Shapes | Sets shape-specific options. |
| Cutout controls | Images | Adjust the cutout type, offset, and smoothing. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Multiple selected elements, or a group | Groups the selected elements together, or ungroups a selected group. |
| **[!UICONTROL Combine]** | Compatible shapes | Combines selected shapes into a single shape. |
| **[!UICONTROL Audio replace]** | Audio and video | Replaces the audio track with a file from your asset library. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Text | Adjusts the font family, weight, size, horizontal alignment, and other advanced typography settings. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Images and video | Sets the fill image or video source for the element. |
| **[!UICONTROL Trim]** | Video and audio | Opens trimming mode to set the clip's start and end points. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Video and audio | Adjusts the audio level. |
| ![Playback speed](/help/creative/assets/speed.png "Playback speed") ([!UICONTROL Playback speed]) | Video and audio | Adjusts the playback rate. |
| ![Crop](/help/creative/assets/crop.png "Crop") ([!UICONTROL Crop]) | All | Crops the element to a custom area. |
| Rotation and flip controls | All | Rotate or flip the selected element. |
| ![Stroke](/help/creative/assets/stroke.png "Stroke") ([!UICONTROL Stroke]) | All | Sets the border color and width. |
| **[!UICONTROL Text Background]** | Text | Adds a background color behind the text. |
| **[!UICONTROL Animations]** | All | Adds or edits entry, exit, or loop animations. |
| **[!UICONTROL Style]** | All | Opens a menu with **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]**, and **[!UICONTROL Blur]** options. |
| **[!UICONTROL Shadow]** | All | Adds or edits a drop shadow. |
| **[!UICONTROL Opacity]** | All | Sets the element's transparency level. |
| **[!UICONTROL Position]** | All | Adjusts the element's size, position, and rotation numerically. |
| ![Editing panel](/help/creative/assets/template-video-editing-panel.png "Editing panel") | All | Opens or closes an [editing panel](#detailed-element-properties-for-video-templates) for the selected element with more editing capabilities. |

#### Detailed element properties for video templates

In the video template editor, click ![Editing panel](/help/creative/assets/template-video-editing-panel.png "Editing panel") in the toolbar to open an editing panel for the selected element with more editing capabilities. The editing panel appears to the left of the canvas and is separate from the [!UICONTROL Layers] panel, which lists the layers in the template.

##### Individual elements

When you select a single image, video, shape, or text element, the editing panel shows the applicable sections below.

| Panel section | Tool | Controls |
| --- | --- | --- |
| [!UICONTROL Layer] | Alignment and layer positioning | Aligns the selected layer to the left, horizontal center, right, top, vertical center, or bottom. The arrangement menu changes its front-to-back stacking order. These controls position the layer itself; they don't justify text within the layer. |
| | [!UICONTROL Rotate & Flip] | Enter a rotation angle in degrees. Use ![Flip horizontal](/help/creative/assets/video-layer-flip-horizontal.png "Flip horizontal") to mirror the layer horizontally or ![Flip vertical](/help/creative/assets/video-layer-flip-vertical.png "Flip vertical") to mirror it vertically. |
| | ![Opacity](/help/creative/assets/video-layer-opacity.png "Opacity") [!UICONTROL Opacity] | Makes the selected layer more or less transparent. |
| | ![Blend mode](/help/creative/assets/video-layer-blend-mode.png "Blend mode") [!UICONTROL Blend Mode] | Changes how the selected layer's colors combine with the layers behind it. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Opens additional controls for the layer's position and dimensions. Availability depends on the selected layer's transform permissions. |
| [!UICONTROL Shape] | ![Shape options](/help/creative/assets/video-layer-shape-options.png "Shape options") [!UICONTROL Shape] and shape-specific properties | Changes the shape and its available properties, such as points, sides, inner diameter, line width, or corner radius. The controls depend on the selected shape. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Enters vector-editing mode to edit the shape's path, when available. |
| [!UICONTROL Character] | ![Typeface](/help/creative/assets/video-layer-typeface.png "Typeface") Typeface, ![Text style](/help/creative/assets/video-layer-text-style.png "Text style") text style, ![Bold](/help/creative/assets/video-layer-text-bold.png "Bold") bold, ![Italic](/help/creative/assets/video-layer-text-italic.png "Italic") italic, and ![Font size](/help/creative/assets/video-layer-font-size.png "Font size") font size | (Text layers) Changes the font family, font style, and size of the selected text. |
| | ![Align left](/help/creative/assets/video-layer-text-align-left.png "Align left") / ![Align center](/help/creative/assets/video-layer-text-align-center.png "Align center") / ![Align right](/help/creative/assets/video-layer-text-align-right.png "Align right") Text alignment | (Text layers) Aligns text within its frame to the left, center, or right, or detects the alignment automatically. |
| | ![Advanced text settings](/help/creative/assets/video-layer-advanced-text-settings.png "Advanced text settings") Advanced text settings | (Text layers) Opens additional typography settings. |
| [!UICONTROL Fill] | ![Fill](/help/creative/assets/video-layer-fill.png "Fill") Fill controls | Changes the selected layer's color, image, or video fill. The controls reflect the current fill type and open its settings. For text, changes the text color. |
| [!UICONTROL Stroke] | ![Stroke](/help/creative/assets/video-layer-stroke.png "Stroke") Stroke controls | Enables or disables the outline and changes its color, width, style, and placement. Additional controls appear when the stroke is enabled. |
| [!UICONTROL Text Background] | ![Text background](/help/creative/assets/video-layer-text-background.png "Text background") Background controls | (Text layers) Adds or changes the background behind the text. |
| [!UICONTROL Animations] | ![Animation](/help/creative/assets/video-layer-animation.png "Animation") [!UICONTROL Presets] | Opens animation presets for the selected layer, including entrance, exit, and loop animations. |
| [!UICONTROL Appearance] | ![Adjustments](/help/creative/assets/video-layer-adjustments.png "Adjustments") [!UICONTROL Adjustments] | Changes visual properties of the selected layer. |
| | ![Filter](/help/creative/assets/video-layer-filter.png "Filter") [!UICONTROL Filter] | Applies a visual filter to the selected layer. |
| | ![Effects](/help/creative/assets/video-layer-effects.png "Effects") [!UICONTROL Effect] | Applies an effect to the selected layer. |
| | ![Blur](/help/creative/assets/video-layer-blur.png "Blur") [!UICONTROL Blur] | Applies a blur to the selected layer. |
| | ![Shadow](/help/creative/assets/video-layer-shadow.png "Shadow") [!UICONTROL Shadow] | Adds or changes the selected layer's shadow. |

##### Multiple selections and specialized elements

When you select multiple elements, a group, a cutout element, or an audio clip, the editing panel shows the selection-specific sections below. Multiple elements, groups, and cutouts also retain the [!UICONTROL Layer] section.

| Panel section | Tool | Controls |
| --- | --- | --- |
| [!UICONTROL Layer] | Alignment and layer positioning | Aligns multiple selected elements or a group. The arrangement menu changes their front-to-back stacking order. |
| | [!UICONTROL Rotate & Flip] | Rotates or flips the selected elements or group. |
| | ![Opacity](/help/creative/assets/video-layer-opacity.png "Opacity") [!UICONTROL Opacity] | Makes the selected elements or group more or less transparent. |
| | ![Blend mode](/help/creative/assets/video-layer-blend-mode.png "Blend mode") [!UICONTROL Blend Mode] | Changes how the selected elements' or group's colors combine with the layers behind them. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Opens controls for the selected elements' or group's position and dimensions. Available controls depend on the selected elements. |
| [!UICONTROL Selection] | ![Group](/help/creative/assets/video-layer-group.png "Group") Group / ![Ungroup](/help/creative/assets/video-layer-ungroup.png "Ungroup") Ungroup | Appears below [!UICONTROL Layer] for multiple selected layers or a selected group. Groups selected layers so they can be managed together, or separates a group into individual layers. |
| [!UICONTROL Settings] | ![Cutout clip](/help/creative/assets/video-layer-cutout-clip.png "Cutout clip") / ![Cutout overlay](/help/creative/assets/video-layer-cutout-overlay.png "Cutout overlay") Cutout controls | (Cutout layers) Appears below [!UICONTROL Layer]. Selects the cutout type and adjusts its offset and edge smoothing. |
| [!UICONTROL Audio Properties] | ![Trim](/help/creative/assets/video-layer-trim.png "Trim") Trim, ![Volume](/help/creative/assets/video-layer-volume.png "Volume") volume, and ![Playback speed](/help/creative/assets/video-layer-playback-speed.png "Playback speed") playback speed | (Audio layers) Sets the clip's start and end points, audio level, and playback speed. |

#### Edit elements directly on the canvas

##### Display ad templates

| Action | Description |
| --- | --- |
| **[!UICONTROL Replace]** | (Image elements only) Opens the Images panel so you can replace the image with one from your asset library. |
| ![Move forward](/help/creative/assets/cs-icon-move-forward.png "Move forward") **[!UICONTROL Move forward]** | Moves the element one step forward in the stacking order (toward the front). |
| ![Move backward](/help/creative/assets/cs-icon-move-backward.png "Move backward") **[!UICONTROL Move backward]** | Moves the element one step backward in the stacking order (toward the back). |
| ![Duplicate](/help/creative/assets/cs-icon-duplicate.png "Duplicate") **[!UICONTROL Duplicate]** | Creates a copy of the element. |
| ![Delete](/help/creative/assets/cs-icon-delete.png "Delete") **[!UICONTROL Delete]** | Removes the element from the canvas. |
| Rotation handle | Click and drag the handle above a selected element to rotate it. Hold **[!UICONTROL Shift]** while dragging to snap the rotation to 15-degree increments. |

You can also click and drag a selected element to reposition it, and click and drag the handles around it to resize it.

##### Video ad templates

| Action | Description |
| --- | --- |
| **[!UICONTROL Edit text]** | (Text elements only) Switches to text editing mode so you can type and format text directly on the canvas. In text editing mode, a secondary menu provides **[!UICONTROL Text color]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, and **[!UICONTROL Text variables]** (template placeholders). |
| **[!UICONTROL Replace]** | (Image elements only) Opens the asset library so you can swap the image. |
| **[!UICONTROL Bring forward]** | Moves the element one step forward in the stacking order. |
| **[!UICONTROL Send backward]** | Moves the element one step backward in the stacking order. |
| **[!UICONTROL Duplicate]** | Creates a copy of the element. |
| **[!UICONTROL Delete]** | Removes the element from the canvas. |
| **... > [!UICONTROL Flip horizontal]** | Flips the element horizontally 180 degrees. |
| **... > [!UICONTROL Flip vertical]** | Flips the element vertically 180 degrees. |
| **... > [!UICONTROL Copy Element]** | Copies the element to the canvas clipboard. |
| **... > [!UICONTROL Pastes Element]** | Pastes the copied element. |

You can also click and drag a selected element to reposition it, and click and drag the handles around it to resize it.

### Control timing and playback

Both display and video editors display a timeline panel at the bottom of the canvas.

#### Display ad templates

The timeline shows a track for each layer on the canvas, spanning the time range the layer is visible based on its enter and exit animation timing. Drag a track's start or end handle to adjust its enter or exit time, or drag a track to reorder layers. Click the ruler or drag the playhead to move to a point in time.

The timeline toolbar includes a **[!UICONTROL Duration]** field (0-60 seconds), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, a current time / total duration display, a loop toggle, **[!UICONTROL Timeline Scale]** zoom controls, a **[!UICONTROL Fit View]** button, and a collapse/expand toggle.

#### Video ad templates

The timeline shows all video and audio clips in the template. Use the timeline to review how clips are arranged in time and to trim clips by dragging their start and end handles. You can't add a new clip directly on the timeline; add it from the left panel or canvas instead, and it then appears as a clip on the timeline.

### Manage layers

The [!UICONTROL Layers] panel on the right side of the canvas lists all elements in the template and lets you manage their order, visibility, and properties. For display templates, click **[!UICONTROL Open Layers]** in the canvas toolbar to open it. For video templates, the panel is open by default.

Click any layer to select the corresponding element on the canvas.

**Tabs (display ad templates only)**

Display templates have two tabs at the top of the [!UICONTROL Layers] panel:

* **[!UICONTROL Dynamic]** &mdash; Lists only the layers that can be swapped during ad generation, such as images and text that the AI agent can replace. This is the default view for generating ad variations.
* **[!UICONTROL All]** &mdash; Shows the complete layer hierarchy for the template, including structural containers. Use this view to inspect or reorganize how elements are nested.

Video templates show all layers in a single list with no tabs.

**Per-layer actions**

Hold the cursor over a layer to see the following actions:

| Action | Description |
| --- | --- |
| ![Rename layer](/help/creative/assets/edit.png "Rename layer") **[!UICONTROL Rename layer]** | Lets you enter a new layer name in the panel. |
| ![Lock layer](/help/creative/assets/cs-icon-lock.png "Lock layer") **[!UICONTROL Lock layer]** / ![Unlock layer](/help/creative/assets/cs-icon-unlock.png "Unlock layer") **[!UICONTROL Unlock layer]** | Prevents or allows the layer from being moved, edited, or reordered. |
| ![Hide layer](/help/creative/assets/cs-icon-hidden.png "Hide layer") **[!UICONTROL Hide layer]** / ![Show layer](/help/creative/assets/cs-icon-visible.png "Show layer") **[!UICONTROL Show layer]** | Hides or shows the layer on the canvas. Hidden layers are preserved in the template but don't appear when the template renders. |
| ![Drag to reorder](/help/creative/assets/cs-icon-drag.png "Drag to reorder") Drag to reorder | (Display ad templates only) Drag the reorder icon to change the layer's position in the stacking order. The layer must be unlocked to reorder it. |

**Panel footer**

| Action | Description |
| --- | --- |
| ![Duplicate selected layer](/help/creative/assets/cs-icon-duplicate.png "Duplicate selected layer") **[!UICONTROL Duplicate selected layer]** | Creates a copy of the selected layer. |
| ![Delete selected layer](/help/creative/assets/cs-icon-delete.png "Delete selected layer") **[!UICONTROL Delete selected layer]** | Deletes the selected layer. |
| **[!UICONTROL Group selected layers]** (video templates only) | Groups two or more selected layers into a single group. Appears only when two or more layers are selected. You can ungroup grouped layers or remove individual layers from the group using the controls on the group row. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

>[!MORELIKETHIS]
>
>* [About Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Manage assets in Creative Studio](creative-studio-manage-assets.md)
>* [Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Manage dynamic creatives in Creative Studio](creative-studio-manage-dynamic-ads.md)
