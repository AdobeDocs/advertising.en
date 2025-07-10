---
title: Create an experience with decision tree targeting
description: Learn how to create a targeted ad experience using a decision tree.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
---
# Create an experience with decision tree targeting

*Closed beta* 

Create a targeted ad experience using a decision tree. Each experience uses ads from a single creative library.

>[!NOTE]
>
>* Once you create a targeted experience, you can't later change it to a non-targeted experience, which uses a different workflow.
>* Make sure your ad experiences include targeting that's compatible with the campaigns in which you'll implement it. Hierarchical targeting behavior may vary by DSP. When you upload an ad experience tag to Advertising DSP and attach it to a placement, ad-level targeting is applied on top of (not instead of) placement-level targeting. For example, if a placement targets users in Australia and an ad targets users in Japan, then the ad will target the "Everyone Else" branch.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Click **[!UICONTROL Create New Experience]**.

1. Enter the [general experience settings](experience-settings-targeting.md).

1. Click **[!UICONTROL Create]**.

1. In the decision tree, do the following:

   1. (Optional) Change the view settings for the decision tree.

      Your settings are saved until you log out.

      * Zoom in or out by moving the slider.

      * Switch between viewing a vertical list and a horizontal list by clicking ![View as Vertical Tree](/help/creative/assets/tree-vertical.png "View as Vertical Tree") or ![View as Horizontal Tree](/help/creative/assets/tree-horizontal.png "View as Horizontal Tree"), respectively.

   1. (Optional) Set up the ad targets and corresponding creatives in any of the following ways:

      * Targets:
      
        * [Add a target node to the final level](experience-target-node-add-final.md).
        
        * [Insert a target node between nodes](experience-target-node-add-inner.md).
        
        * [Add a sibling target node between nodes](experience-target-node-add-sibling.md).
        
        * [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md).

      * Creative bundles:

        * [Assign and unassign creatives to a final node](experience-assign-creative-bundles.md).
        
          If you don't assign at least one bundle to each final node, you can opt to use the default creatives for each unassigned node when you save the experience. To publish an experience, you must either assign bundles or use the default creatives for each final node.

        * [Customize the tracking URLs for creatives in the assigned bundles](experience-tracking-urls-targeting.md).

        * [Customize creative optimization and scheduling](experience-optimization-scheduling-targeting.md) for the assigned bundles.

1. (Optional) Switch between the decision tree and the general settings:

   * To open the general settings from the decision tree, click **[!UICONTROL Experience Form]** in the upper right.

   * To open the decision tree from the general settings, click **[!UICONTROL Decision Tree]** in the upper right.

1. Click **[!UICONTROL Save]**, and then do the following.

   * (If each node at the bottom-most level includes at least one creative bundle) Click **[!UICONTROL OK]**.
   
   * (If each node at the bottom-most level doesn't include at least one creative bundle) Do one of the following:
   
     * To save the experience without all required creative bundles, click **[!UICONTROL Save as Draft]**.
     
       You can't create an ad tag for a [draft](experience-about.md#experience-statuses) experience.

     * To assign the default creative to each target that hasn't already been assigned a creative bundle, click **[!UICONTROL Assign Default Creatives]**. After you review the updated tree with the default creatives assigned, click **[!UICONTROL Save]** and **[!UICONTROL OK]**.
     
     * To continue editing the decision tree, click **[!UICONTROL Continue Edit]**.

When the experience is live, [!DNL Creative] automatically creates an ad tag for each applicable creative size. You can then [export the ad tag and implement it in a DSP](/help/creative/experiences/experience-tag-export.md).

For video ad experiences, video creatives are transcoded automatically by DSP as VAST 2.0 tags so you can preview them. You can optionally [apply publisher-specific transcoding](experience-tag-video-transcoding.md) to any video ad experience tag.

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
