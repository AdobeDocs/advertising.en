---
title: About tracking for Search, Social, & Commerce
description: Learn about tracking options for Search, Social, & Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
---
# About tracking for Search, Social, & Commerce

To track the performance of your ads, Search, Social, & Commerce needs impression, click, cost, and conversion (transaction) data for your ads. Search, Social, & Commerce uses this data to build the data forecasting models it needs to optimize your ad portfolios.

## Cost, click, and impression data

Search, Social, & Commerce retrieves impression, click, and cost data directly from [supported ad networks](/help/search-social-commerce/introduction/supported-inventory.md) every day. In addition, Search, Social, & Commerce can add a unique click-tracking code (including a redirect to a tracking server) in your tracking templates and destination URLs to track display/content impressions, clicks, and cost and later tie the events to conversions.

If you want to track campaigns on ad networks with which Search, Social, & Commerce doesn't sync data, then you must provide data for those campaigns by sending a daily feed file with the impression, click, and cost data.

### Click-tracking tags

Your Search, Social, & Commerce implementation team sets up click tracking by updating the tracking templates and destination URLs for ads, keywords, placements, product groups, and sitelink extensions in your synched ad campaigns to include a unique tracking ID string and an Adobe Advertising redirect. They also add tracking to the land page suffixes (final URL suffixes) for your [!DNL Google Ads] and [!DNL Microsoft® Advertising] accounts and campaigns.

The tracking parameters enable Adobe Advertising to track clicks at an individual keyword level (search campaigns) or ad variation level (search campaigns with content or site targeting, display campaigns, and social campaigns). Each time a user views a display/content ad or clicks one of your ads, the ad network sends the event to the Adobe Advertising pixel servers using a click-tracking tag associated with the keyword or ad. For clicks:
  
* For [!DNL Google Ads] and [!DNL Microsoft® Advertising] ads on browsers that support parallel tracking, the ad network sends the click to your website first and then to the Adobe Advertising pixel servers, which then place a cookie on the user’s computer, if one doesn't already exist.
  
* In all other cases, the ad network sends the click directly to the Adobe Advertising pixel servers. The pixel server places a cookie on the user’s computer (if one doesn't already exist) and then redirects the user to the relevant URL on your website. The overall experience for the end user is the same as it would be without a redirect.

The cookie is set in the [!DNL Adobe] domain (`everesttech.net`) as a first-party cookie. After a redirect, the user is on the advertiser's domain, and the cookie is then treated as a third-party cookie. For more information about Adobe Advertising cookies, see "[Adobe Advertising cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html)."

## Conversion data

When a customer clicks an ad or views a display or social ad, Search, Social, & Commerce needs to map each resulting conversion back to the originating click or display/social impression.

The advertiser plays a role in supplying the conversion data for all clicks and display/social impressions. Conversion data can include information about any type of event that occurs on a website that may be used for bid optimization. You can provide conversion data by implementing conversion tracking code in the advertiser's conversion pages (such as the "success" page that's displayed after a customer completes a transaction) or by sending a daily feed file with conversion data that was captured by another method.

### Conversion-tracking tags

You can use [conversion tags from various vendors](/help/search-social-commerce/tracking/conversion-tracking-about.md).
  
When you use an Adobe Advertising conversion tag and a user completes a successful transaction and lands on a "success" page, the Adobe Advertising pixel server checks for the existence of the cookie on the user’s computer, which was set at the time of the click redirect. When it finds a cookie, information about the transaction event is passed using the ef_transid parameter, and the transaction is recognized as a conversion and is credited to the preceding ad click or display impression.

If the user clicked more than one of your ads, Adobe Advertising credits the transaction to the final ad click or (for display or video campaigns) the final ad impression unless you specify otherwise. Your [click lookback window](/help/search-social-commerce/glossary.md#c-d) and [impression lookback window](/help/search-social-commerce/glossary.md#i-j) determine the number of days after a paid click or a display/video impression (respectively) occurs in which the event can be attributed to a conversion.
  
The Adobe Advertising implementation team works with the advertiser to determine the format of the conversion tags the advertiser needs to implement, identify the webpages on which each conversion tag should be inserted, and then provide the conversion tags to implement.
