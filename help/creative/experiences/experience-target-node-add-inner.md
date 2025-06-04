---
title: Add a target node between nodes in an experience
description: Learn how to add a target node between target bodes in an ad experience.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
---
# Add a target node between nodes in an experience

*Experiences with decision tree targeting only*
*Closed beta*

When you insert a target node between existing levels, the new target node retains all existing child targets and creatives, and the new node initially is called "All." You can optionally keep the new node without adding more specific targets.

To define a specific target, add an additional sibling target node at the same level, specify the new target, and then assign creatives to just that target. Adding a sibling target node creates the new target node and moves all child targets and creatives that were previously assigned to "All" to a new "Everything Else" node at the same level. This way, the addition of the new target doesn't affect the existing child branches because only the new sibling node includes the new targeting information.

>[!NOTE]
>
>To add a target node to the bottom level of a decision tree, see "[Add a target node to the final level in an experience](experience-target-node-add-final.md)."

<!-- 1. [ways to get to the decision tree] -->

1. Under the node at which you want to insert the target, click ![Add](/help/creative/assets/add.png "Add"), and then select **[!UICONTROL Insert New Target]**.

1. Do one of the following:

   * If sibling nodes don't already exist, then do the following:
   
     1. Select the target type, and then click **[!UICONTROL Apply]**:
     
        * For Adobe Audience targets, select **[!UICONTROL Adobe Audience]**.
        
        * For geographical targets, select a single geographical category (such as [!UICONTROL Geo: Country]).
        
        * For data pass targets, select **[!UICONTROL Data Pass]**.
        
        * For retargeting pixel targets, select **[!UICONTROL RT Pixel].
        
        * For device targets, select a single target category (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]**, or **[!UICONTROL Device: Browser]**).

   * If sibling nodes already exist, then do the following:
   
     * For Adobe Audience targets, do the following:
     
       1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Audience Targeting] options, open the **[!UICONTROL Adobe Segments]** tab, specify one or more of the advertiser's [!DNL Adobe] audience targets, and then click **[!UICONTROL Create]**<!-- Why not "Save" like for the other node types/use cases? -->.
       
       1. (Optional) To create multiple target nodes when multiple audiences are specified, select **[!UICONTROL Split targets to create nodes]**.
       
          This feature creates a separate target node (with separate creative bundles) for each specified audience. If you don't split the targets, then the user can belong to any of the specified audiences (a [!DNL Boolean] `OR` statement). **Note:** Unsplit *location* targets use (a [!DNL Boolean] `AND` statement) instead.
          
       1. Click **[!UICONTROL Apply]**.

     * For geographical targets, do the following:
   
       1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Geo Targeting] options, specify one or more of the geographical targets, and then click **[!UICONTROL Save]**.
       
          Zip code targets have bulk editing options. To paste multiple zip codes, click the **[!UICONTROL Paste postal codes]** tab, select the country, paste or enter zip codes separated by commas or on separate lines, and then click **[!UICONTROL Include All]**. To remove an included zip code target, hold the cursor over the target and click ![Remove](/help/creative/assets/delete.png "Remove") **[!UICONTROL Remove]**.
     
       1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.
       
          This feature creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all of the specified locations (a [!DNL Boolean] `AND` statement). **Note:** Unsplit *audience* targets use (a [!DNL Boolean] `OR` statement) instead.

       1. Click **[!UICONTROL Apply]**.

     * For a data pass target, enter a single data pass value, and then click **[!UICONTROL Apply]**.
     
       The key for the key-value pair is already set in the **[!UICONTROL Data Pass]** field in the [!UICONTROL Advanced] section of the [experience settings](experience-settings-targeting.md).

     * For a retargeting pixel target, select a single retargeting pixel to use and the values for any of the pixel's attributes that are required to show the creatives, and then click **[!UICONTROL Apply]**.
     
       The attributes for the retargeting pixel are configured in the [retargeting pixel settings](/help/creative/pixels/retargeting-pixel-manage.md).

     * For device targets, do the following:
      
        1. Select the targets.
        
        1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.
        
           This feature creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all of the specified locations (a [!DNL Boolean] `AND` statement). **Note:** Unsplit *audience* targets use (a [!DNL Boolean] `OR` statement) instead.

        1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.

        1. Click **[!UICONTROL Apply]**.

1. Do any of the following:

   * (Optional) [Assign creatives](experience-assign-creative-bundles.md) to the new target node and to the "Everything Else" node.

   * (Optional) [Add a sibling target node](experience-target-node-add-sibling.md) of the specified target type.
   
   * (Optional) To save the experience:
   
     1. Click **[!UICONTROL Save]**, and then **[!UICONTROL OK]**.
     
     1. (If each node at the bottom-most level doesn't include at least one creative): Do one of the following:
     
        * To save the experience without all required creative bundles, click **[!UICONTROL Save as Draft]**.
        
          You can't create an ad tag for a draft experience.
        
        * To assign the default creative to each target that hasn't already been assigned a creative bundle, click **[!UICONTROL Assign Default Creatives]**. After you review the updated tree with the default creatives assigned, click **[!UICONTROL Save]** and **[!UICONTROL OK]**.
        
        * To continue editing the decision tree, click **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Add a target node to the final level](experience-target-node-add-final.md)
>* [Add a sibling target node between nodes](experience-target-node-add-sibling.md)
>* [Copy child nodes and creatives to another node at the same level](experience-target-node-copy.md)
>* [Assign creatives to a final node](experience-assign-creative-bundles.md)
>* [Delete a target node or creative leaf node](/help/creative/experiences/experience-target-node-delete.md)
>* [Create an experience with decision tree targeting](experience-create-targeting.md)
>* [Edit an experience with decision tree targeting](experience-edit-targeting.md)
>* [Targeted experience settings](experience-settings-targeting.md)
