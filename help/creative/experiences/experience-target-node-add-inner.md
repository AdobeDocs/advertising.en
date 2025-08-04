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
     
        * For audience targets, select **[!UICONTROL Audience]**.
        
        * For geographical targets, select a single geographical category (such as [!UICONTROL Geo: Country]).
        
        * For data pass targets, select **[!UICONTROL Data Pass]**.
        
        * For retargeting pixel targets, select **[!UICONTROL RT Pixel].
        
        * For device targets, select a single target category (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]**, or **[!UICONTROL Device: Browser]**).

   * If sibling nodes already exist, then do the following:
   
     * For audience targets, do the following:
   
       1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Audience Targeting] options, and then do the following:
       
          * To add the first segment, locate the segment in the left panel, and select the check box next to the segment name.
          
          * To add a segment to an existing segment group:
          
            1. Click the segment group in the right panel.
            
            1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.
            
               *[!UICONTROL Exclude All]* isn't available to the first segment group. For an audience that includes only exclusions, build this audience as *[!UICONTROL Include Any]* and then exclude that audience when you add it to a placement within your DSP.
            
            1. Locate the new segment in the left panel, and select the check box next to the segment name.
            
               The segment group is automatically updated with the new segment.
        
          * To add a new segment group:
          
            1. Click **[!UICONTROL + New Group]** in the right panel.
            
            1. (Optional) Change the logic between the previous group and the new group to *[!UICONTROL And]* or *[!UICONTROL Or]*, as needed.
            
            1. Locate the segments for the new group in the left panel, and select the check boxes next to the segment names.
            
            1. (Optional) Change the group logic to *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*, or *[!UICONTROL Exclude All]*, as needed.
       
       1. Click **[!UICONTROL Create]**.
       
       1. Click **[!UICONTROL Apply]**.

     * For geographical targets, do the following:
   
       1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Geo Targeting] options, specify one or more of the geographical targets, and then click **[!UICONTROL Save]**.
       
          Zip code targets have bulk editing options. To paste multiple zip codes, click the **[!UICONTROL Paste postal codes]** tab, select the country, paste or enter zip codes separated by commas or on separate lines, and then click **[!UICONTROL Include All]**. To remove an included zip code target, hold the cursor over the target and click ![Remove](/help/creative/assets/delete.png "Remove") **[!UICONTROL Remove]**.
     
       1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.
       
          This feature creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all of the specified locations (a [!DNL Boolean] `AND` statement).

       1. Click **[!UICONTROL Apply]**.

     * For a data pass target, optionally customize the data pass key, enter a single data pass value, and then click **[!UICONTROL Apply]**.
     
       A default value for the key in the key-value pair is already set in the **[!UICONTROL Data Pass]** field in the [!UICONTROL Advanced] section of the [experience settings](experience-settings-targeting.md). You can optionally can customize the key.

     * For a retargeting pixel target, select a single retargeting pixel to use and the values for any of the pixel's attributes that are required to show the creatives, and then click **[!UICONTROL Apply]**.
     
       The attributes for the retargeting pixel are configured in the [retargeting pixel settings](/help/creative/pixels/retargeting-pixel-manage.md).

     * For device targets, do the following:
      
        1. Select the targets.
        
        1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.
        
           This feature creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all of the specified locations (a [!DNL Boolean] `AND` statement).

        1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.

        1. Click **[!UICONTROL Apply]**.

1. (Optional) Specify a custom branch name for a user-defined branch.

   By default, user-defined branches are labeled with the applied targets.

   You can't create a custom branch name for an "All" or "Everyone Else" branch. 

   1. Hold the cursor over the target node and click **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.
   
   1. Enter the **[!UICONTROL Node Name]**, and then click **[!UICONTROL Save]**.

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
