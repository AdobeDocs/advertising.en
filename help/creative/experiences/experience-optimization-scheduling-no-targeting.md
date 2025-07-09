---
title: Customize creative optimization and scheduling for an experience
description: Learn how to
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
---
# Customize creative optimization and scheduling for an experience without decision tree targeting

*Experiences with existing creatives only*
*Closed beta*

By default, the creative rotation for an ad experience tag is determined algorithmically to optimize the overall click-through rate, and the creative optimization settings apply to all assigned creatives. You can customize the creative rotation to manually run the creatives according to relative weights or to algorithmically optimize for a specified Advertising DSP custom goal. You can also schedule specific creatives to run during specified, sequential time periods and apply custom creative rotation settings for each schedule.

## Configure creative optimization without scheduling

When creative scheduling is disabled, the creative optimization settings apply to all assigned creatives.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Tag Manager]**.
     
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Tag Manager]**.

1. Hold the cursor over the row for the applicable ad tag and click ![Ad Schedule](/help/creative/assets/edit-gray.png "Edit tracking URLs") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" --><!-- Tag Manager has only a list view, but no card view, as of 2/2. >

1. Disable **[!UICONTROL Schedule]**.

1. Select the creative rotation type:

   * *[!UICONTROL Weighted]:* Rotates the creatives manually according to relative weights. Enter the weight for each creative as a percentage. The weights for all selected creatives must add up to 100.
   
   * *[!UICONTROL Algorithmic]:* Rotates the creatives algorithmically according to a specified optimization goal.
   
     * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (video experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Click **[!UICONTROL Save]**.

## Configure creative optimization with creative scheduling

You can optionally schedule specific creatives used for an ad experience tag to run during specified, sequential time periods between the experience start and end dates, and apply custom creative rotation settings for each schedule. For example, you can schedule Creative 1 to run during the first two weeks to optimize for click-through rate and Creative 2 to run during the following two weeks to optimize for a specified custom goal.

When you use scheduling, you must schedule creatives through the duration of the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Do one of the following:

   * In card view, click **[!UICONTROL ...]** next to the experience name, and then click **[!UICONTROL Tag Manager]**.
     
   * In table view, hold the cursor over the row, click **[!UICONTROL More]**, and then click **[!UICONTROL Tag Manager]**.

1. Hold the cursor over the row for the applicable ad tag and click ![Ad Schedule](/help/creative/assets/edit-gray.png "Edit tracking URLs") **[!UICONTROL Ad Schedule]**. <!-- For targeted experiences, this is "Edit Schedules" --><!-- Tag Manager has only a list view, but no card view, as of 2/2. >

1. Enable **[!UICONTROL Schedule]**.

1. For the first schedule:

   1. In the left column, select the check box next to each creative to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives manually according to relative weights. Enter the weight for each creative as a percentage. The weights for all selected creatives must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (video experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. For each additional schedule:

   1. Click **[!UICONTROL + Add Schedule]**.

   1. In the left column, select the check box next to each creative to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives manually according to relative weights. Enter the weight for each creative as a percentage. The weights for all selected creatives must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select either *[!UICONTROL Click Through Rate]* or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).<!-- Verify -->

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Manually create an ad tag for an applicable creative size](/help/creative/experiences/experience-tag-create-manually.md)
>* [Assign creatives to an ad tag for experiences without targeting](experience-tag-assign-creatives.md)
>* [Customize the tracking URLs for an experience without decision tree targeting](experience-tracking-urls-no-targeting.md)
