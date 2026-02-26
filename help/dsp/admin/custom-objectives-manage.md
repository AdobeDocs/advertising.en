---
title: Manage custom objectives
description: 
role: User, Admin
feature: DSP Optimization, DSP Packages
---
# Manage custom objectives

*Beta feature*

*Available for DSP accounts that are linked to Search, Social, & Commerce accounts*

Objectives define the success events that an advertiser sets to meet its business objectives, such as to maximize profits or to meet a specific sales target. In DSP, objectives are available as [custom goals](/help/dsp/campaign-management/packages/package-settings.md). Each package that uses the optimization goal "[!UICONTROL Highest Return on Ad Spend (ROAS)"] or "[!UICONTROL Lowest Cost per Acquisition (CPA)]" must include a custom goal to help achieve the overall optimization goal.

An objective consists of the metrics (properties) to be tracked and optimized, and the relative weights of those metrics. For example, suppose that three conversion metrics are relevant to a specific package in one of your campaigns: "PDF Download" valued at 20 USD, "Email Signup" valued at 30 USD, and "Order Confirmation" valued at 40 USD. If you want to give weight according to the one-time monetary value of the customer action, then the relative weights of the metrics would be 1, 1.5, and 2.

The available conversion metrics include all metrics tracked using the Adobe Advertising conversion pixel and through Adobe Analytics.

Each objective can include:

* **[!UICONTROL Goal] metrics**, which represent an advertiser's primary success metrics. They typically include core business outcomes for a package, such as Revenue, Leads, or Sales. Each objective must have at least one goal metric.

* **[!UICONTROL Assist] metrics**, which optionally assist, predict, precede, or contribute to driving goal metrics. Examples include engagement metrics, such as Test Drives and Trials. You can either assign your own weighted assist metrics or let [!DNL Adobe AI] automatically assign and update weighted assist events to maximize your goal events.

All changes to objective options are tracked at the field level and are listed in a change log.

>[!PREREQUISITES]
>
>Before you can create custom goals, the DSP account must be linked to a Search, Social, & Commerce account with the same Adobe Experience Cloud organization ID, even if you aren't a Search, Social, & Commerce customer. If your DSP account isn't linked to a [!DNL Search, Social, & Commerce] account, then contact your Adobe Account Team.

>[!NOTE]
>
>* Advertising Search, Social, & Commerce also uses objectives. Each Search, Social, & Commerce portfolio must have an objective so that the optimization capability can create click and revenue models for the portfolio.
>* You can use the same objective for multiple DSP packages and/or multiple Search, Social, & Commerce portfolios.

<!-- Edit all this and below, including links 

Probably everything in Settings > Conversions is allowed, but verify:

## Available metrics

You can include any of the following in your objectives:

* Metrics that Adobe Advertising tracks using the [Adobe Advertising conversion tracking pixel](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md). **[Do DSP-only clients have these?]**

* (Advertisers with [!DNL Adobe Analytics for Advertising]) [Conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/overview.md).

 -->

## Create an objective

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the upper right, click **[!UICONTROL Create]**.

1. Enter the [objective settings](#custom-objective-settings).

   When you choose automated bidding, you can assign properties (metrics) to the objective as "[!UICONTROL Goal]" metrics. For custom bidding, you can assign properties as either "[!UICONTROL Goal]" or weighted "[!UICONTROL Assist]" metrics, but you must include at least one goal metric.

   <!-- Verify -->The goal and assist labels don't affect optimization. Only the weights of the included metrics affect optimization.

1. In the upper right, click **[!UICONTROL Save]**.

In the [DSP package settings](/help/dsp/campaign-management/packages/package-settings.md) for packages that use the optimization goal "[!UICONTROL Highest Return on Ad Spend (ROAS)"] or "[!UICONTROL Lowest Cost per Acquisition (CPA)]," the objective name is now included in the [!UICONTROL Custom Goals] list. When you select the objective as the custom goal for a package, the [!UICONTROL Conversion Metric] list includes all goal metrics for the objective.

## Edit an objective

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Edit]**.

1. Change any of the [objective settings](#custom-objective-settings).

1. In the upper right, click **[!UICONTROL Save]**.

## View the change log for a custom objective

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Change Log]**.


<!-- Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## Custom objective settings {#custom-objective-settings}

<!-- What is AMOClient? -->

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| Section | Parameter | Description |
|---------|-----------|-------------|
| Basic Details | AMOClient | The advertiser's unique Adobe Advertising ID. |
| Basic Details | Objective Name | The name of the objective.<br><br>All objective names for Advertising DSP must be prefixed the name with "ADSP_" (not case sensitive), such as "ADSP_Registrations." Use a name that is easy to identify when you want to assign it to a package. |
|  | Description | (Optional) A description of the objective. The description appears when you hold the cursor over the name in the Custom Objectives list. If you don't include a description, the objective name is repeated instead. |
| Bidding Strategy |  | The objective's bidding strategy, which determines the types of events that you can configure:<ul><li><b>[!UICONTROL Automated Bidding]:</b> Assign properties (metrics) to the objective as [!DNL goal] metrics. [!DNL Adobe AI] automatically assigns and updates weighted assist events to maximize your goal events.</li><li><b>[!UICONTROL Custom Bidding]:</b> Set up your own bidding strategy by assigning properties as either "[!DNL goal]" or weighted "[!DNL assist]" events.</li></ul> |
| Properties | [!UICONTROL Available Metrics] | All metrics tracked for the advertiser. To add a metric as a goal, click <b>[!UICONTROL Goal]</b> next to the metric name. ([!UICONTROL Custom Bidding] only) To add a metric that assists the assigned goal metrics, click <b>[!UICONTROL Assist]</b> next to the metric name.<br><br><b>Notes:</b> [!DNL Analytics] custom events follow this naming convention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Example: `custom_event_16_examplersid.` [!DNL Analytics] dimensions and segments aren't available for Adobe Advertising optimization.<br><br><b>Tip:</b> For optimum performance, the combined metrics in the custom goal (objective) must total at least ten conversions per day. When they don't, the best practice is to add additional supporting conversion metrics, such as product pages or application starts, to the objective. See [Best Practices for Building a Custom Goal](#custom-goal-best-practices) for guidelines. |
|  | Selected Metrics | The name of each conversion metric included in the objective. Do any of the following:<ul><li>To add a metric as a goal, click <b>[!UICONTROL Goal]</b> next to the metric name in the [!UICONTROL Available Metrics] column.</li><li>([!UICONTROL Custom Bidding] strategy only) To add a metric that assists the assigned goal metrics, click <b>[!UICONTROL Assist]</b> next to the metric name in the [!UICONTROL Available Metrics] column. Then enter the numeric weight of the metric relative to other metrics in the objective. The weight must be greater than zero (0) and may include decimals. The default weight is 1.</li><li>([!UICONTROL Custom Bidding] strategy only) To edit the weight of an assist metric, click inside the field and enter the numeric weight of the metric relative to other metrics in the objective. The weight must be greater than zero (0) and may include decimals. The default weight is 1.</li><li>To remove a metric from the objective, hold the cursor over the metric name and click **[!UICONTROL X]**./li></ul>**Notes:**<ul><li>Make sure that the different metrics and their weights make sense relatively. For example, you can't directly compare a count with a dollar amount.</li><li>Large relative changes between the objective weights can cause temporary volatility in performance, so monitor performance after the change.</li></ul>. |

>[!MORELIKETHIS]
>
>* [Optimization Goals and How to Use Them](/help/dsp/optimization/optimization-goals.md)
>* [Best Practices for Custom Goals](/help/dsp/optimization/custom-goal.md)
>* [Package Settings](/help/dsp/campaign-management/packages/package-settings.md)
>* [Manage Conversions](/help/dsp/admin/conversion-metrics-manage.md)
