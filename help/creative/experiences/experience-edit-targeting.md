---
title: Edit an experience with decision tree targeting
description: Learn how to edit the settings for a targeted ad experience using a decision tree.
feature: Creative Experiences
---
# Edit an experience with decision tree targeting

*Closed beta*

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific experiences.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Edit]**.
   
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Edit]**.

1. Edit the [general experience settings](experience-settings-targeting.md).

1. (Optional) To edit the decision tree, click **[!UICONTROL Decision Tree]** in the upper right, and then do any of the following:

   * ([Processing](experience-about.md#experience-statuses) experiences) Do one of the following:
   
      * To discard the existing, unposted changes to the live experience, click **[!UICONTROL Discard and start again]**.
      
      * To keep the existing, unposted changes, click **[!UICONTROL Continue editing draft]**.
      
      * To edit the experience details, click **[!UICONTROL Edit Experience Details]**.

   * (Optional) Change the view settings for the decision tree.
   
     Your settings are saved until you log out.
   
   * Zoom in or out by moving the slider.
   
   * Switch between viewing a vertical list and a horizontal list by clicking ![View as Vertical Tree](/help/creative/assets/tree-vertical.png "View as Vertical Tree") or ![View as Horizontal Tree](/help/creative/assets/tree-horizontal.png "View as Horizontal Tree"), respectively.

   * (Optional) Change up the ad targets and corresponding creatives in any of the following ways:
   
     * Targets:
     
       *[Add a target node to the final level](experience-target-node-add-final.md) in an experience.
       
       * [Insert a target node between nodes](experience-target-node-add-inner.md).
       
       * [Add a sibling target node between nodes](experience-target-node-add-sibling.md).
       
       * [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md).

     * Creative bundles:
     
       * [Assign and unassign creatives to a final node](experience-assign-creative-bundles.md).
       
         If you don't assign at least one bundle to each final node, you can opt to use the default creatives for each unassigned node when you save the experience. To be published, the experience must be assigned either bundles or use the default creatives for all ads created from it.
       
       * [Customize the tracking URLs for creatives in the assigned bundles](experience-tracking-urls-targeting.md).
       
       * [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) for the assigned bundles.

1. Click **[!UICONTROL Save]**, and then do the following.

   * (If each node at the bottom-most level includes at least one creative bundle) Click **[!UICONTROL OK]**.
   
   * (If each node at the bottom-most level doesn't include at least one creative bundle) Do one of the following:
   
     * To save the experience without all required creative bundles, click **[!UICONTROL Save as Draft]**.
     
       You can't create an ad tag for a [draft](experience-about.md#experience-statuses) experience.

     * To assign the default creative to each target that hasn't already been assigned a creative bundle, click **[!UICONTROL Assign Default Creatives]**. After you review the updated tree with the default creatives assigned, click **[!UICONTROL Save]** and **[!UICONTROL OK]**.
     
     * To continue editing the decision tree, click **[!UICONTROL Continue Edit]**.

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
