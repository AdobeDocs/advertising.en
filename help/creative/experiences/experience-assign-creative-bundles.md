---
title: Assign and unassign creative bundles to a final node in an experience
description: Learn how to assign creatives to each target in your ad experiences.
feature: Creative Experiences
---
# Assign and unassign creative bundles to a final node in an experience

*Experiences with decision tree targeting only*
*Closed beta*

You can assign creative bundles to a target node at the bottom-most level in an experience decision tree. For experiences for which you haven't configured targets, the bottom-most level is under "All."

For standard ad experiences, you can assign only standard creative bundles. For dynamic ad experiences, you can assign only dynamic creative bundles.

>[!NOTE]
>
>If you don't assign at least one creative bundle to each final node, you can opt to use the default creatives for each unassigned node when you [save the experience](experience-create-targeting.md). To be published, the experience must be assigned either bundles or use the default creatives for all ads created from it.

<!-- The optimization and ad scheduling features and tracking URLs customization are in a different place now -- include here or in separate procedures? -->

<!-- 1. [ways to get to the decision tree] -->

1. Do one of the following:

   * (Final nodes without creatives) Under the node, click ![Add](/help/creative/assets/add.png "Add"), and then select **[!UICONTROL Assign Bundles]**.

   * (Nodes with existing creatives) Hold the cursor over the creative bundle box below the target node<!-- wording???? --> and click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Select the check box next to each bundle to assign to the target node, and deselect the check box next to each bundle to unassign.

   Only bundles of the relevant bundle type for the experience (standard or dynamic) are listed.

1. Click **[!UICONTROL Attach to Bundles]**.

1. (Optional) [Customize the tracking URLs for creatives in the assigned bundles](experience-tracking-urls-targeting.md).

1. (Optional) [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) for the assigned bundles.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

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
