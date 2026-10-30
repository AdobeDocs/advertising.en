---
title: Add a target node between nodes in an experience
description: Learn how to add a target node between target bodes in an ad experience.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
---
# Add a target node between nodes in an experience

*Experiences with decision tree targeting only*

When you insert a target node between existing levels, the new target node retains all existing child targets and creatives, and the new node initially is called "All." You can optionally keep the new node without adding more specific targets.

To define a specific target, add an additional sibling target node at the same level, specify the new target, and then assign creatives to just that target. Adding a sibling target node creates the new target node and moves all child targets and creatives that were previously assigned to "All" to a new "Everything Else" node at the same level. This way, the addition of the new target doesn't affect the existing child branches because only the new sibling node includes the new targeting information.

>[!NOTE]
>
>To add a target node to the bottom level of a decision tree, see "[Add a target node to the final level in an experience](experience-target-node-add-final.md)."

## Using the AI-driven editor (Beta) {#ai-editor}

While you're [creating](experience-create-targeting.md#ai-editor) or [editing](experience-edit-targeting.md#ai-editor) the experience, you can ask the AI agent to insert a target level. Identify where to insert it and which existing branches and creatives to retain, and review the result. To insert the level directly in the canvas:

1. At the boundary where you want to insert the level, click **[!UICONTROL Add targeting level]**.

   In horizontal view, this control is an icon with the same label.

1. In **[!UICONTROL New targeting level]**, select the target category, and then click **[!UICONTROL Add targeting level]**.

   * For audience targets, select **[!UICONTROL Audience]**.

   * For geographical targets, select a single geographical category (such as **[!UICONTROL Geo: Country]**).

   * For data pass targets, select **[!UICONTROL Data Pass]**.

   * For retargeting pixel targets, select **[!UICONTROL RT Pixel]**.

   * For device targets, select a single target category (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]**, or **[!UICONTROL Device: Browser]**).

   Inserting a level doesn't prompt for target values. The new level initially uses "All" and retains the existing child targets and creatives.

1. (Optional) To define a specific target at the new level, [add a sibling target node](experience-target-node-add-sibling.md#ai-editor). Otherwise, keep the new "All" node without adding specific targets.

1. (Optional) To rename a user-defined target node, click **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, enter the **[!UICONTROL Node Name]**, and then click **[!UICONTROL Save]**.

   You can't rename an "All" or "Everyone Else" node.

1. Review the retained branches, and [assign creative bundles](experience-assign-creative-bundles.md#ai-editor) to any new final nodes.

1. [Save the experience](#save).

## Using the manual editor {#manual-editor}

[Open the manual editor](experience-edit-targeting.md#experience-open) before following these steps.

1. Under the node at which you want to insert the target, click ![Add](/help/creative/assets/add.png "Add"), and then select **[!UICONTROL Insert New Target]**.

1. Do one of the following:

   * If sibling nodes don't already exist, then do the following:
   
     1. Select the target type, and then click **[!UICONTROL Apply]**:
     
        * For audience targets, select **[!UICONTROL Audience]**.
        
        * For geographical targets, select a single geographical category (such as **[!UICONTROL Geo: Country]**).
        
        * For data pass targets, select **[!UICONTROL Data Pass]**.
        
        * For retargeting pixel targets, select **[!UICONTROL RT Pixel]**.
        
        * For device targets, select a single target category (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]**, or **[!UICONTROL Device: Browser]**).

   * If sibling nodes already exist, then do the following:
   
     * For audience targets:

        1. Click **[!UICONTROL Click to Browse]** to open the **[!UICONTROL Audience Targeting]** options.

        1. Configure the audience segments and groups:

           * To add the first segment, locate the segment in the left panel, and select the check box next to the segment name.

           * To add segments to an existing segment group:

              1. Click the segment group in the right panel.

              1. (Optional) Change the group logic to **[!UICONTROL Include Any]**, **[!UICONTROL Include All]**, or **[!UICONTROL Exclude All]**, as needed.

                 **[!UICONTROL Include Any]** matches users in at least one selected segment; **[!UICONTROL Include All]** requires membership in all selected segments.

                 **[!UICONTROL Exclude All]** isn't available for the first segment group. For an audience that includes only exclusions, build the audience using **[!UICONTROL Include Any]**, and then exclude that audience when you add it to a placement within your DSP.

              1. Locate the new segment in the left panel, and select the check box next to the segment name. Repeat for each additional segment.

                 The segment group is automatically updated with the new segments.

           * To add a new segment group:

              1. Click **[!UICONTROL + New Group]** in the right panel.

              1. (Optional) Change the logic between the previous group and the new group to **[!UICONTROL And]** or **[!UICONTROL Or]**, as needed.

                 **[!UICONTROL And]** requires users to meet both groups' conditions; **[!UICONTROL Or]** requires them to meet at least one group's conditions.

              1. Locate the segments for the new group in the left panel, and select the check boxes next to the segment names.

              1. (Optional) Change the group logic to **[!UICONTROL Include Any]**, **[!UICONTROL Include All]**, or **[!UICONTROL Exclude All]**, as needed.

        1. Click **[!UICONTROL Create]**.

        1. Click **[!UICONTROL Apply]**.

     * For geographical targets, do the following:
   
       1. Click **[!UICONTROL Click to Browse]** to open your [!UICONTROL Geo Targeting] options, specify one or more of the geographical targets, and then click **[!UICONTROL Save]**.
       
          Zip code targets have bulk editing options. To paste multiple zip codes, click the **[!UICONTROL Paste postal codes]** tab, select the country, paste or enter zip codes separated by commas or on separate lines, and then click **[!UICONTROL Include All]**. To remove an included zip code target, hold the cursor over the target and click ![Remove](/help/creative/assets/delete.png "Remove") **[!UICONTROL Remove]**.
     
       1. (Optional) To create multiple target nodes when multiple geographical targets are specified, select **[!UICONTROL Split targets to create nodes]**.
       
          This feature creates a separate target node (with separate creative bundles) for each specified geographical target. If you don't split the targets, then the user must belong to all of the specified locations (a [!DNL Boolean] `AND` statement).

       1. Click **[!UICONTROL Apply]**.

     * For a data pass target, optionally customize the data pass key, enter a single data pass value, and then click **[!UICONTROL Apply]**.
     
       The default data pass key is configured in the **[!UICONTROL Data Pass]** field in the **[!UICONTROL Advanced]** section of the [general experience settings](experience-settings-targeting.md). Customize the key for the target if needed.

     * For a retargeting pixel target, select a single retargeting pixel to use and the values for any of the pixel's attributes that are required to show the creatives, and then click **[!UICONTROL Apply]**.
     
       The available attributes are configured in the [retargeting pixel settings](/help/creative/pixels/retargeting-pixel-manage.md).

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

1. (Optional) [Assign creative bundles](experience-assign-creative-bundles.md#manual-editor) to the new target node and to the "Everything Else" node.

1. (Optional) [Add a sibling target node](experience-target-node-add-sibling.md#manual-editor) of the specified target type.

## Save the experience {#save}

The following steps apply to both editors.

{{$include /help/_includes/experience-save.md}}

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
