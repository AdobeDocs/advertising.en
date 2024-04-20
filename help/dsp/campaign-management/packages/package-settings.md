---
title: Package Settings
description: See descriptions of the available package settings.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
---
# Package Settings

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** The package name. The maximum length is 60 characters.

**[!UICONTROL Description]:** (Optional) A description of the package.

**[!UICONTROL 3rd Party Billed Fees]:** (Optional) A static third-party fee to be tracked as a non-billable cost:

>[!NOTE]
>
>Billable fees are reflected in the [!UICONTROL Net CPM] metric.
>
* **[!UICONTROL CPM]:** The cost per 1000 impressions (CPM).

* **[!UICONTROL CPM Description]:** A description of the CPM fee.

You can override the package-level setting at the [placement level](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Read-only for existing packages) At which level to pace and cap placements in the package:

* **[!UICONTROL Package level pacing]:** This pacing strategy operates by pacing and capping all included placements as a *group*. This strategy ensures that all placements within a given package are optimized holistically, distributing spend based on performance and scale to selected key performance indicators (KPIs).

* **[!UICONTROL Placement level pacing]:**  This pacing strategy operates by pacing and capping all included placements *individually*. The best practice is to use this strategy only to execute guaranteed private marketplace deals.

**[!UICONTROL Flight Dates]:** The package's start date and end date.

To optionally create non-even pacing flights for the package, select *[!UICONTROL *Activate Custom Flighting]** and set up the custom flights in the [!UICONTROL Flighting] section below. Once you enable custom flighting and save the package, you can't disable custom flighting.

>[!NOTE]
>
>* The flight dates must be included within the campaign flight dates. In addition, the flight dates for all placements that are assigned to this package must be included within these dates.
> * You can't edit the package start date when custom flighting is activated.

**[!UICONTROL Budget]:** (Packages with package-level pacing only) The gross budget cap and the budget interval.

For packages with custom flighting, the budget interval is always *[!UICONTROL All time]*. For packages without custom flighting, specify the budget interval: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* or *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Packages with package-level pacing and dynamic margin management only) The gross budget cap for the duration of the package.

**[!UICONTROL Optimization Goal]:** (Packages with package-level pacing only) The optimization goal for the package. See descriptions of each optimization goal at [Optimization Goals and How to Use Them](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. The custom goal can optionally include additional weighted upper-funnel events (such as page visits and shopping cart additions) to be used in addition to the CPA or ROAS metric for package optimization. For more information about the best practices for custom goals and campaigns that use them, see [Best Practices for Building a Custom Goal](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) and [Best Practices for Setting up Performance Campaigns](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) Tells the optimization model to learn only from click-based conversions. Otherwise, the optimization model learns from both click- and impression-based conversions.

**[!UICONTROL Conversion Metric]:** (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event (such as signups) or revenue event/sale amount (such as purchases and purchase values) to use for computing the return on ad spend or the cost per acquisition. Select from a list of all primary events ("goal metrics") mapped to the selected custom goal. If the list is empty, then edit the custom goal to include at least one of the underlying events as a goal metric. 

**[!UICONTROL Package Goal Type]:** (Packages with custom optimization goals only) The purpose of the package. This setting helps determine how to optimize the package:

* *[!UICONTROL Prospecting]:* Prospecting packages focus on acquiring new customers.

* *[!UICONTROL Retargeting]:* Retargeting packages focus on re-exposing prior visitors or customers.

* *[!UICONTROL Other]:* All other purposes.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package.

**[!UICONTROL Target]:** (Packages with package-level pacing only) The target goal, which is used to track performance.

>[!NOTE]
>
>This field is only a benchmark and isn't used for decisioning.

**[!UICONTROL Frequency Cap]:** (Packages with package-level pacing only) The number of times a unique device or person (depending on the specified [!UICONTROL Cross Device Level] for the campaign) can be served ads from the package. Options include *[!UICONTROL Unlimited]* or a specific amount per day, week, or month.

>[!NOTE]
>
>* You can set frequency caps at the campaign, package, and placement levels. DSP respects the strictest frequency cap in the campaign hierarchy.
>* The best practice is to set frequency caps for both prospecting and retargeting at the package level.
> * Higher frequency caps result in higher spend and impressions but lower reach. Lower frequency caps result in lower spend and impressions but higher reach.

**[!UICONTROL Pace on]:** (Packages with package-level pacing only) What pacing is based on:

* *[!UICONTROL Budget]:* (Default) This option delivers as many impressions as possible within the allocated package budget.

* *[!UICONTROL Impressions]:* This option delivers impressions until a specified quantity is reached within a specified interval. When you select this option, specify the number of impressions and the interval: *All time,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* or *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Packages with package-level pacing only) How to pace ad delivery across the entire flight:

* *[!UICONTROL Even]:* Paces delivery uniformly throughout each flight, with a target of 50% of the delivery in the first half of the flight.

* *[!UICONTROL Slightly Ahead]:* (The default) Accelerates delivery so that it's 55-65% complete halfway through the flight duration.

* *[!UICONTROL Frontload]:* Accelerates delivery so that it's 65-75% complete halfway through the flight.

* *[!UICONTROL Aggressive Frontload]:* Accelerates delivery so that it's 75-85% complete halfway through the flight.

**[!UICONTROL Intraday pacing]:** (Packages with package-level pacing only) How to pace ad delivery across each day within the flight:

* *[!UICONTROL Even]:* (The default) Scales delivery based on inventory availability. Generally, more ads are delivered per hour in the daytime, when auction volume is higher, and fewer ads are delivered in the mornings and evenings.

* *[!UICONTROL ASAP]:* Accelerates delivery to twice the speed of *Even*. 

   >[!CAUTION]
   >
   >This option can negatively affect performance. Use it only when you are fully prioritizing delivery and spend over performance optimization.

## [!UICONTROL Flighting]

(Packages with package-level pacing and with "[!UICONTROL Activate Custom Flighting]" enabled) Custom flight periods within the overall [!UICONTROL Flight Dates] specified in the [!UICONTROL Goals & Budget] section.

For each flight, enter the start date, end date, and the target number of impressions. To add another flight, click **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [About Package Management](package-about.md)
>* [Create a Package](package-create.md)
>* [Edit a Package](package-edit.md)
>* [Attach a Placement to a Package](package-attach-placement.md)
>* [View the Change Log for a Package](package-change-log.md)
>* [FAQs About Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
