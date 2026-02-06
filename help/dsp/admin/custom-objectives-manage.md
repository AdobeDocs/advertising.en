---
title: Manage custom objectives
description: 
role: User, Admin
---
# Manage custom objectives

*Beta feature*

Objectives are goals that an advertiser sets to meet its business objectives, such as to maximize profits or to meet a specific sales target. Both Advertising Search, Social, & Commerce and Advertising DSP use objectives:

* Each Search, Social, & Commerce portfolio must have an objective so that the optimization capability can create click and revenue models for the portfolio.

* In DSP, objectives appear as custom goals for DSP accounts that are linked to Search, Social, & Commerce accounts. Each package that uses the optimization goals "Highest Return on Ad Spend (ROAS)" or "Lowest Cost per Acquisition (CPA)" must include a custom goal that helps achieve the overall optimization goal.

An objective consists of the conversion metrics to be tracked and optimized, and the relative weights of those metrics. For example, suppose that an online magazine with two online subscription levels and one print subscription level and the objective "maximize profits" has three metrics: "basic online subscriptions" valued at 20 USD, "premium online subscriptions" valued at 40 USD, and "print subscriptions" valued at 30 USD. If the magazine wants to give weight according to the one-time monetary value of the subscription, then the relative weights of the metrics would be 1, 2, and 1.5, respectively.

For each metric in the objective, you can:

* Configure separate weights for conversions from mobile devices.

* Label the metric as a [!UICONTROL Goal] metric or an [!UICONTROL Assist] metric.

* Apply weight recommendations to the metrics.

>[!NOTE]
>* (Search, Social, & Commerce) You can associate an objective with a portfolio when you [create the portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) or by later [modifying the portfolio settings](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md).
>* (Advertisers with DSP accounts that are linked to Search, Social, & Commerce accounts) In Advertising DSP, you can select an objective as a [custom optimization goal](/help/dsp/campaign-management/packages/package-settings.md) for a package with package-level pacing.
>* You can use the same objective for multiple Search, Social, & Commerce portfolios and/or multiple DSP packages.
>* The metrics for each objective in the [!UICONTROL Objectives] view don't include data from DSP.

## Available metrics

You can include any of the following in your objectives:

* Metrics that Adobe Advertising tracks using the [Adobe Advertising conversion tracking pixel](/help/search-social-commerce/tracking/conversion-tracking-advertising.md).

* [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* (Advertisers with [!DNL Adobe Analytics for Advertising]) [Conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/overview.md).

  In Search, Social, & Commerce, the following [site engagement metrics](/help/integrations/analytics/analytics-data-in-advertising.md) are automatically factored into the portfolio bidding algorithms: `timespent_secs_1stvisit`, `timespent_secs_total`, `pageviews_1stvisit`, `pageviews_total`, and `bounces`.

* [!DNL Google] metrics:<!-- Search only, or might DSP-only clients also have these? -->

  * [[!DNL Google Ads]-tracked conversions](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) from synced [!DNL Google Ads] accounts.

  * (Advertisers with [[!DNL Google Analytics] integrations](/help/search-social-commerce/admin/data-sources/data-source-about.md)) Page views, Sessions, Bounce Rate (calculated as bounces/sessions), and Session Duration.

    In Search, Social, & Commerce, these metrics are automatically factored into the portfolio bidding algorithms.
 
## Option to upload objectives to the ad networks

You can optionally [upload the objectives for the account's portfolios to [!DNL Google Ads] and/or [!DNL Microsoft Advertising] as conversions](/help/search-social-commerce/tools/objective-upload-to-networks.md) so that you can use them for campaign- or ad group-level optimization. When you enable the option, Search, Social, & Commerce passes the weighted revenue data at the EF ID (click ID) level to the ad network daily. It omits any ad network-tracked metrics.

## Create an objective

>[!NOTE]
>
>You can associate an objective with a portfolio when you [create the portfolio](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md) or by later [modifying the portfolio settings](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md). You can use the same objective for multiple portfolios.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Objectives]**.

1. In the upper right, click **[!UICONTROL Create Objective]** or ![Add](/help/search-social-commerce/assets/add-new.png "Add").

   The button shown depends on your browser width. 

1. Enter the objective settings.

  For instructions, see the help within the user interface or in the Optimization Guide, which is available from within Search, Social, & Commerce.

1. At the bottom of the settings, click **[!UICONTROL Save]**.

Objectives prefixed with "`ADSP_`" (not case-sensitive) for use with Advertising DSP packages are available as custom goals within DSP within two days.

## Edit an objective

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Objectives]**.

1. Select the check box next to the objective. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit") **[!UICONTROL Edit]**.

1. Change any of the objective settings.

   For instructions, see the help within the user interface or in the Optimization Guide, which is available from within Search, Social, & Commerce.

1. Save the data:

   * To save the objective, click **[!UICONTROL Save]**.
   
   * To create a new objective with the specified settings, click **[!UICONTROL Save As]**, enter the name of the new objective, and then click **[!UICONTROL Save]**.

## Delete an objective

You can delete an objective that's not assigned to a portfolio.

1. In the main menu, click **[!UICONTROL Goals] > [!UICONTROL Objectives]**.

1. Select the check box next to the objective. In the toolbar above the data table, click ![Delete](/help/search-social-commerce/assets/delete-new.png "Delete") **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

## Apply weight recommendations to an objective

For instructions, see the help within the user interface or in the Optimization Guide, which is available from within Search, Social, & Commerce.

## Custom objective settings

<!-- What is AMOClient? -->

| Section | Parameter | Description |
|---------|-----------|-------------|
| Basic Details | AMOClient | The advertiser's unique Adobe Advertising ID. |
| Basic Details | Objective Name | The name of the objective.<br><br>All objective names for [Advertising DSP](/help/dsp/home.md) must be prefixed the name with "ADSP_" (not case sensitive), such as "ADSP_Registrations." Use a name that will be easy to identify when you want to assign it to a package. |
|  | Description | (Optional) A description of the objective. The description will appear as a tooltip when you hold the cursor over the name in the Custom Objectives list. |

|  | Bidding Strategy |  |


| Available Metrics | Include hidden metrics | List all metrics tracked for the advertiser, including [conversion metrics that are excluded in management views and reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md), in the Available Metrics list. By default, the list includes only the [conversion metrics that can be shown in management views and reports](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) for the advertiser. |
| Your Objective | Metric | The name of each conversion metric included in the objective. To add a conversion metric to the objective, move it from the [!UICONTROL Available Metrics] list to here either a) by dragging and dropping it or b) by selecting it and then clicking [!UICONTROL >].<br><br>"Clicks" is already added to indicate how heavily to weight clicks relative to the conversion metrics specified for the objective. For optimization, clicks are considered another conversion metric for the objective. This allows you to give as much or as little importance as you want to past clicks during optimization. The default click value is *0.0001*. For example, when the weight of a metric is *1*, then a click value of *0.0001* means that each click is worth 1/10000th of a conversion for that metric. If another metric in the objective has a weight of *2*, then each click is worth 1/20000th of a conversion. This field is editable only by some roles. Contact your Adobe Account Team if you have questions about this value.<br><br>* (Advertisers with an [Adobe Advertising](/help/search-social-commerce/introduction/about.md)-[Adobe](/help/search-social-commerce/introduction/about.md) [Analytics](/help/search-social-commerce/admin/data-sources/data-source-about.md) integration) The following metrics from [Analytics](/help/search-social-commerce/admin/data-sources/data-source-about.md) are automatically factored into the portfolio bidding algorithms and generally shouldn't be added to the objective: [timespent_secs_1stvisit](/help/search-social-commerce/definitions/def-analytics-metric-pageviews-firstvisit.md), [timespent_secs_total](/help/search-social-commerce/definitions/def-analytics-metric-timespent-secs-total.md), [pageviews_1stvisit](/help/search-social-commerce/definitions/def-analytics-metric-pageviews-firstvisit.md), [pageviews_total](/help/search-social-commerce/definitions/def-analytics-metric-pageviews-total.md), and [bounces](/help/search-social-commerce/definitions/def-analytics-metric-bounces.md). If you want to add any of these metrics to the objective for more control over how they're are factored in, consult your Adobe Account Team to determine how to weight them to meet your goals.<br><br>* For objectives used for [Advertising DSP](/help/dsp/home.md) packages, include only metrics that are attributed to DSP. Any metrics attributed to [Search, Social, & Commerce](/help/search-social-commerce/home.md) or to any other ad network are ignored.<br><br>* For objectives to use with campaign- or ad group-level optimization (hybrid portfolios):<br><br>  * The best practice is to match the metrics in the objective with the metrics used for the conversion goals or conversion actions for the campaigns that use the objective. Using additional conversion goals may impact portfolio performance. Manually set each campaign's conversion goals or conversion actions within the ad network's editor.<br><br>  * For portfolios that include only Google Ads or Microsoft Advertising campaigns, you can optimize to conversions tracked by the ad network, which are automatically synced to Search, Social, & Commerce. The portfolio objective must include only the ad network-tracked conversions, each with a weight of "1."<br><br>  * When you [upload your Search, Social, & Commerce objectives to the ad network](/help/search-social-commerce/tools/objective-upload-to-networks.md), include metrics from offline feed data only if the advertiser is sending a feed daily at a consistent time and with a transaction/conversion timestamp. Irregular or delayed feed metrics can cause issues in the upload.<br><br>  * When you [upload your Search, Social, & Commerce objectives to the ad network](/help/search-social-commerce/tools/objective-upload-to-networks.md) and the campaign goals include ad network-tracked conversions, then add the ad network-tracked conversions within the ad network's editor instead of within the objective settings. Ad network-tracked conversions aren't re-uploaded to the ad network with the objective. In addition, within the ad network's editor, add the uploaded portfolio objective metric (which begins with "O_ACS_OBJ") as a conversion goal or action for the relevant campaigns in either of the following ways:<br><br>    * (When most campaigns in the account will be optimized to Search, Social, & Commerce portfolio objectives) For Google Ads accounts, make the uploaded portfolio objective metric (which begins with "O_ACS_OBJ") the primary conversion action for the account, and switch all of the campaign's ad network-tracked conversion metrics to secondary conversion actions. For Microsoft Advertising accounts, set the uploaded portfolio objective metric (which begins with "O_ACS_OBJ") to "Include in "Conversions"="Yes," and set all of the campaign's ad network-tracked conversion metrics to "No."<br><br>    * Create a custom campaign-level goal for each portfolio objective metric (which begins with "O_ACS_OBJ"), and assign the goal to campaigns in the portfolio. |
|  | Type | Designate all of your metrics as either goal metrics or assist metrics. When you include at least one goal metric and one assist metric, the optimization capability generates a weight recommendation for each assist metric based on its contribution to the primary goal metrics.<br><br>* [!UICONTROL Goal] — Goals represent an advertiser's primary success metrics. They typically include core business outcomes for a portfolio, such as Revenue, Subscriptions, Leads, or Sales.<br><br>* [!UICONTROL Assist] — Use for metrics that assist, predict, precede, or contribute to driving goal metrics. Examples include engagement metrics such as Page Scroll Depth, Demo Registrations, Test Drives, and Trials.<br><br>**Note:** The goal and assist labels don't affect optimization. Only the weights and non-mobile weights of the included metrics affect optimization. |


|  | \[Weight\] | The numeric weight of the metric relative to other metrics in the objective. This value is used for ads on all relevant device types. The weight must be greater than zero (0) and may include decimals. The default weight is 1.**Notes:**<ul><li>Make sure that the different mobile weights make sense relatively. For example, you can't directly compare a count with a dollar amount.</li><li>Large relative changes between the objective weights can cause temporary volatility in performance, so monitor performance after the change.</li></ul>. |


