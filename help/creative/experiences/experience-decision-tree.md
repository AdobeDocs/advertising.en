---
title: The decision tree layout
description: Learn about the AI-driven and manual decision tree editors for experiences with targeting.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
TQID: 'https://experienceleague.adobe.com/JFrcVBHxv90Fchk-VfkmxAITQJswboszNMFOfaAQlL4'
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
# The decision tree layout for [!DNL Creative] experiences

When you enable the "[!UICONTROL Targeting]" option for an experience, you set up the experience using a decision tree.

Initially, each decision tree begins with the root level, "All." You can add one or more target nodes, and then assign creative bundles to the final nodes in each branch of the decision tree.

## AI-driven editor (Beta) {#ai-editor}

The AI-driven editor opens by default when you create or edit an experience with targeting. It combines a conversation with the AI agent and an interactive decision tree canvas.

* Describe the targeting structure or changes you want in the conversation, and review the resulting tree before saving.

* Edit the canvas directly to add target levels and nodes, assign bundles, and configure creative optimization and tracking URLs. You don't need to switch to the manual editor to use these controls.

* View the experience name, status, and advertiser in the header, and use node IDs, when available, to identify target nodes when you describe changes.

* Use **[!UICONTROL Zoom in]**, **[!UICONTROL Zoom out]**, and **[!UICONTROL Change orientation]** to adjust the view. **[!UICONTROL Reset tree]** clears the tree after confirmation; it doesn't just reset the zoom.

While the assistant is processing a change, the canvas and its **[!UICONTROL Save]** button are temporarily disabled. Wait for processing to finish before making another canvas change.

## Manual editor {#manual-editor}

To open the existing manual editor from the AI-driven editor, click **[!UICONTROL Manual Decision Tree]**. You can also select **[!UICONTROL Create Decision Tree Manually (Legacy)]** from the experience's actions in the [!UICONTROL Experiences] view. See [Switch editors or edit the experience settings](experience-edit-targeting.md#switch-editors).

In the manual editor, the tree is displayed vertically by default. You can change to a horizontal view and adjust the zoom with a slider. Your view settings are saved until you log out.

The following examples show the manual editor:

![Example of a vertical decision tree without targets](/help/creative/assets/experience-decision-tree-no-targets.png "Example of a vertical decision tree without targets")

![Example of a horizontal decision tree without targets](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png "Example of a horizontal decision tree without targets")

>[!IMPORTANT]
>
>Save any changes you want to keep before leaving the AI-driven editor. Clicking **[!UICONTROL Manual Decision Tree]**, **[!UICONTROL Experience Form]**, or **[!UICONTROL Cancel]** opens a confirmation dialog. Clicking **[!UICONTROL Yes]** discards unsaved tree changes; clicking **[!UICONTROL No]** keeps you in the editor.

## Terms

**Tree:** The overall decisioning structure as a tree with branches.

**Target Node:** A target within a branch.

**Leaf Node:** A set of creatives assigned to a final target node.

## Targets in a decision tree

Each decision tree can have up to five levels of targets. The experience-level targets are applied in conjunction with your DSP's targeting options; hierarchical targeting behavior may vary by DSP. Make sure that your ad experiences include targeting that's compatible with the campaigns in which you'll implement it.

Each target level can include multiple branches, each with one or more nodes with the same target type (audience segment, geographical location type, values for specified data pass keys, attributes for a specified retargeting pixel, or device category). You can assign creative bundles in each ad size for which you've specified a default image creative or video creative to the lowest-level target nodes.

<!-- Add a screen shot of the AI editor -->The following example shows targets in the manual editor:

![Example of a decision tree with targets](/help/creative/assets/experience-decision-tree.png "Example of a decision tree with targets")

When you add a target node to the final level, you specify the target for the new node. An additional sibling node, "Everything Else," is automatically created for everyone who doesn't match the specified target. You can then add additional sibling nodes with different targets of the same type.

When you insert a target node between existing levels, however, the first node for the new level is initially assigned to "All." To identify a specific target, create a sibling target node at the same level, for which you specify the actual target. This action creates the target node and replaces the "All" node with an "Everything Else" node (which includes all creative bundles previously assigned to All). You can then add additional sibling nodes with different targets of the same type.

For all parent nodes, you can optionally copy all child target nodes and creative bundles and paste them into another node at the same level. You can either add the pasted nodes to the existing framework or replace the existing framework with them.

## Creatives in a decision tree

Assign creative bundles to each final target node in the experience.

Within each node with creative bundles, you can optionally rotate the included creatives a) algorithmically to optimize the click-through rate or a custom objective, b) according to specified weights, or c) in a specific sequence. You can also optionally rotate the creatives in a specified time sequence any combination of the same options.

You can optionally customize the landing page URLs, impression-tracking URLs, and click-tracking URLs, as needed for individual creatives. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [About experiences in Advertising Creative 2.0](experience-about.md)
>* [Create an experience with targeting](/help/creative/experiences/experience-create-targeting.md)
>* [Targeted experience settings](/help/creative/experiences/experience-settings-targeting.md)
