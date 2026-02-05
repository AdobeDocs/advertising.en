---
title: Customize creative optimization and scheduling for an experience
description: Learn how to configure optimization and ad scheduling for targeted experiences.
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
---
# Customize creative optimization and scheduling for an experience with decision tree targeting

*Target nodes with existing creatives only*

By default, the creative rotation for an experience is determined algorithmically to optimize the overall click-through rate, and the creative optimization settings apply to all assigned bundles. You can alternately algorithmically optimize for a specified Advertising DSP custom goal; rotate bundles according to a specified bundle sequence, with a specified number of impressions across each bundle sequence; or according to relative weights. You can also schedule specific creative bundles to run during specified, sequential time periods and apply custom creative rotation settings for each schedule.

>[!NOTE]
>
>These features aren't available for nodes that use the default creatives instead of assigned creatives.

## Configure creative optimization without scheduling

When creative scheduling is disabled, the creative optimization settings apply to all assigned creatives.

1. Hold the cursor over the creative leaf node below the target node and click **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Disable **[!UICONTROL Schedule]**.  

1. Select the creative rotation type for ad variants in the associated bundles:

   * *[!UICONTROL Weighted]:* Shows ad variants in the associated creative bundles according to relative weights. Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.<!-- For example, if Bundle 1 is 60 and Bundle 2 is 40, then Bundle 1 is shown 60% of the time, and Bundle 2 is shown 40% of the time. -->
   
   * *[!UICONTROL Algorithmic]:* Shows the most effective ad variants more often, based on a specified goal.
   
     * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (standard video ad experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* Shows the associated creative bundles in a specified order (with Bundle 1 served first, Bundle 2 served second, and so on), with a specified total number of impressions across each bundle sequence. The ad sizes that are served are determined by the available inventory. You can configure the final bundle in the sequence to a\) be displayed indefinitely (the default) or b\) loop back to the first bundle. For example, you could display any of the ad variants in Bundle 1 for three (3) impressions, then display any ad variant in Bundle 2 for one (1) impression, then display any of the ad variants in Bundle 3 for two (2) impressions, and then begin the loop again. Alternately, once the ad variants in Bundle 3 are displayed, you could continue to display the ad variants in Bundle 3 indefinitely, rather than creating a loop. When you enable sequencing:

     1. Drag and drop the assigned bundles into the desired order.

       By default, the assigned bundles are sequenced in the order in which they were added to the experience.
     
     1. Enter the number of impressions for each sequence.
     
     1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. Click **[!UICONTROL Save]**.

## Configure creative optimization with creative scheduling

You can optionally schedule specific creative bundles to run during specified, sequential time periods between the experience start and end dates, and apply custom creative rotation settings for each schedule. For example, you can schedule Bundle 1 to run during the first two weeks to optimize for click-through rate and Bundle 2 to run during the following two weeks to optimize for a specified custom goal.

When you use scheduling, you must schedule bundles through the duration of the experience.

1. Hold the cursor over the creative leaf node below the target node and click **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]**.

1. Enable **[!UICONTROL Schedule]**.

1. For the first schedule:

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives in each bundle manually according to relative weights. Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives in each bundle algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select *[!UICONTROL Click Through Rate]*, (standard video ad experiences) *[!UICONTROL Completion Rate]*, or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Rotates the associated creative bundles in a specified order (with Bundle 1 served first, Bundle 2 served second, and so on), with a specified total number of impressions across each bundle sequence. The ad sizes that are served are determined by the available inventory. You can configure the final bundle in the sequence to a\) be displayed indefinitely (the default) or b\) loop back to the first bundle. For example, you could display any of the creatives in Bundle 1 for three (3) impressions, then display any creative in Bundle 2 for one (1) impression, then display any of the creatives in Bundle 3 for two (2) impressions, and then begin the loop again. Alternately, once the creatives in Bundle 3 are displayed, you could continue to display the creatives in Bundle 3 indefinitely, rather than creating a loop. When you enable sequencing:
      
        1. Drag and drop the assigned bundles into the desired order.
        
           By default, the assigned bundles are sequenced in the order in which they were added to the experience.
        
        1. Enter the number of impressions for each sequence.
        
        1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. For each additional schedule:

   1. Click **[!UICONTROL + Add Schedule]**.

   1. In the left column, select the check box next to each creative bundle to add to the first schedule.
   
   1. Specify the start and end dates for the schedule.

   1. Select the creative rotation type:

      * *[!UICONTROL Weighted]:* Rotates the creatives in each bundle manually according to relative weights. Enter the weight for each bundle as a percentage. The weights for all selected bundles must add up to 100.

      * *[!UICONTROL Algorithmic]:* Rotates the creatives in each bundle algorithmically according to a specified optimization goal.

        * For the **[!UICONTROL Optimization Goal]**, select either *[!UICONTROL Click Through Rate]* or *[!UICONTROL Custom Objective]*.  If you select *[!UICONTROL Custom Objective]*, then select an existing [Advertising DSP custom goal](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* Rotates the associated creative bundles in a specified order, with a specified total number of impressions across each bundle sequence. When you enable sequencing:
      
        1. Drag and drop the assigned bundles into the desired order.
        
           By default, the assigned bundles are sequenced in the order in which they were added to the experience.
        
        1. Enter the number of impressions for each sequence.
        
        1. For the last sequence, change whether to a\) display the final bundle in the sequence indefinitely (*[!UICONTROL Infinite]* (the default) or b\) loop back to the first bundle after the final bundle is displayed (*[!UICONTROL Keep in Loop]*).

1. Click **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Assign and unassign creative bundles to a final node in an experience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)
