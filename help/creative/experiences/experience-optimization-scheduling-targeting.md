---
title: Customize creative optimization and scheduling for an experience
description: Learn how to
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
---
# Customize creative optimization and scheduling for an experience with decision tree targeting

*Target nodes with existing creatives only*
*Closed beta*

By default, the creative rotation for an experience is determined algorithmically to optimize the overall click-through rate, and the creative optimization settings apply to all assigned bundles. You can customize the creative rotation to manually run the creatives in each bundle according to relative weights or to algorithmically optimize for a specified Advertising DSP custom goal. You can also schedule specific creative bundles to run during specified, sequential time periods and apply custom creative rotation settings for each schedule.

>[!NOTE]
>
>These features aren't available for nodes that use the default creatives instead of assigned creatives.

## Configure creative optimization without scheduling

When creative scheduling is disabled, the creative optimization settings apply to all assigned creatives.

1. Hold the cursor over the creative leaf node below the target node and click **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Disable **[!UICONTROL Schedule]**.  

1. Select the creative rotation type:

   * *[!UICONTROL Weighted]:* Rotates the creatives in each bundle manually according to relative weights. Enter the weight for each bundle as a percentage. The weights for all bundles must add up to 100.
   
   * *[!UICONTROL Algorithmic]:* Rotates the creatives in each bundle algorithmically according to a specified optimization goal.
   
     * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (video experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

1. Click **[!UICONTROL Save]**.

## Configure creative optimization with creative scheduling

You can optionally schedule specific creative bundles to run during specified, sequential time periods between the experience start and end dates, and apply custom creative rotation settings for each schedule. For example, you can schedule Bundle 1 to run during the first two weeks to optimize for click-through rate and Bundle 2 to run during the following two weeks to optimize for a specified custom goal.

When you use scheduling, you must schedule bundles through the duration of the experience.

1. Hold the cursor over the creative leaf node below the target node and click **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]**.

1. Enable **[!UICONTROL Schedule]**.

1. For the first schedule:

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives in each bundle manually according to relative weights. Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives in each bundle algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (video experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

1. For each additional schedule:

   1. Click **[!UICONTROL + Add Schedule]**.

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives in each bundle manually according to relative weights. Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives in each bundle algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select either *[!UICONTROL Click Through Rate]* or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Assign and unassign creative bundles to a final node in an experience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)
