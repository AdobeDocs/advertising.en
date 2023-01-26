---
title: Best Practices for Building a Custom Goal
description: Learn the best practices for building custom goals to define your success events.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
---
# Best Practices for Building a Custom Goal

## Custom Goals with a Single Property

The following examples show how you might configure goals that target a single property (metric).

### Example for a Campaign with the "[!UICONTROL Highest ROAS - Custom Goal]" Optimization Goal

If your campaign goal is revenue ([!UICONTROL Highest ROAS - Custom Goal]), then your custom goal (objective) will include the "[!UICONTROL Revenue]" property with a weight of one (1).

![example of a ROAS custom goal with a single property](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] of one equates to a value of one for each $1 of revenue that's tracked.
>
> For example, a $250 conversion with a weight of one is reported as $250. If the conversion metric is assigned a weight of 0.5, then the $250 conversion is reported as $125 in Adobe Advertising ($250 Conversion * 0.5 [!UICONTROL Property Weight] = $125).

### Example for a Campaign with the "[!UICONTROL Lowest CPA - Custom Goal]" Optimization Goal

If your campaign goal is the lowest cost per acquisition (CPA) and it requires only one success event, then you'll include that one metric (in the following example, "Application Submit"). The best practice is to set the weight as one (1).

![example of a CPA custom goal with a single property](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] of one equates to a value of one for each conversion that's tracked.
>
> For example, if 10 Application Submit conversions are tracked, then 10 Application Submit conversions are reported.  If the conversion metric is assigned a weight of 0.5, then the 10 conversions are reported as five (5) in Adobe Advertising (10 Conversions * 0.5 [!UICONTROL Property Weight] = 5).

## Custom Goals with Multiple Properties

There are two scenarios in which you would use multiple properties in a custom goal:

* Your campaign goal has multiple success events. For example, maybe you’re advertising for more than one on-site action, and all are being attributed to your CPA goal. The following example objective includes three separate properties (PDF Download, Contact Us, and Email Sign up), each with a weight of one (1), which tells the [!DNL Adobe Sensei] algorithm that each of the properties has equal importance. If you include properties with varying costs or importance, then you can adjust their relative weights accordingly.

   ![example of a custom goal with multiple properties](/help/dsp/assets/custom-goal-multiple-properties.png)

* The single property in your custom goal isn't achieving the minimum of 10 conversions per day required for optimized performance. This can occur because of minimal daily package spend or a limited number of natural conversions. Adding additional supporting properties to the custom goal can help you achieve the 10-conversions-per-day threshold. Ten supporting events can help a package meet the 10/day threshold, even when each of their weights is below one (1). But you may not need to add that many events.

   When you add supporting properties to a custom goal, weight them according to their relative importance to the main success event, and keep in mind the quantity of data points. This allows the Adobe Sensei algorithm to balance multiple properties and optimize toward your goal.

   The following example objective includes three properties, each with a different weight: Application Submit = 1, Application Start = 0.1, and Advertiser Landing Page = 0.01. This means that each Application Submit conversion has the same value to your business as an average of 10 Application Start conversions and 100 Advertiser Landing Page conversions.

   ![example of a custom goal with multiple properties](/help/dsp/assets/custom-goal-multiple-properties2.png)

   If, instead, you weighted Landing Page visits equally to Application Submits, the naturally higher quantity of landing page visits could overwhelm your goal and skew to landing page visits.<!--reword-->

>[!MORELIKETHIS]
>
>* [About Custom Goals](custom-goal-about.md)
>* [Create a Custom Goal](custom-goal-create.md)
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
