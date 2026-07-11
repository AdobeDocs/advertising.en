---
title: Manage ad templates in Creative Studio
description: Learn how to create, import, organize, and manage ad templates in the Creative Studio Templates tab in Adobe Advertising Creative.
feature: Creative Studio
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

The tab also lists your existing ad templates at the bottom of the page <!-- Only in the Templates tab -->as [individual cards (the default) or as tables/lists](/help/creative/introduction/customize-data-views.md). The ad template list includes tabs for [!UICONTROL All], [!UICONTROL System Templates] (which are uploaded to your account by your Adobe Account Team<!-- verify -->), and [!UICONTROL User Templates]. By default, ad templates for all of your advertisers are shown. To view only ad templates for a specific advertiser, select from the advertiser list at the top of the page. 

<!-- Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.

-->

### Available actions

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Creation:

* [Import HTML5 ad templates](#templates-import)

* [Create an ad template manually](#template-create)

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

<!-- I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Template editor controls {#template-controls}

Both template editors share the same top toolbar and [!UICONTROL Layers] panel. The navigation bar or canvas toolbar, left panel, canvas controls, and inspector panel differ between display and video templates.

### Top bar

The top bar is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

### Canvas toolbar

#### Display ad templates

The canvas toolbar sits above the canvas in the display editor.

| Control | Description |
| --- | --- |
| **[!UICONTROL Undo]** | Undoes the last action. |
| ![Redo](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Redoes the last undone action. |
| **[!UICONTROL Links]** | Opens a panel to manage the click-through URLs attached to elements in the template. |
| Zoom controls | Click **[!UICONTROL Zoom out]** or **[!UICONTROL Zoom in]** to adjust the canvas magnification (10%-150%, in 10% increments). Click the zoom level label &mdash; which shows **[!UICONTROL Auto]** when the canvas fits automatically, or a percentage when set manually &mdash; to open a menu with options: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]**, and **[!UICONTROL Zoom Out]**. |
| Ad size | Shows the current ad dimensions (for example, 300 × 250). Click to open the size picker, which offers six commonly used IAB standard sizes as cards, plus a dropdown with all 19 standard IAB display ad sizes. The default size for new templates is 300 × 250 (Medium Rectangle). |
| ![Open Layers panel](/help/creative/assets/layers-panel-open.png "Open Layers panel") | Opens the [!UICONTROL Layers] panel. Appears only when the [!UICONTROL Layers] panel is closed. |

#### Video ad templates

The video editor navigation bar sits above the canvas and contains the following controls.

| Control | Description |
| --- | --- |
| **[!UICONTROL Undo]** /  ![Redo](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | Undoes or redoes the last action. |
| Zoom controls | Click **[!UICONTROL Zoom out]** or **[!UICONTROL Zoom in]** to adjust the canvas magnification. Click the zoom level to open a menu with options: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]**, and **[!UICONTROL Zoom Out]**. |
| ![Open Layers panel](/help/creative/assets/layers-panel-open.png "Open Layers panel") | Opens the [!UICONTROL Layers] panel. Appears only when the [!UICONTROL Layers] panel is closed. |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### Left panel

#### Display ad templates

The left panel contains a column of icons. Click an icon to open its content panel; click the same icon again to close it.

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Search across all asset types in your library. |
| **[!UICONTROL Upload]** | Upload images<!-- not there as of 7/10:  or font files (TTF, OTF, WOFF, WOFF2)--> into the editor for use in the current template. You can upload up to 20 files at a time. |
| **[!UICONTROL Templates]** | Browse ad templates from your Creative Studio library to use as a base layer or reference element. |
| **[!UICONTROL My Assets]** | Browse all assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Images]** | Browse only the image assets you've uploaded in the Creative Studio Assets tab.. |
| **[!UICONTROL Text]** | Add a text element to the canvas, including any custom fonts you've uploaded. |
| **[!UICONTROL Elements]** | Add shapes and layout elements such as buttons and rectangles. |

You can drag an item from any panel directly onto the canvas, or click it to place it at a default position.

#### Video ad templates

The left panel contains a column of icons. Click an icon to open its content panel; click the same icon again to close it.

| Icon | Description |
| --- | --- |
| **[!UICONTROL Search]** | Search across all asset types in your library. |
| **[!UICONTROL Upload]** | Upload image, video, audio, or font files (TTF, OTF, WOFF, WOFF2) into the editor for use in the current template. You can upload up to 20 files at a time. |
| **[!UICONTROL Templates]** | Browse ad templates from your Creative Studio library. |
| **[!UICONTROL My Assets]** | Browse all assets you've uploaded in the Creative Studio Assets tab. |
| **[!UICONTROL Images]** | Browse only the image assets you've uploaded in the Creative Studio Assets tab.. |
| **[!UICONTROL Video]** | Browse only the video assets you've uploaded in the Creative Studio Assets tab.. |
| **[!UICONTROL Audio]** | Browse only the audio assets you've uploaded in the Creative Studio Assets tab.. |
| **[!UICONTROL Text]** | Add a text element to the canvas, including any custom fonts you've uploaded. |
| **[!UICONTROL Elements]** | Add shapes and vector elements. |

You can drag an item from any panel directly onto the canvas, or click it to place it at a default position.

### Canvas toolbars

Click an element on the canvas to select it. Two toolbars appears above or below the selected element with the following options. 

#### Inspector panel (video ad templates)

When an element is selected, a contextual inspector bar appears at the top of the editing area with controls that vary by element type.

| Control | Element types | Description |
| --- | --- | --- |
| **[!UICONTROL Audio replace]** | Audio and video | Replaces the audio track with a file from your asset library. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]** | Text | Adjusts the font family, style, weight, size, and horizontal alignment. |
| **[!UICONTROL Fill]** | All | Sets the fill color or image for the element. |
| **[!UICONTROL Trim]** | Video and audio | Opens trimming mode to set the clip's start and end points. |
| **[!UICONTROL Volume]** | Video and audio | Adjusts the audio level. |
| **[!UICONTROL Playback speed]** | Video and audio | Adjusts the playback rate. |
| **[!UICONTROL Crop]** | All | Crops the element to a custom area. |
| **[!UICONTROL Stroke]** | All | Sets the border color and width. |
| **[!UICONTROL Animations]** | All | Adds or edits entry, exit, or loop animations. |
| **[!UICONTROL Appearance]** | All | Applies color adjustments, filters, effects, and blur. |
| **[!UICONTROL Shadow]** | All | Adds or edits a drop shadow. |
| **[!UICONTROL Opacity]** | All | Sets the element's transparency level. |
| **[!UICONTROL Position]** | All | Adjusts the element's size, position, and rotation numerically. |

#### General controls

##### Display ad templates

| Action | Description |
| --- | --- |
| **[!UICONTROL Replace]** | (Image elements only) Opens the Images panel so you can replace the image with one from your asset library. |
| ![Move forward](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | Moves the element one step forward in the stacking order (toward the front). |
| ![Move backward](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | Moves the element one step backward in the stacking order (toward the back). |
| ![Duplicate](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | Creates a copy of the element. |
| ![Delete](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | Removes the element from the canvas. |

You can also drag a selected element to reposition it, and drag the handles around it to resize it.

##### Video ad templates

Click an element on the canvas to select it. A context menu appears with the following options:

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

You can also drag a selected element to reposition it, and drag the handles around it to resize it.

### Timeline (video ad templates)

The video editor displays a timeline panel at the bottom of the canvas showing all video and audio clips in the template. Use the timeline to review how clips are arranged in time and to trim clips by dragging their start and end handles.

### [!UICONTROL Layers] panel

The [!UICONTROL Layers] panel lists all elements in the template and lets you manage their order, visibility, and properties. For display templates, click **[!UICONTROL Open Layers]** in the canvas toolbar to open it. For video templates, the panel is open by default.

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
| ![Rename layer](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | Lets you enter a new layer name in the panel. |
| ![Lock layer](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![Unlock layer](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | Prevents or allows the layer from being moved, edited, or reordered. |
| ![Hide layer](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![Show layer](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | Hides or shows the layer on the canvas. Hidden layers are preserved in the template but don't appear when the template renders. |
| ![Drag to reorder](/help/creative/assets/cs-icon-drag.png) Drag to reorder | (Display ad templates only) Drag the reorder icon to change the layer's position in the stacking order. The layer must be unlocked to reorder it. |

**Panel footer**

| Action | Description |
| --- | --- |
| ![Duplicate selected layer](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | Creates a copy of the selected layer. |
| ![Delete selected layer](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | Deletes the selected layer. |
| **[!UICONTROL Group selected layers]** (video templates only) | Groups two or more selected layers into a single group. Appears only when two or more layers are selected. Grouped layers can be ungrouped or have individual layers removed from the group using the controls on the group row. |

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

   * To add a template as a favorite, click ![Favorite](/help/creative/assets/favorite-null.png).

   * To remove a template as a favorite, click ![Favorite](/help/creative/assets/favorite.png).

## Delete an ad template {#template-delete}

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Hold the cursor over the template card or table row and click **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [About Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Manage assets in Creative Studio](creative-studio-manage-assets.md)
>* [Manage standard ads in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Manage dynamic creatives in Creative Studio](creative-studio-manage-dynamic-ads.md)
