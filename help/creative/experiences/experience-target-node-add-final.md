---
title: Add a target node to the final level in an experience
description: Learn how to add a target node to the final target level of an ad experience.
feature: Creative Experiences
---
# Add a target node to the final level in an experience

*Experiences with decision tree targeting only*
*Closed beta*

When you add a target node to the bottom-most level in the experience &mdash; whether it's the root "All" node, a target-specific node, or an "Everything Else" node &mdash; you define the target directly without needing to create a sibling node. This creates the target node and an additional "Everything Else" node at the same level.

>[!NOTE]
>
>To insert a target node between existing levels of an decision tree, see "[Insert a target node between nodes in an experience](experience-target-node-add-inner.md)."

<!-- 1. [ways to get to the decision tree] -->

1. Under the node at which you want to insert the target, click ![Add](/help/creative/assets/add.png "Add"), and then select **[!UICONTROL Insert New Target]**.

1. Specify the targets:

   * For Adobe Audience targets, select **[!UICONTROL Adobe Audience]**, and then do the following:
   
     1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Audience Targeting] options, open the **[!UICONTROL Adobe Segments]** tab, specify one or more of the advertiser's [!DNL Adobe] audience targets, and then click **[!UICONTROL Create]**.
     
     1. (Optional) To create multiple target nodes when multiple audiences are specified, select **[!UICONTROL Split targets to create nodes]**.

        This creates a separate target node (with separate creative bundles) for each specified audience. If you don't split the targets, then the user must belong to all specified audiences.

     1. Click **[!UICONTROL Apply]**.

   * For geographical targets, select a single geographical category (such as [!UICONTROL Geo: Country]), and then do the following:
   
     1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Geo Targeting] options, specify one or more of the geographical targets, and then click **[!UICONTROL Save]**.

        Zip code targets have bulk editing options. To paste multiple zip codes, click the **[!UICONTROL Paste postal codes]** tab, select the country, paste or enter zip codes separated by commas or on separate lines, and then click **[!UICONTROL Include All]**. To remove an included zip code target, hold the cursor over the target and click ![Remove](/help/creative/assets/delete.png "Remove") **[!UICONTROL Remove]**.
     
     1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.

        This creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all specified locations.

     1. Click **[!UICONTROL Apply]**.

   * For a data pass target, select **[!UICONTROL Data Pass]**, enter a single data pass value, and then click **[!UICONTROL Apply]**.
   
    The key for the key-value pair is already set in the **[!UICONTROL Data Pass]** field in the [!UICONTROL Advanced] section of the [experience settings](experience-settings-targeting.md).

   * For a retargeting pixel target, select **[!UICONTROL RT Pixel]**, select a single retargeting pixel to use and the required values for any of the pixel's attributes that must be present in order to show the creatives, and then click **[!UICONTROL Apply]**.
   
     The attributes for the retargeting pixel are configured in the [retargeting pixel settings](/help/creative/pixels/retargeting-pixel-manage.md).

   * For device targets, do the following:
   
     1. Select a single target category (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]**, or **[!UICONTROL Device: Browser]**), and then select the targets.
     
     1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.

        This creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all specified locations.

     1. Click **[!UICONTROL Apply]**.

1. Do any of the following:

   * (Optional) [Assign creatives](experience-assign-creative-bundles.md) to the new target node and to the "Everything Else" node.
   
   * (Optional) To save the experience:
   
     1. Click **[!UICONTROL Save]**, and then **[!UICONTROL OK]**.
     
     1. (If each node at the bottom-most level doesn't include at least one creative): Do one of the following:
     
        * To save the experience without all required creative bundles, click **[!UICONTROL Save as Draft]**.
        
          You can't create an ad tag for a draft experience.

        * To assign the default creative to each target that hasn't already been assigned a creative bundle, click **[!UICONTROL Assign Default Creatives]**. After you review the updated tree with the default creatives assigned, click **[!UICONTROL Save]** and **[!UICONTROL OK]**.
        
        * To continue editing the decision tree, click **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Insert a target node between nodes](experience-target-node-add-inner.md)
>* [Add a sibling target node between nodes](experience-target-node-add-sibling.md)
>* [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md)
>* [Assign creatives to a final node](experience-assign-creative-bundles.md)
>* [Delete a target node or creative leaf node](/help/creative/experiences/experience-target-node-delete.md)
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Edit an experience with decision tree targeting](experience-edit-targeting.md)
>* [Targeted experience settings](experience-settings-targeting.md)
