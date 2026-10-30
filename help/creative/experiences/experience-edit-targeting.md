---
title: Edit an experience with decision tree targeting
description: Learn how to edit a targeted ad experience using the AI-driven or manual decision tree editor.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
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
# Edit an experience with decision tree targeting

The AI-driven editor (Beta) opens by default for experiences with targeting. You can work with the AI agent, edit the canvas directly, or open the existing manual editor.

## Open the experience {#experience-open}

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific experiences.

1. Do one of the following:

   * To open the AI-driven editor:

      * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Edit]**.

      * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Edit]**.

   * To open the manual editor:

      * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

      * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

      * Within the AI-driven editor, 

## Edit using the AI-driven editor (Beta) {#ai-editor}

1. [Open the experience](#experience-open).

1. Describe the targeting changes you want in the conversation. Identify the affected branch by its targets or, when shown on the canvas, its node ID.

1. Review the updated tree, and describe any further changes. Wait for the assistant to finish processing before interacting with the canvas.

1. (Optional) Make changes directly in the canvas:

   * [Add a final-level target](experience-target-node-add-final.md#ai-editor), [insert a target level](experience-target-node-add-inner.md#ai-editor), or [add a sibling target](experience-target-node-add-sibling.md#ai-editor).

   * Edit a target's criteria by clicking **[!UICONTROL ...]** > **[!UICONTROL Edit]** next to the target, changing the values, and then clicking **[!UICONTROL Edit Node]**.

   * [Copy child nodes and creatives](experience-target-node-copy.md#ai-editor) or [delete a node](experience-target-node-delete.md#ai-editor).

   * [Assign or unassign creative bundles](experience-assign-creative-bundles.md#ai-editor).

   * [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) or [tracking URLs](experience-tracking-urls-targeting.md#ai-editor).

1. [Save the experience](#save).

## Edit using the manual editor {#manual-editor}

1. [Open the experience](#experience-open).

1. (Experiences with status `[processing](experience-about.md#experience-statuses)`) If prompted about an existing, unposted draft, do one of the following:

   * Click **[!UICONTROL Continue editing draft]** to review and keep editing the draft.

   * Click **[!UICONTROL Discard and start again]** to discard the draft and start from the live version.

   * Click **[!UICONTROL Cancel this edit]** to stop editing.

1. (Optional) Adjust the zoom slider, or click ![View as Vertical Tree](/help/creative/assets/tree-vertical.png "View as Vertical Tree") or ![View as Horizontal Tree](/help/creative/assets/tree-horizontal.png "View as Horizontal Tree") to change the orientation.

   Your view settings are saved until you log out.

1. Change the targets and creatives as needed:

   * [Add a final-level target](experience-target-node-add-final.md#manual-editor), [insert a target between nodes](experience-target-node-add-inner.md#manual-editor), or [add a sibling target](experience-target-node-add-sibling.md#manual-editor).

   * [Copy child nodes and creatives](experience-target-node-copy.md#manual-editor) or [delete a node](experience-target-node-delete.md#manual-editor).

   * [Assign or unassign creative bundles](experience-assign-creative-bundles.md#manual-editor).

   * [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) or [tracking URLs](experience-tracking-urls-targeting.md#manual-editor).

1. [Save the experience](#save).

## Switch editors or edit the experience settings {#switch-editors}

>[!IMPORTANT]
>
>Before leaving the AI-driven editor, save any tree changes you want to keep. Switching to the manual editor or experience form doesn't transfer unsaved changes.

* **AI-driven editor to manual editor:** Click **[!UICONTROL Manual Decision Tree]**. In the confirmation dialog, click **[!UICONTROL Yes]** to discard unsaved changes and open the manual editor, or **[!UICONTROL No]** to stay.

* **AI-driven editor to general settings:** Click **[!UICONTROL Experience Form]**, and then click **[!UICONTROL Yes]** to discard unsaved tree changes and open the form. Edit the [general experience settings](experience-settings-targeting.md), and then click **[!UICONTROL Save]**.

* **Manual editor to general settings:** Save any tree changes you want to keep, and then click **[!UICONTROL Experience Form]**. Edit the [general experience settings](experience-settings-targeting.md), and then click **[!UICONTROL Save]**.

* **General settings to AI-driven editor:** Click **[!UICONTROL Decision Tree]**. Saving changes to a targeted experience's general settings also opens the AI-driven editor.

* **Manual editor to AI-driven editor:** Save your tree changes, return to the [!UICONTROL Experiences] view, and select **[!UICONTROL Edit]** for the experience.

To leave the AI-driven editor without opening another editor, click **[!UICONTROL Cancel]**. Click **[!UICONTROL Yes]** to discard unsaved tree changes, or **[!UICONTROL No]** to continue editing.

## Save the experience {#save}

The following steps apply to both editors.

{{$include /help/_includes/experience-save.md}}

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
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [View the change log for an experience](/help/creative/experiences/experience-view-change-log.md)
