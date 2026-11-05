---
title: Create an experience with decision tree targeting
description: Learn how to create a targeted ad experience using the AI-driven or manual decision tree editor.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Create an experience with decision tree targeting

Create a targeted ad experience using a decision tree. Each experience uses ads from a single creative library.

The AI-driven editor (Beta) opens by default. You can configure the tree through the AI agent or edit its canvas directly. You can also switch to the existing manual editor.

>[!NOTE]
>
>* Once you create a targeted experience, you can't later change it to a non-targeted experience, which uses a different workflow.
>* Make sure that your ad experiences include targeting that's compatible with the campaigns in which you'll implement it. Hierarchical targeting behavior may vary by DSP. When you upload an ad experience tag to Advertising DSP and attach it to a placement, ad-level targeting is applied on top of (not instead of) placement-level targeting. For example, if a placement targets users in Australia and an ad targets users in Japan, then the ad will target the "Everyone Else" branch.

## Create the experience

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Click **[!UICONTROL Create New Experience]**.

1. Enter the [general experience settings](experience-settings-targeting.md), with **[!UICONTROL Targeting]** enabled.

1. Click **[!UICONTROL Create]**.

   The AI-driven decision tree editor opens for the new experience.

1. Configure the tree using either of the following procedures.

## Configure the tree using the AI-driven editor (Beta) {#ai-editor}

1. In the conversation, describe the targeting structure you want, including the criteria for each branch and how to handle viewers who don't match a specified target.

1. Review the tree in the canvas. To request changes, describe them in the conversation. Wait for the assistant to finish processing before interacting with the canvas.

1. (Optional) Refine the tree directly in the canvas:

   * [Add a final-level target](experience-target-node-add-final.md#ai-editor), [insert a target level](experience-target-node-add-inner.md#ai-editor), or [add a sibling target](experience-target-node-add-sibling.md#ai-editor).

   * [Copy child nodes and creatives](experience-target-node-copy.md#ai-editor) or [delete a node](experience-target-node-delete.md#ai-editor).

1. [Assign creative bundles to the final nodes](experience-assign-creative-bundles.md#ai-editor), and optionally [customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) and [tracking URLs](experience-tracking-urls-targeting.md#ai-editor).

   To publish the experience, you must assign bundles to each final node or use the experience's default creatives. You can assign defaults to unassigned nodes when you save.

1. (Optional) Edit the general experience settings:

   1. To save any tree changes you want to keep, click **[!UICONTROL Save]**.

   1. Click **[!UICONTROL Experience Form]**, and then click **[!UICONTROL Yes]** to discard unsaved tree changes and open the form.

   1. Edit the [general experience settings](experience-settings-targeting.md), and then click **[!UICONTROL Save]**.

      The AI-driven editor opens.

1. [Save the experience](#save).

## Configure the tree using the manual editor {#manual-editor}

1. In the AI-driven editor, click **[!UICONTROL Manual Decision Tree]**, and then click **[!UICONTROL Yes]** to leave the AI-driven editor.

   Save any AI-editor changes you want to keep before switching. Confirming the switch discards unsaved tree changes.

1. (Optional) Change the view settings:

   * Zoom in or out by moving the slider.

   * Switch between vertical and horizontal views by clicking ![View as Vertical Tree](/help/creative/assets/tree-vertical.png "View as Vertical Tree") or ![View as Horizontal Tree](/help/creative/assets/tree-horizontal.png "View as Horizontal Tree").

   Your view settings are saved until you log out.

1. Configure the ad targets and corresponding creatives:

   * [Add a final-level target](experience-target-node-add-final.md#manual-editor), [insert a target between nodes](experience-target-node-add-inner.md#manual-editor), or [add a sibling target](experience-target-node-add-sibling.md#manual-editor).

   * [Copy child nodes and creatives](experience-target-node-copy.md#manual-editor) or [delete a node](experience-target-node-delete.md#manual-editor).

   * [Assign creative bundles](experience-assign-creative-bundles.md#manual-editor), and optionally [customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) and [tracking URLs](experience-tracking-urls-targeting.md#manual-editor).

1. (Optional) To edit the general experience settings, click **[!UICONTROL Experience Form]** and edit the [general experience settings](experience-settings-targeting.md).

1. [Save the experience](#save).

## Save the experience {#save}

The following steps apply to both editors.

{{$include /help/_includes/experience-save.md}}

## Ad tags and video transcoding for saved experiences

When the experience is live, [!DNL Creative] automatically creates one ad tag for each applicable creative size or video duration. You can then [export an ad tag and implement it in a DSP](/help/creative/experiences/experience-tag-export.md).

For video ad experiences, video creatives are transcoded automatically by Adobe Advertising DSP as VAST 2.0 tags so you can preview them. You can optionally [apply transcoding for a different DSP](experience-tag-video-transcoding.md) to any video ad experience tag.

>[!MORELIKETHIS]
>
>* [Targeted experience settings](experience-settings-targeting.md)
>* [Add a target node to the final level](experience-target-node-add-final.md)
>* [Insert a target node between nodes](experience-target-node-add-inner.md)
>* [Add a sibling target node between nodes](experience-target-node-add-sibling.md)
>* [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md)
>* [Assign creatives to a final node](experience-assign-creative-bundles.md)
>* [Customize the tracking URLs for creatives in the assigned bundles](experience-tracking-urls-targeting.md)
>* [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md)
>* [Export and implement an ad experience tag for a live experience](/help/creative/experiences/experience-tag-export.md)
>* [Edit an experience with decision tree targeting](experience-edit-targeting.md)
>* [View the change log for an experience](/help/creative/experiences/experience-view-change-log.md)
