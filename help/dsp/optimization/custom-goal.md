---
title: Custom Goals
description: Learn about custom goals to define your success events in packages optimized for the lowest CPA or the highest ROAS.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
---
# Custom Goals

Custom goals define the success events that an advertiser requires to meet its business objectives. Each package that uses the optimization goal "[!UICONTROL Highest Return on Ad Spend (ROAS)"] or "[!UICONTROL Lowest Cost per Acquisition (CPA)]" must include a custom goal to help achieve the overall optimization goal. You can create custom goals as *objectives* in [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Each custom goal consists of one or more conversion metrics and the relative weights of those metrics. The available conversion metrics include all metrics tracked using the Adobe Advertising conversion pixel and through Adobe Analytics.

For example, suppose that three conversion metrics are relevant to a specific package in one of your campaigns: "PDF Download" valued at 20 USD, "Email Signup" valued at 30 USD, and "Order Confirmation" valued at 40 USD. If you want to give weight according to the one-time monetary value of the customer action, then the relative weights of the metrics would be 1, 1.5, and 2.

Once you [create a custom goal](#custom-goal-create), you can [assign it to a package](/help/dsp/campaign-management/packages/package-settings.md) for reporting and algorithmic optimization using Adobe Sensei.

## Create a Custom Goal {#custom-goal-create}

To create a custom goal, the DSP account must be linked to a [!DNL Search, Social, & Commerce] account with the same Adobe Experience Cloud organization ID, from within the [!DNL Search, Social, & Commerce] client settings. If your DSP account isn't linked to a [!DNL Search, Social, & Commerce] account, then contact your Adobe Account Team.

1. Log in to [!DNL Advertising Search, Social, & Commerce] at (users in North America) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) or (all other users) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Make sure the metrics that you want to include in your goal have been tracked, are available in the product, and include a display name:

    1. In the main menu, click **[!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions]**.

    1. Locate the metric, and make sure that **[!UICONTROL Show in UI and Reports]** is enabled for the metric.

       >[!NOTE]
       >
       >* [!DNL Analytics] custom events follow this naming convention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Example: `custom_event_16_examplersid`

    1. If the metric doesn't have a value in the **[!UICONTROL Display Name]** column, then click in the cell, enter the display name, and click **[!UICONTROL Apply].**

1. Create the custom goal as an *objective*:

    1. In the main menu, click **[!UICONTROL Search]** > **[!UICONTROL Optimization] > [!UICONTROL New Objectives Beta]**.

    1. In the toolbar, click ![Create](/help/dsp/assets/create-search-ui.png "Create").

    1. Enter the objective settings, including the associated metrics and their relative numeric weights for non-mobile devices and mobile devices, and then save the objective.
    
       At least one metric must have the metric type *[!UICONTROL Goal]*.
       
       >[!NOTE]
       >
       >* [!DNL Analytics] custom events follow this naming convention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Example: `custom_event_16_examplersid`
       >* [!DNL Analytics] dimensions and segments aren't available for Adobe Advertising optimization.

       >[!TIP]
       >
       >For optimum performance, the combined metrics in the custom goal (objective) must total at least ten conversions per day. When they don't, the best practice is to add additional supporting conversion metrics, such as product pages or application starts, to the objective. See [Best Practices for Building a Custom Goal](#custom-goal-best-practices) for guidelines.
       
In the DSP package settings for packages that use the optimization goal "[!UICONTROL Highest Return on Ad Spend (ROAS)"] or "[!UICONTROL Lowest Cost per Acquisition (CPA)]," the objective name is now included in the [!UICONTROL Custom Goals] list. When you select the objective as the custom goal for a package, the [!UICONTROL Conversion Metric] list includes all goal metrics for the objective.

## Best Practices for Building a Custom Goal {#custom-goal-best-practices}

### Custom Goals with a Single Metric

The following examples show how you might configure goals that target a single conversion metric.

#### Example for a Campaign with the "[!UICONTROL Highest Return on Ad Spend (ROAS)]" Optimization Goal

If your campaign goal is revenue ([!UICONTROL Highest Return on Ad Spend (ROAS)]), and revenue from all device types is equally important to you, then include the "[!UICONTROL Revenue]" metric with a non-mobile weight (for conversions from a non-mobile device) of one (1) and a mobile weight (for conversions from a mobile device) of one (1). Select the metric type *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> A mobile weight or non-mobile weight of one (1) equates to a value of one (1) for each $1 of revenue that's tracked.
>
> For example, a $250 conversion with a non-mobile weight of one (1) is reported as $250 for conversions. If the conversion metric is assigned a non-mobile weight of 0.5, then the $250 conversion from a non-mobile device is reported as $125 in Adobe Advertising ($250 Conversion * 0.5 [!UICONTROL Non-mobile Weight] = $125).

#### Example for a Campaign with the "[!UICONTROL Lowest Cost per Acquisition (CPA)]" Optimization Goal

If your campaign goal is the lowest cost per acquisition (CPA) and it requires only one success event (such as "Application Submit"), then include that one metric and specify the metric type as *[!UICONTROL Goal]*. The best practice is to set both the non-mobile weight and the mobile weight as one (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> A mobile weight or non-mobile weight of one (1) equates to a value of one (1) for each conversion that's tracked. For example, if 10 Application Submit conversions are tracked, then 10 Application Submit conversions are reported. If the conversion metric is assigned a non-mobile weight of 0.5, however, then the 10 non-mobile conversions are reported as five (5) in Adobe Advertising (10 Conversions * 0.5 [!UICONTROL Non-mobile Weight] = 5).

### Custom Goals with Multiple Metrics

There are two scenarios in which you would use multiple metrics in a custom goal:

* Your campaign goal has multiple success events. For example, maybe you’re advertising for more than one on-site action (PDF Download, Contact Us, and Email Sign up), and all are actions contribute to your CPA goal. If the objective includes the three separate metrics, each with non-mobile and mobile weights of one (1), then the [!DNL Adobe Sensei] algorithm treats each of the metrics and user device types with equal importance. If the different metrics and device types have varying costs or importance, then you adjust their relative weights accordingly.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* The single conversion metric in your custom goal isn't achieving the minimum of 10 conversions per day required for optimized performance. This can occur because of minimal daily package spend or a limited number of natural conversions. Adding additional supporting metrics to the custom goal can help you achieve the 10-conversions-per-day threshold. Ten supporting events can help a package meet the 10/day threshold, even when each of their weights is below one (1). But you may not need to add that many events.

   When you add supporting metrics to a custom goal, weight them according to their relative importance to the main success event, and keep in mind the quantity of data points. This allows the Adobe Sensei algorithm to balance multiple metrics and optimize toward your goal.

   The following example objective includes three metrics, each with a different non-mobile weight: Application Submit = 1, Application Start = 0.1, and Advertiser Landing Page = 0.01. This means that each Application Submit conversion from non-mobile devices has the same value to your business as an average of 10 Application Start conversions from non-mobile devices and 100 Advertiser Landing Page conversions from non-mobile devices.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

   If, instead, you weighted Landing Page visits equally to Application Submits, then the naturally higher quantity of landing page visits could overwhelm your goal and skew to landing page visits.<!--reword-->

>[!MORELIKETHIS]
>
>* [Optimization Goals and How to Use Them](optimization-goals.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
> * [How DSP Optimizes Your Campaigns](optimization-how-dsp-optimizes-campaigns.md)
