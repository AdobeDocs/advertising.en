---
title: Customize creative optimization and scheduling for an experience
description: Learn how to configure optimization and ad scheduling for targeted experiences.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
TQID: 'https://experienceleague.adobe.com/gDBTQn7F0ZNeiEylTDA9HNgDockR6FHE3MSvr0bJaDM'
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
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# Customize creative optimization and scheduling for an experience with decision tree targeting

*Target nodes with existing creatives only*

By default, an experience optimizes creative rotation for overall click-through rate across all assigned bundles. You can customize the rotation settings or schedule specific bundles to run during sequential time periods, with separate rotation settings for each schedule.

>[!NOTE]
>
>These features aren't available for nodes that use the default creatives instead of assigned creatives.

You can configure these settings directly in the canvas of the AI-driven editor (Beta) or in the manual editor. In either editor, saving the bundle dialog updates the working tree; you must also [save the experience](#save) from the tree header.

## Rotation settings {#rotation-settings}

* **[!UICONTROL Weighted]:** Shows ad variants in the associated creative bundles according to relative weights.

* **[!UICONTROL Algorithmic]:** Shows the most effective ad variants more often, based on a specified optimization goal, such as click-through rate or an Advertising DSP custom goal.

* **[!UICONTROL Sequence] (AI-driven editor) or [!UICONTROL Sequencing] (manual editor):** Shows the associated creative bundles in a specified order, with a specified number of impressions for each bundle in the sequence. By default, bundles are sequenced in the order in which they were added to the experience. The ad sizes that are served are determined by the available inventory. The final bundle can serve indefinitely (the default), or the sequence can loop back to the first bundle.

  For example, a sequence could serve ad variants from Bundle 1 for three impressions, Bundle 2 for one impression, and Bundle 3 for two impressions, and then repeat. Without looping, Bundle 3 continues to serve indefinitely.

## Configure creative optimization without scheduling

When creative scheduling is disabled, the creative optimization settings apply to all assigned creatives.

### Using the AI-driven editor (Beta) {#without-scheduling-ai}

1. While you're [creating](experience-create-targeting.md#ai-editor) or [editing](experience-edit-targeting.md#ai-editor) the experience, click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** on the creative leaf node.

   For a final node without bundles, click **[!UICONTROL Assign Bundles]** and [assign the bundles](experience-assign-creative-bundles.md#ai-editor) first.

1. Open the **[!UICONTROL Creative optimisation]** tab.

1. Disable **[!UICONTROL Schedule]**.

1. Select the creative rotation type and configure its settings:

   * **[!UICONTROL Weighted]:** Enter the relative weight for each bundle row. The weights must total 100. To distribute weights equally, click **[!UICONTROL Apply equal weight]**.

   * **[!UICONTROL Algorithmic]:** Select an **[!UICONTROL Optimization goals]** option. If you choose a custom objective, select the existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md) in **[!UICONTROL Custom objective]**.

   * **[!UICONTROL Sequence]:** Drag the bundles into the desired order, and enter the number of impressions for each sequence. Enable **[!UICONTROL Keep in loop]** to repeat the sequence, or leave it disabled to set the last bundle's impressions to **[!UICONTROL Infinite]**.

1. Click **[!UICONTROL Save]** in the dialog.

1. [Save the experience](#save).

### Using the manual editor {#without-scheduling-manual}

[Open the manual editor](experience-edit-targeting.md#experience-open) before following these steps.

1. While you're [creating](experience-create-targeting.md) or [editing](experience-edit-targeting.md) the experience, open the creative optimization settings:

   1. Hold the cursor over the creative leaf node below the target node and do the following:
   
      * For existing bundles, click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.
      
      * For new bundles, click **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** and [assign the bundles](experience-assign-creative-bundles.md).
   
   1. Click the **[!UICONTROL Creative Optimization]** tab.

1. Disable **[!UICONTROL Schedule]**.  

1. Select the creative rotation type for ad variants in the associated bundles:

   * *[!UICONTROL Weighted]:* Enter the weight for each bundle as a percentage. To apply equal weights to all associated bundles, click (![Apply equal weight](/help/creative/assets/apply-equal-weight.png "Apply equal weight")). The weights for all selected bundles must add up to 100.
   
   * *[!UICONTROL Algorithmic]:* For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (standard video ad experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*. If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:*

     1. Drag and drop the assigned bundles into the desired order.

     1. Enter the number of impressions for each sequence.
     
     1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. Click **[!UICONTROL Save]**.

## Configure creative optimization with creative scheduling

You can optionally schedule specific creative bundles to run during specified, sequential time periods between the experience start and end dates, and apply custom creative rotation settings for each schedule. For example, you can schedule Bundle 1 to run during the first two weeks to optimize for click-through rate and Bundle 2 to run during the following two weeks to optimize for a specified custom goal.

When you use scheduling, you must schedule bundles through the duration of the experience.

### Using the AI-driven editor (Beta) {#with-scheduling-ai}

1. While you're [creating](experience-create-targeting.md#ai-editor) or [editing](experience-edit-targeting.md#ai-editor) the experience, click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** on the creative leaf node.

   For a final node without bundles, click **[!UICONTROL Assign Bundles]** and [assign the bundles](experience-assign-creative-bundles.md#ai-editor) first.

1. Open the **[!UICONTROL Creative optimisation]** tab, and enable **[!UICONTROL Schedule]**.

1. Select the **[!UICONTROL Timezone]** for the schedule.

1. For the first schedule:

   1. Select the check box next to each bundle to include in the left column.

   1. Specify the start and end dates and times.

   1. Select the creative rotation type and configure its settings:

      * **[!UICONTROL Weighted]:** Enter the relative weight for each bundle row in the schedule. The weights must total 100. To distribute weights equally, click **[!UICONTROL Apply equal weight]**.

      * **[!UICONTROL Algorithmic]:** Select an **[!UICONTROL Optimization goals]** option. If you choose a custom objective, select the existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md) in **[!UICONTROL Custom objective]**.

      * **[!UICONTROL Sequence]:** Drag the bundles into the desired order, and enter the number of impressions for each sequence. Enable **[!UICONTROL Keep in loop]** to repeat the sequence, or leave it disabled to set the last bundle's impressions to **[!UICONTROL Infinite]**.

1. For each additional schedule, click **[!UICONTROL + Add Schedule]**, select its schedule card, and configure its bundles, dates and times, and rotation settings.

   The bundle check boxes apply to the selected schedule, not all schedules. Make sure the schedules cover the entire experience duration with assigned bundles.

1. Click **[!UICONTROL Save]** in the dialog.

1. [Save the experience](#save).

### Using the manual editor {#with-scheduling-manual}

[Open the manual editor](experience-edit-targeting.md#experience-open) before following these steps.

1. While you're [creating](experience-create-targeting.md) or [editing](experience-edit-targeting.md) the experience, open the creative optimization settings:

   1. Hold the cursor over the creative leaf node below the target node and do the following:
   
      * For existing bundles, click **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.
      
      * For new bundles, click **[!UICONTROL ...]** > **[!UICONTROL Assign Bundles]** and [assign the bundles](experience-assign-creative-bundles.md).

   1. Click the **[!UICONTROL Creative Optimization]** tab.

1. Enable **[!UICONTROL Schedule]**.

1. For the first schedule:

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start date and start time and the end date and end time for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Enter the weight for each bundle as a percentage. To apply equal weights to all bundles in the schedule, click (![Apply equal weight](/help/creative/assets/apply-equal-weight.png "Apply equal weight")). The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (standard video ad experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*. If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*
      
        1. Drag and drop the assigned bundles into the desired order.
        
        1. Enter the number of impressions for each sequence.
        
        1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. For each additional schedule:

   1. Click **[!UICONTROL + Add Schedule]**.

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* For the **[!UICONTROL Optimization Goal]**, select either *[!UICONTROL Click Through Rate]* or *[!UICONTROL Custom Objective]*. If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:*
      
        1. Drag and drop the assigned bundles into the desired order.
        
        1. Enter the number of impressions for each sequence.
        
        1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. Click **[!UICONTROL Save]**.

## Save the experience {#save}

The following steps apply to both editors.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Assign and unassign creative bundles to a final node in an experience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)
>* [View the change log for an experience](/help/creative/experiences/experience-view-change-log.md)
