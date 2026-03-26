---
title: Best practices for custom goals
description: Learn about the best practices for defining custom goals for packages optimized for the lowest CPA or the highest ROAS.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
---
# Best practices for custom goals

<!-- rewrite and/or move into "Manage Custom Goals" -->

Custom goals define the success events that an advertiser requires to meet its business objectives. Each package that uses the optimization goal "[!UICONTROL Highest Return on Ad Spend (ROAS)"] or "[!UICONTROL Lowest Cost per Acquisition (CPA)]" must include a custom goal to help achieve the overall optimization goal. You can create custom goals as *[custom objectives](/help/dsp/admin/custom-objectives-manage.md)*. The name of each objective for DSP must be prefixed with "ADSP_".

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Each custom goal (objective) consists of one or more conversion metrics to be tracked and optimized, and the relative weights of those metrics. You can [assign a custom goal to a package](/help/dsp/campaign-management/packages/package-settings.md) for reporting and algorithmic optimization using [!DNL Adobe AI].

To create and manage custom goals, see "[Manage Custom Objectives](/help/dsp/admin/custom-objectives-manage.md)."

## Custom goals with a single metric

The following examples show how you might configure goals that target a single conversion metric.

### Example for a campaign with the "[!UICONTROL Highest Return on Ad Spend (ROAS)]" optimization goal

If your campaign goal is revenue ([!UICONTROL Highest Return on Ad Spend (ROAS)]), and revenue from all device types is equally important to you, then include the "[!UICONTROL Revenue]" metric with a weight of one (1). Select the metric type *[!UICONTROL Goal]*.

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> A weight of one (1) equates to a value of one (1) for each $1 of revenue that's tracked for display ads on any device. For example, a $250 conversion with a weight of one (1) is reported as $250 for conversions. If the conversion metric is assigned a weight of 0.5, then the $250 conversion is reported as $125 in Adobe Advertising ($250 Conversion * 0.5 [!UICONTROL weight] = $125).

### Example for a campaign with the "[!UICONTROL Lowest Cost per Acquisition (CPA)]" optimization goal

If your campaign goal is the lowest cost per acquisition (CPA) and it requires only one success event (such as "Application Submit"), then include that one metric and specify the metric type as *[!UICONTROL Goal]*. The best practice is to set the weight as one (1).

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> A weight of one (1) equates to a value of one (1) for each conversion that's tracked for display ads on any device. For example, if 10 Application Submit conversions are tracked, then 10 Application Submit conversions are reported. If the conversion metric is assigned a weight of 0.5, however, then the 10 conversions are reported as five (5) in Adobe Advertising (10 Conversions * 0.5 [!UICONTROL weight] = 5).

## Custom goals with multiple metrics

There are two scenarios in which you would use multiple metrics in a custom goal:

* Your campaign goal has multiple success events. For example, maybe you're advertising for more than one on-site action (PDF Download, Contact Us, and Email Sign up), and all are actions contribute to your CPA goal. If the objective includes the three separate metrics, each with weights of one (1), then the [!DNL Adobe AI]-powered algorithm treats each of the metrics and user device types with equal importance. If the different metrics have varying costs or importance, then adjust their relative weights accordingly.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* The single conversion metric in your custom goal isn't achieving the minimum of 10 conversions per day required for optimized performance. This can occur because of minimal daily package spend or a limited number of natural conversions. Adding additional supporting metrics to the custom goal can help you achieve the 10-conversions-per-day threshold. Ten supporting events can help a package meet the 10/day threshold, even when each of their weights is below one (1). But you may not need to add that many events.

   When you add supporting metrics to a custom goal, weight them according to their relative importance to the main success event, and keep in mind the quantity of data points. This allows the [!DNL Adobe AI]-powered algorithm to balance multiple metrics and optimize toward your goal.

   The following example objective includes three metrics, each with a different weight: Application Submit = 1, Application Start = 0.1, and Advertiser Landing Page = 0.01. This means that each Application Submit conversion has the same value to your business as an average of 10 Application Start conversions and 100 Advertiser Landing Page conversions.

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

   If, instead, you weighted Landing Page visits equally to Application Submits, then the naturally higher quantity of landing page visits could overwhelm your goal and skew optimization toward landing page visits.

>[!MORELIKETHIS]
>
>* [Manage custom objectives](/help/dsp/admin/custom-objectives-manage.md)
>* [Optimization goals and how to use them](optimization-goals.md)
>* [Package settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP optimizes your campaigns](optimization-how-dsp-optimizes-campaigns.md)
