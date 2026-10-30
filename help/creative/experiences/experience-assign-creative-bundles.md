---
title: Assign and unassign creative bundles to a final node in an experience
description: Learn how to assign creatives to each target in your ad experiences.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: 'https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M'
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
# Assign and unassign creative bundles to a final node in an experience

*Experiences with decision tree targeting only*

You can assign creative bundles to a target node at the bottom-most level in an experience decision tree. For experiences for which you haven't configured targets, the bottom-most level is under "All."

For standard ad experiences, you can assign only standard creative bundles. For dynamic ad experiences, you can assign only dynamic creative bundles.

>[!NOTE]
>
>If you don't assign at least one creative bundle to each final node, you can opt to use the default creatives for each unassigned node when you [save the experience](experience-create-targeting.md). To publish an experience, you must either assign bundles or use the default creatives for each final node.

## Using the AI-driven editor (Beta) {#ai-editor}

While you're [creating](experience-create-targeting.md#ai-editor) or [editing](experience-edit-targeting.md#ai-editor) the experience, use the canvas controls:

1. Do one of the following:

   * For a final node without bundles, click **[!UICONTROL Assign Bundles]**.

   * For a node with existing bundles, click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** on its creative leaf node.

1. On the **[!UICONTROL Assign Bundles]** tab, select the check box next to each bundle to assign, and deselect the check box next to each bundle to unassign.

   Only bundles of the relevant type for the experience (standard or dynamic) are listed.

1. (Optional) Open the **[!UICONTROL Creative optimisation]** tab to [customize rotation and scheduling](experience-optimization-scheduling-targeting.md).

1. Click **[!UICONTROL Save]** in the dialog to update the working tree.

1. (Optional) [Customize the tracking URLs](experience-tracking-urls-targeting.md#ai-editor).

1. [Save the experience](#save) from the tree header to persist your changes.

## Using the manual editor {#manual-editor}

[Open the manual editor](experience-edit-targeting.md#experience-open) before following these steps.

1. Do one of the following:

   * (Final nodes without creatives) Under the node, click **[!UICONTROL Assign Bundles]**.

   * (Nodes with existing creatives) Hold the cursor over the creative bundle box below the target node and click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Select the check box next to each bundle to assign to the target node, and deselect the check box next to each bundle to unassign.

   Only bundles of the relevant bundle type for the experience (standard or dynamic) are listed.

1. Click **[!UICONTROL Save]**.

1. (Optional) [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) for the assigned bundles.

1. (Optional) [Customize the tracking URLs for creatives in the assigned bundles](experience-tracking-urls-targeting.md).

## Save the experience {#save}

The following steps apply to both editors. Saving the bundle dialog alone doesn't save or publish the experience.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Add a target node to the final level](experience-target-node-add-final.md)
>* [Insert a target node between nodes](experience-target-node-add-inner.md)
>* [Add a sibling target node between nodes](experience-target-node-add-sibling.md)
>* [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md)
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Edit an experience with decision tree targeting](experience-edit-targeting.md)
>* [Targeted experience settings](experience-settings-targeting.md)
>* [Export and implement an ad experience tag for a live experience](experience-tag-export.md)
>* [View the change log for an experience](/help/creative/experiences/experience-view-change-log.md)
