---
title: (New UI) About objectives
description: Learn about objectives to meet your business goals.
feature: Search Objectives, Search Optimization
---
# (New UI) About objectives

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

>[!MORELIKETHIS]
>
>* [Create an objective](objective-create.md)
>* [Edit an objective](objective-edit.md)
>* [Delete an objective](objective-delete.md)
>* [Apply weight recommendations to an objective](objective-apply-weight-recommendations.md)
>* [Objective settings](objective-settings.md)
