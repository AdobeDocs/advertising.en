---
title: Conversion tracking options for Search, Social, & Commerce
description: Learn about conversion tracking options for Search, Social, & Commerce.
---
# Conversion tracking options for Search, Social, & Commerce

Search, Social, & Commerce can use conversion data that's tracked in the following ways:

* **Adobe Advertising-tracked conversions:** The advertiser inserts an Adobe Advertising conversion-tracking tag on each conversion page. The tag sends the conversion data to a tracking server. You can use either the legacy third-party pixel or the newer first-party pixel. See "[Comparison of each conversion tracking method](#conversion-tracking-comparison)."

* **Adobe Analytics conversions:** The advertiser uses Adobe Analytics tracking for all conversions. This option requires an Adobe Advertising-Adobe Analytics integration. See "[Adobe Analytics conversion tracking](conversion-tracking-analytics.md)" for more information.

* **[!DNL Google Analytics] conversions:** The advertiser uses the [!DNL Google Analytics] tag to track all conversions. See "[[!DNL Google Ads] conversion data in Search, Social, & Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)" for more information about the conversions that are automatically synced.

* **Advertiser-tracked conversions:** (Search, Social, & Commerce clients only) The advertiser provides Search, Social, & Commerce a feed file with any combination of online and offline conversion data. See "[Conversion tracking using an EF ID feed](feed-efid.md)" and "[Conversion tracking using a transaction ID feed](feed-transaction-id.md)."

## Comparison of each conversion tracking method {#conversion-tracking-comparison}

As browser cookie policies continue to become stricter, it's important to understand your current tracking capabilities and to identify your best options for the longer term.

| Tracking Method | Description | Limitations | Benefits | Recommended? |
|----|----|----|----|----|
| Adobe Analytics | Advertisers with [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) automatically import their [!DNL Analytics] standard and custom events to Adobe Advertising for reporting and optimization. | <ul><li>[!DNL Safari] allows only a seven-day conversion lookback, which is reset on repeat site visits during the lookback window.</li><li> Expect similar limitations in [!DNL Chrome] in 2024.</li></ul> | <ul><li>Seamless integration with [!DNL Analytics]</li> <li>See paid search data in [!DNL Analytics] Analysis Workspace</li><li>Benefits beyond paid search</li></ul> | Yes |
| Legacy Adobe Advertising Pixel | Advertisers add legacy Adobe Advertising image or JavaScript pixels to their conversion pages. The pixel fires when a user who clicked an ad reaches the page. This method relies on third-party cookies. | <ul><li>[!DNL Safari] blocks all conversion tracking using this method.</li><li>Expect similar limitations in [!DNL Chrome] in 2024.</li></ul> | The pixel is already implemented. However, you still must [implement the additional ITP mapping tag](itp-conversion-mapping-tag.md).<br><br>Recommendation: Switch to the first-party pixel. | No |
| Adobe Advertising First-party Pixel | Advertisers do the following: <ul><li>Implement the JavaScript library for the [Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) across their entire site.</li><li>Add the Adobe Advertising [JavaScript tags with ITP mapping](itp-conversion-mapping-tag.md) to any page that could be a landing page from a search click (ideally, on all pages, since landing pages may change over time). The tag allows Adobe Advertising to track a conversion event that occurs on a page that's converts large numbers to scientific notation the landing page.</li><li>Add the Adobe Advertising [JavaScript conversion tracking tag v3](format-conversion-tag-jsv3.md) to conversion pages.</li></ul> | <ul><li>[!DNL Safari] allows only a seven-day conversion lookback, which is reset on repeat site visits during the lookback window.</li><li>Expect similar limitations in [!DNL Chrome] in 2022.</li></ul> | [!DNL Safari] tracks conversions during the seven-day lookback. Because the lookback is reset on repeat site visits during the lookback window, the limitation doesn't affect all [!DNL Safari] users. | No |
| EFID Feed | The advertiser's search accounts are set up to generate destination URLs/final URLs with Adobe Advertising unique IDs (tokens). When a user clicks an ad, Adobe Advertising creates a unique ID (`EFID`) and displays it at the end of the final URL. The advertiser's client system captures the EFID as a unique identifier for conversions that result from the click and sends it to Adobe Advertising in a revenue feed that includes the EFID, transaction date, and conversion property. Adobe Advertising then uses the EFID to match the conversion to the original click. | <ul><li>The advertiser must have a way to capture the EFID and send automated feeds to Adobe Advertising daily.</li><li>Conversions can be tracked for up to 180 days (per Adobe Advertising) or according to the limits of the advertiser's system.</li></ul> | <ul><li>This method uses first-party conversion data, so it's not affected by third-party cookie limitations.</li><li>Online and offline conversions can be sent in one feed.</li><li>No code changes or tags are required for the site.</li></ul> | Yes |
| Transaction ID Feed [combo feed] | Advertisers add Adobe Advertising pixels that include a parameter for a unique transaction ID (`ev_transid=&lt;transid&gt;`) to their webpages, and Adobe Advertising captures the unique Transaction ID that's created when the pixel fires. The advertiser's client system also captures the [!UICONTROL Transaction ID] and sends Adobe Advertising a revenue feed for offline conversions with matching [!UICONTROL Transaction ID] values | <ul><li>If the advertiser is using the legacy pixel, which [!DNL Safari] blocks from firing, then the ID isn't captured to use for offline data.</li><li>The feed isn't automated.</li></ul> | <ul><li>If you implement the first-party pixel, then the [!UICONTROL Transaction ID] is captured in [!DNL Safari].</li><li>Provides tracking of offline/approved conversion events.</li></ul> | No |
| Google Conversions | Conversions tracked with [!DNL Google Analytics] tags are automatically imported to Adobe Advertising via an API connection. Each conversion name has a `&quot;GGL_&quot;` prefix. | <ul><li>Google typically doesn't track offline data.</li><li>Microsoft® Advertising conversions aren't included.</li></ul> | Google uses machine learning to extrapolate "[modeled conversions](https://support.google.com/google-ads/answer/10081327)." | No |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [About Adobe Advertising conversion-tracking tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics conversion tracking](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Conversion tracking using an EF ID feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Conversion tracking using a transaction ID feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
