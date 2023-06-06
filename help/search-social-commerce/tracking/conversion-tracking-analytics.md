---
title: Adobe Analytics conversion tracking
description: Learn about using Adobe Analytics conversion tracking for your campaigns in Adobe Advertising.
---
# Adobe Analytics conversion tracking

*Advertisers with an Adobe Advertising-Adobe Analytics integration only*

For advertisers with an Adobe Advertising-Adobe Analytics integration, Advertising Cloud can connect your ad clicks and impressions with the site engagement and conversion metrics tracked by [!DNL Analytics] when you use a redirect with token (`ef_id` parameter) in your click-tracking URLs for your [bid units](/help/search-social-commerce/glossary.md#a-b). The [!DNL Analytics] data is automatically sent to Advertising Cloud via a daily feed file.

See "[Overview of [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html)" for more information about the integration.

>[!PREREQUISITES]
>
> Time zones in the Search, Social, & Commerce advertiser account, the [!DNL Analytics] report suites, and the ad network accounts must match. If they don't match, data variances will exist across systems.

## Implementation overview 

1. In [!DNL Analytics], your Search, Social, & Commerce implementation team modifies the following configuration settings for each report suite:

   * The expiration for the `ef_id` eVar is changed to match the advertiser's click lookback window for Adobe Advertising.
   
   * The Adobe Advertising user ID.
   
   * Standard and custom events to use for optimization.

1. In Search, Social, & Commerce, your implementation team:

   1. Synchronizes the existing ad network accounts hierarchy into Search, Social, & Commerce.
   
   1. Adds redirects with "`ef_id`" token passing to the tracking URLs and posts them to the ad network.
   
     This step prepends a redirect to the Adobe Advertising tracking server (except for [!DNL Google Ads] and [!DNL Microsoft Advertising] ads in browsers that support parallel tracking) and adds a dynamically populated "ef_id" parameter to the URL at the time of the ad click. When parallel tracking applies, end users are sent directly from your ad to your final URL, and your tracking template URL (with click measurement) is loaded in the background.

Once the integration is complete, Search, Social, & Commerce automatically receives all on-page event data tracked in [!DNL Analytics] for the report suites that were configured.

>[!MORELIKETHIS]
>
>* [Conversion tracking options](conversion-tracking-about.md)
