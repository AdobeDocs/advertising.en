---
title: Expected Data Variances Between [!DNL Analytics] and Adobe Advertising
description: Expected Data Variances Between [!DNL Analytics] and Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
---
# Expected Data Variances Between [!DNL Analytics] and Adobe Advertising

*Advertisers with an Adobe Advertising-Adobe Analytics Integration Only*

Advertisers with the [!DNL Analytics for Advertising] <!-- (A4AdC) --> integration track paid advertising through Adobe Advertising and Adobe Analytics. When you track media, campaigns, and channels via multiple systems, the same data sets from different systems rarely match completely. This document explains how you should expect data for media that's trafficked through Adobe Advertising to compare to data in the different systems in which the media is tracked within [!DNL Analytics].

>[!NOTE]
>
>This document is focused on Adobe Advertising and Analytics, but many of the key points are also transferable to other tracking solutions.

## Attribution Differences in Similar Reports

### Potentially Different Lookback Windows and Attribution Models

The [!DNL Analytics for Advertising] integration uses two variables ([!DNL eVars] or [!DNL rVars] \[reserved [!DNL eVars]]\) to capture the [EF ID and AMO ID](ids.md). These variables are configured with a single lookback window (the time within which click-throughs and view-throughs are attributed) and an attribution model. Unless otherwise specified, the variables are configured to match the default, advertiser-level click lookback window and attribution model in Adobe Advertising.

However, lookback windows and attribution models are configurable in both Analytics (via the [!DNL eVars]) and in Adobe Advertising. Further, in Adobe Advertising, the attribution model is configurable not only at the advertiser level (for bid optimization) but also within individual data views and reports (for reporting purposes only). For example, an organization may prefer to use the even distribution attribution model for optimization but use last touch attribution for reports in Advertising DSP or [!DNL Advertising Search, Social, & Commerce]. Changing attribution models changes the number of attributed conversions.

If a reporting lookback window or attribution model is modified in one product and not in the other, then the same reports from each system show distinct data:

* **Example of discrepancies caused by different lookback windows:**

     Suppose Adobe Advertising has a 60-day click lookback window and [!DNL Analytics] has a 30-day lookback window. And suppose that a user comes to the site through an Adobe Advertising-tracked ad, leaves, and then returns on day 45 and converts. Adobe Advertising attributes the conversion to the initial visit because the conversion occurred within the 60-day lookback window. [!DNL Analytics], however, can't attribute the conversion to the initial visit because the conversion occurred after the 30-day lookback window had expired. In this example, Adobe Advertising reports a higher number of conversions than [!DNL Analytics] does.

     ![Example of a conversion attributed in Adobe Advertising but not [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Example of discrepancies caused by different attribution models:**

     Suppose a user interacts with three different Adobe Advertising ads before converting, with revenue as the conversion type. If an Adobe Advertising report uses an even distribution model for attribution, then it attributes the revenue evenly across all ads. If [!DNL Analytics] uses the last touch attribution model, however, then it attributes the revenue to the last ad. In the following example, Adobe Advertising attributes an even 10 USD of the 30 USD of revenue captured to each of the three ads, whereas [!DNL Analytics] attributes all 30 USD of revenue to the last ad seen by the user. When you compare reports from Adobe Advertising and [!DNL Analytics], you can expect to see the impact of the difference in attribution.

     ![Different revenue attributed to Adobe Advertising and [!DNL Analytics] based on different attribution models](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>The best practice is to use the same lookback windows and attribution model in both Adobe Advertising and [!DNL Analytics]. Work with your Adobe Account Team as necessary to identify the current settings and to keep the configurations in sync.

These same concepts apply to any other like channels that use different lookback windows or attribution models.

#### Different Lookback Windows for View-Through Tracking {#impression-lookback}

In Adobe Advertising, attribution is based on clicks and impressions, and you can configure different lookback windows for clicks and for impressions. In [!DNL Analytics], however, attribution is based on click-throughs and view-throughs, and you don't have the option to set different attribution windows for click-throughs and view-throughs; tracking for each starts at the initial site visit. An impression can occur the same day or multiple days before a view-through occurs, and this can impact where the attribution window starts in each system.

Typically, the majority of view-through conversions occur quickly enough that both systems attribute credit. However, some conversions may occur outside the Adobe Advertising impression lookback window but within the [!DNL Analytics] lookback window; such conversions are attributed to the view-through in [!DNL Analytics] but not to the impression in Adobe Advertising.

In the following example, suppose a visitor was served an ad on Day 1, performed a view-through visit (that is, visited the ad's landing page without previously clicking the ad) on Day 2, and converted on Day 45. In this case, Adobe Advertising would track the user from Days 1-14 (using a 14-day lookback), [!DNL Analytics] would track the user from Days 2-61 (using a 60-day lookback), and the conversion on Day 45 would be attributed to the ad within [!DNL Analytics] but not within Adobe Advertising.

![Example of a view-through conversion attributed in [!DNL Analytics] but not Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

A further cause of discrepancies is that, in Adobe Advertising, you can assign view-through conversions a custom *view-through weight* that is relative to the weight attributed to a click-based conversion. The default view-through weight is 40%, which means that a view-through conversion is counted as 40% of the value of a click-based conversion. [!DNL Analytics] provides no such weighting of view-through conversions. So, for example, a 100 USD revenue order captured in [!DNL Analytics] is discounted to 40 USD in Adobe Advertising if you're using the default view-through weight &mdash; a difference of 60 USD.

Consider these differences when comparing view-through conversions between Adobe Advertising and [!DNL Analytics] reports.

#### Available Attribution Models

| Adobe Advertising Attribution | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] Allocation |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Don't Use* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>For linear allocation, [!DNL Analytics] attributes success events equally across all [!DNL eVar] values within a single visit, so use linear allocation with an [!DNL eVar] expiration of "Visit." For advertising, however, the use of linear attribution leads to allocation that is not truly linear and to less-than-ideal reporting. For example, if a visitor interacts with three ads before converting in three separate visits, only the ad seen in the last visit is attributed to the conversion, not all three ads.
>
>In addition, switching conversion allocation to or from "Linear" prevents historical data from displaying, which can can lead to misstated data in reports. For example, linear allocation might divide revenue across a number of different [!DNL eVar] values. If you change allocation to "Most Recent," then 100% of that revenue becomes associated with the most recent single value. This association can lead you to incorrect conclusions.
>
>To prevent confusion, [!DNL Analytics] makes historical data unavailable in the reporting interface. You can view the historical data if you change the [!DNL eVar] back to the initial allocation setting, although you should not change [!DNL eVar] allocation settings simply to access historical data. Adobe recommends using a new [!DNL eVar] when you want to apply a new allocation setting for data that's already being recorded, rather than changing allocation settings for an [!DNL eVar] that already has a significant amount of historical data.

See a list of [!DNL Analytics] attribution models and their definitions at [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

If you're logged into [!DNL Search, Social, & Commerce], you can find a list 

* (Users in North America) [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* (All other users) [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Event Date Attribution in Adobe Advertising

In Adobe Advertising, you can report conversion data either by the associated click date/event date (the date of the click or impression event) or by the transaction date (conversion date). The concept of click/event date reporting doesn't exist in [!DNL Analytics]; all conversions tracked in [!DNL Analytics] are reported by transaction date. As a result, the same conversion may be reported with different dates in Adobe Advertising and [!DNL Analytics]. For example, consider a user who clicks an ad on January 1 and converts on January 5. If you're viewing the conversion data by event date in Adobe Advertising, then the conversion is reported on January 1, when the click occurred. In [!DNL Analytics], the same conversion is reported on January 5.

![Example of a conversion attributed to different dates](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] reporting](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) allows you to configure rules to identify different marketing channels based on distinct aspects of hit information. You can track Adobe Advertising-tracked channels ([!UICONTROL Display Click Through], [!UICONTROL Display View Through], and [!UICONTROL Paid Search]) as [!DNL Marketing Channels] by using the `ef_id` query string parameter to identify the channel. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> However, even though the [!DNL Marketing Channels] reports can track Adobe Advertising channels, the data may not match the Adobe Advertising reports for several reasons. See the following sections for more information.

>[!NOTE]
>
> The following core concepts also apply to any multi-channel tracking that involves campaigns not tracked in Adobe Advertising, such as the [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) variable (also known as the "Tracking code" dimension or "[!DNL eVar] 0") and custom [!DNL eVar] tracking.

### Potentially Different Attribution Models in [!DNL Marketing Channels]

Most [!DNL Marketing Channels] reports are configured with [!UICONTROL Last Touch] attribution, for which the last marketing channel detected is assigned 100% of the conversion value. Using different attribution models for the [!DNL Marketing Channels] reports and Adobe Advertising reports leads to discrepancies in attributed conversions.

### A Potentially Different Lookback Window in [!DNL Marketing Channels]

The lookback window for [!DNL Marketing Channels] can be customized. In Adobe Advertising, the click lookback window is configurable, although a fixed 60-day window is common. If the two products use different lookback windows, you can expect data discrepancies.

### Different Channel Attribution in [!DNL Marketing Channels]

Adobe Advertising reports capture only paid media trafficked through Adobe Advertising (paid search for [!DNL Advertising Search, Social, & Commerce] ads, and display for Advertising DSP ads), whereas [!DNL Marketing Channels] reports can track all digital channels. This can lead to a discrepancy in the channel for which a conversion is attributed.

For example, paid search and natural search channels often have a symbiotic relationship, in which each channel assists the other. The [!DNL Marketing Channels] report attributes some conversions to natural search that Adobe Advertising doesn't because it doesn't track natural search.

Consider also a customer who views a display ad, clicks a paid search ad, clicks inside an email message, and then places a 30 USD order. Even if Adobe Advertising and [!DNL Marketing Channels] both use the last touch attribution model, the conversion would still be attributed differently to each. Adobe Advertising doesn't have access to the [!UICONTROL Email] channel, so it would credit paid search for the conversion. [!DNL Marketing Channels], however, has access to all three channels, so it would credit [!UICONTROL Email] for the conversion.

![Example of different conversion attribution in Adobe Advertising versus [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

For more explanation of why the metrics may vary, see "[Why Channel Data Can Vary Between Adobe Advertising and [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)."

## Data Differences in Adobe Analytics [!DNL Paid Search Detection]

The [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) feature in [!DNL Analytics] allows companies to [define rules to track paid and organic search traffic](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) for specified search engines. The [!DNL Paid Search Detection] rules use both a query string and the referring domain to identify paid and natural search traffic. The [!DNL Paid Search Detection] reports are part of the larger group of [Finding Methods](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) reports, which expire either when a specified event (such as a Cart Checkout) occurs or the visit ends.

The following is the interface for creating a [!DNL Paid Search Detection] rule set:

![Example of a Paid Search Detection rule set in [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

The resulting [!DNL Paid Search Detection] reports include the [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine], and [!UICONTROL Natural Search Keywords] reports.

Note the following two limitations with data in [!DNL Paid Search Detection] reports:

* The [!UICONTROL Paid Search Keywords] and [!UICONTROL Natural Search Keywords] reports show the search queries as identified by the referring URLs, not the keywords on which users bid. Adobe Advertising and [!DNL Analytics] reports show the actual keywords, so don't expect them to align with the [!DNL Paid Search Detection] keyword reports.

* When the [!DNL Paid Search Detection] feature was originally created, the originating search query (the string of characters the user entered into the search bar in the search engine) was more readily available to advertisers via the referring URL. Today, search engines largely obfuscate the search query, and the [!DNL Paid Search Detection] keyword reports are of limited value because most query data falls under "unspecified."

     With [!DNL Analytics for Advertising], advertisers can still track paid keywords in [!DNL Analytics]. The referring domain informs the engine reports which search engine drove the traffic. Since the advertiser-specific account information isn’t tied to the referring domain, all traffic is listed under the search engine. Advertisers with multiple accounts in the same search engine should refer to Adobe Advertising or [!DNL Analytics] reporting for account-specific reporting.

### Why Configure [!DNL Paid Search Detection]?

The [!DNL Paid Search Detection] reports allow you to identify natural search traffic in the [[!DNL Analytics Marketing Channels] reports](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). Separating paid search traffic versus natural search traffic is a great way to understand the value that natural search brings to the full marketing ecosystem.

## Click-Through Data Validation for [!DNL Analytics for Advertising] {#data-validation}

For your integration, you should validate your click-through data to make sure that all pages on your site are properly tracking click-throughs.

In [!DNL Analytics], one of the easiest ways to validate [!DNL Analytics for Advertising] tracking is to compare clicks to instances using a "Clicks to [!UICONTROL AMO ID Instances]" calculated metric, which is calculated as follows:

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] represents the number of times that [AMO IDs](ids.md) are tracked on the site. Each time an ad is clicked, an AMO ID (`s_kwcid`) parameter is added to the landing page URL. The number of [!UICONTROL AMO ID Instances], therefore, is analogous to the number of clicks and can be validated against actual ad clicks. We typically see an 85% match rate for [!DNL Search, Social, & Commerce] and a 30% match rate for [!DNL DSP] traffic (when filtered to include only click-through [!UICONTROL AMO ID Instances]). The difference in expectations between search and display can be explained by the expected traffic behavior. Search captures intent, and, as such, users usually intend to click on the search results from their query. Users who see a display or online video ad, however, are more likely to click the ad unintentionally and then either bounce from the site or abandon the new window that loads before the page activity is tracked.

In Adobe Advertising reports, you can similarly compare clicks to instances using the "[!UICONTROL ef_id_instances]" metric instead of [!UICONTROL AMO ID Instances]:

```
Clicks to EF ID Instances = (ef_id_instances / Clicks)
```

While you should expect a high match rate between the AMO ID and the EF ID, don't expect 100% parity because AMO ID and EF ID fundamentally track different data, and this difference can lead to slight differences in the total [!UICONTROL AMO ID Instances] and [!UICONTROL EF ID Instances]. If the total [!UICONTROL AMO ID Instances] in [!DNL Analytics] differ from [!UICONTROL EF ID Instances] in Adobe Advertising by more than 1%, however, contact your Adobe Account Team for assistance.

For more information about the AMO ID and EF ID, see [Adobe Advertising IDs Used by Analytics](ids.md).

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

### Troubleshooting Disparities Between Clicks and Instances

<!-- The example above is for for clicks-to-instances, but this talks about instances-to-clicks. Which is more relevant? Can we make these both the same; if so, what are the valid %s to mention? -->
**Question: The example above is for for clicks-to-instances, but this talks about instances-to-clicks. Which is more relevant? Can we make these both reference the same ratio; if so, what are the valid %s to mention in each place?**

If the instances-to-clicks ratio is below 85%, check the following:

* Are you missing click tracking for the account or at any sublevel, or do you have duplicate click tracking (for example, at both the account and campaign levels)?

  In Search, Social, & Commerce, [download a bulksheet](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) for the account to check the tracking URLs.

  Also, in [!DNL Analytics], you can see if the EF IF and AMO ID are appended consistently using a "[!DNL s_kwcid] to [!DNL ef-id]" calculated metric, which is calculated as follows: **Question: Are these metrics actually called AMO ID and EF ID or s_kwcid and ef-id in Analytics?**
  
  ```
  [!DNL s_kwcid] to [!DNL ef-id] = ([!UICONTROL s_kwcid] / ef-id)
  ```
  <!-- Are these metrics actually called AMO ID and EF ID or s_kwcid and ef-id in Analytics? -->

  A value greater that 100% indicates that more EF IDs are missing than AMO IDs.

* Does the landing page have a loading problem so that the AMO ID and EF ID (s_kwcid) aren't captured?

* Is the landing page URL redirected so that the AMO ID and EF ID are lost?

* Do all landing pages use the configured report suite?

>[!NOTE]
>
>In theory, it's possible that one instance has multiple clicks. Make sure to check for clicks on different devices (such as desktop, mobile, and tablet).

## Comparing Data Sets in [!DNL Analytics for Advertising] Versus in Adobe Advertising

The [AMO ID](ids.md) (s_kwcid query string parameter) is used for reporting in [!DNL Analytics], and the [EF ID](ids.md) is used for reporting in Adobe Advertising. Because they're distinct values, it's possible for one value to be corrupted or not added to the landing page.

For example, suppose we have the following landing page:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

where the EF ID is "`test_ef_id`" and the AMO ID is "`test_amo_id`."

If a site-side redirect occurs, then the URL could end up like this:

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

where the EF ID is "`test_ef_id`" and the AMO ID is "`test_amo_id#redirectAnchorTag`."

In this example, the addition of the anchor tag adds unexpected characters to the AMO ID, resulting in a value that Analytics doesn't recognize. This AMO ID wouldn't be classified, and conversions associated with it would fall under "[!UICONTROL unspecified]" or "[!UICONTROL none]" in [!DNL Analytics] reports.

Fortunately, while issues like this are common, they typically don't result in a high percentage of discrepancy. However, if you notice a large discrepancy between AMO IDs in [!DNL Analytics] and EF IDs in Adobe Advertising, contact your Adobe Account Team for assistance.

## Other Metric Considerations

### The Difference Between Clicks and Visits {#clicks-vs-visits}

They seem analogous, but clicks and visits represent different data:

* **Click:** [!DNL DSP] or the search engine records a click when a visitor clicks an ad on a publisher’s website.

* **Visit:** [!DNL Analytics] defines a [visit](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) as a series of page views by a user, ending according to to one of several criteria, such as 30 minutes of inactivity.

By definition, a click can lead to multiple visits.

Consider the following example: User 1 and User 2 both access a site by clicking an Adobe Advertising ad. User 1 views four pages and then leaves for the day, so the initial click results in one visit. User 2 views two pages, leaves for a 45-minute lunch, returns, views two more pages, and then leaves; in this case, the initial click results in two visits.

![Example of the difference between clicks and visits](/help/integrations/assets/a4adc-visits-example.png)

### The Difference Between Clicks and Click-Throughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Clicks and click-throughs are two different metrics:

* **Click:** [!DNL DSP] or the search engine records a click when a visitor clicks an ad on a publisher’s website.

* **Click-throughs:** [!DNL Analytics] records a click-through when the visitor lands on the destination website, the landing page loads, and the [!DNL Analytics] request at the bottom of the page sends the data to [!DNL Analytics].

Clicks and click-throughs can differ greatly because of accidental ad clicks. We've observed that most clicks on display ads are accidental clicks, and these accidental visitors hit the Back button before the landing page loads, so [!DNL Analytics] can't record a click-through. This is especially true for ads on which an accidental click is more likely, such as mobile ads, video ads, and ads that fill the screen and must be closed before the user can view the page.

Sites loaded on mobile devices are also less likely to result in click-throughs because of lower bandwidths or available processing power, causing landing pages to take longer to load. It's not uncommon for 50-70% of clicks to not result in click-throughs. In mobile environments, the difference can be as high as 90% because of the combination of a slower browser and the higher likelihood that the user accidentally clicks the ad while scrolling through the page or trying to close the ad.

The click data may also be recorded in environments that can't record click-throughs with the current tracking mechanisms (such as clicks going into, or from, a mobile app) or for which the advertiser deployed only one tracking approach (for example, with the view-through JavaScript approach, browsers that block third-party cookies track clicks, but not click-throughs). A key reason that Adobe recommends deploying both the click URL tracking and view-through JavaScript tracking approaches is to maximize coverage of trackable click-throughs.

### Using Adobe Advertising Traffic Metrics for Non-Adobe Advertising Dimensions

Adobe Advertising provides Analytics with [advertising-specific traffic metrics and the related dimensions from [!DNL DSP] and [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). The Adobe Advertising-provided metrics are applicable only to the specified Adobe Advertising dimensions, and data isn't available for other dimensions in [!DNL Analytics].

For example, if you view the [!UICONTROL Adobe Advertising Clicks] and [!UICONTROL Adobe Advertising Cost] metrics by Account, which is an Adobe Advertising dimension, then the total [!UICONTROL Adobe Advertising Clicks] and [!UICONTROL Adobe Advertising Cost] are shown by account.

![Example of Adobe Advertising metrics in a report using an Adobe Advertising dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

However, if you view the [!UICONTROL Adobe Advertising Clicks] and [!UICONTROL Adobe Advertising Cost] metrics by an on-page dimension (such as Page), for which which Adobe Advertising doesn't provide data, then the [!UICONTROL Adobe Advertising Clicks] and [!UICONTROL Adobe Advertising Cost] for each page are zero (0).

![Example of Adobe Advertising metrics in a report using an unsupported dimension](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Using [!UICONTROL AMO ID Instances] as a Substitute for Clicks with Non-Adobe Advertising Dimensions

Since you can't use [!UICONTROL AMO Clicks] with on-site dimensions, you may want to find an equivalent to clicks. You may be tempted to use Visits as a substitute, but they aren't the best option because each visitor may have multiple visits. (See "[The Difference Between Clicks and Visits](#clicks-vs-visits)." Instead, we recommend using [!UICONTROL AMO ID Instances], which is the number of times the AMO ID is captured. While [!UICONTROL AMO ID Instances] don't match [!UICONTROL AMO Clicks] exactly, they are the best option for measuring click traffic on the site. For more information, see "[Click-Through Data Validation for [!DNL Analytics for Advertising]](#data-validation)."

![Example of [!UICONTROL AMO ID Instances] instead of [!UICONTROL Adobe Advertising Clicks] for an unsupported dimension](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Overview of [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising IDs Used by [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Adobe Advertising Metrics in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Data in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Why Data May Vary Between Adobe Advertising and [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
