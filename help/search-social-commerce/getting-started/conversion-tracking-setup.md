---
title: Setting up conversion tracking for your webpages
description: Learn how to enable Adobe Advertising to track conversions resulting from ad impressions and clicks. 
---
# Setting up conversion tracking for your webpages

Before you can generate reports on conversion data, Adobe Advertising needs impression, click, cost, and conversion (transaction) data for each of your keywords and ads. Adobe Advertising also uses this data to build the data forecasting models it needs to optimize campaign budgets and the bids on your keywords and ads.

To enable Adobe Advertising to track conversions resulting from ad impressions and clicks, you need to do the following:

* Include a unique click tracking code (and maybe additional code to redirect the end user to a tracking server) in the tracking template or destination URL for each keyword, ad, placement, sitelink, and product group in each ad campaign that Search, Social, & Commerce manages. This allows Adobe Advertising to track each ad impression (for display and social ads only) and each click on an ad.

* Track conversion data in one of the following ways:

  * **Adobe Advertising-tracked conversions:** The advertiser inserts an Adobe Advertising conversion-tracking tag on each conversion page.

  * **Adobe Analytics conversions:** The advertiser uses Adobe Analytics tracking for all conversions.

  * **[!DNL Google Analytics] conversions:** The advertiser uses the [!DNL Google Analytics] tag to track all conversions.

  * **Advertiser-tracked conversions:** The advertiser provides a daily feed file with any combination of online and offline conversion data.

For detailed information about implementing tracking, see the help chapter on "Tracking."

>[!MORELIKETHIS]
>
>* [Generate an Adobe Advertising conversion tag](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Generate a Search, Social, & Commerce click-tracking URL using the Tracking URLs tool](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [Decode a Search, Social, & Commerce click-tracking URL](/help/search-social-commerce/tools/click-tracking-url-decode.md)
