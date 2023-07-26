---
title: FAQs about campaigns
description: See answers to questions about campaign management and campaign data views.
exl-id: b5975869-4bc3-461d-8cb7-eeefab157137
---
# FAQs about campaign management

## General information

+++Can I move campaigns and components from one account to another?

Don't move or copy a campaign or campaign component, which has a unique ID, to an account with a different account ID. Doing so will result in data errors.
+++

+++When is click data updated from the ad networks?

The process of pulling the previous day's click data from the search engines begins at 06:00 in the advertiser's time zone.

In addition, [!DNL Google Ads] campaign-level performance metrics on the search network for the current day are pulled at 08:00 and 16:00 in the advertiser's time zone.
+++

+++What actions causes keywords and ads to lose their history?

>[!NOTE]
>
>(Advertisers with portfolios) Expect the performance of new keyword and match type combinations to be volatile while Search, Social, & Commerce gathers data to create new models.

**Actions in the [!UICONTROL Search] > [!UICONTROL Campaigns] views, in the bulksheet posting process, and in the ad network's own editor:**

The existing keyword or ad is deleted and another one is created when:

* ([!DNL Baidu], [!DNL Google Ads], and [!DNL Yandex]) You edit a keyword name.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], and [!DNL Yandex]) You change a keyword's match type.

* You move a keyword between ad groups.

* ([!DNL Google Ads] dynamic search ads, [!DNL Microsoft Advertising] expanded text ads, and all ad types on other supported ad networks) You edit ad copy (headline/title or description) or an ad image.

* You move an ad between ad groups.

**Events in the product inventory feed posting process:**

An existing ad or keyword is deleted and another one is created when:

* A feed file contains a new value for a column used in an ad variation.

* The template settings for an ad changed since the last propagation.

* A new feed file includes a row for an ad or keyword that a) was in a previous file but b) has been omitted since then and was paused or deleted according to the feed data settings.

Depending on the [feed data settings](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), an existing ad or keyword may be deleted when:

* A new feed file doesn't include a row for an existing ad or keyword.

* The scheduled end date for the components of a posted feed file occurs.

* The stock level of an item dips below a minimum specified in the feed data settings.
+++

+++([!DNL Google Ads] campaigns) Changes to the display names for my [!DNL Google]-tracked conversions were reverted.

If you change the display names of the conversion metrics in Search, Social, & Commerce, your changes are overwritten with the names configured in [!DNL Google Ads]. Make any name changes within [!DNL Google Ads].
+++

+++(Google Ads campaigns) Can I use a shared budget for campaigns in portfolios?

For best results, don't add [!DNL Google Ads] campaigns to an [!DNL Google Ads] shared budget if they're in optimized portfolios that are configured to "[!UICONTROL Auto adjust campaign budget limits]." If you do, [!DNL Google Ads] overrides the Search, Social, & Commerce optimized campaign budgets, which may lead to bidding inefficiencies.
+++

+++([!DNL Google Ads] campaigns) Can I send mobile and non-mobile users to different landing pages?

You can use the [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` and `{ifnotmobile}` to determine the domain name of the landing page in one of two ways, as applicable for your sites:

* Include the mobile designation as the host server using `{ifmobile:m}{ifnotmobile:www}`.

  For example, `http://{ifmobile:m}{ifnotmobile:www}.example.com` takes mobile users to m.example.com and non-mobile users to www.example.com.

* Include the mobile designation as the top-level domain using `{ifmobile:mobi}{ifnotmobile:com}`.

  For example, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` takes mobile users to www.example.mobi and non-mobile users to www.example.com.

In both cases, the base URLs with Search, Social, & Commerce tracking include the unencoded `{}` tags and any additional parameters appended to the base URL.

>[!NOTE]
>
>Don't use a full URL as the value for ifnotmobile and ifmobile parameters; use only the variable part of the URL (such as "m" versus "www," or "mobi" versus "com").

+++

+++([!DNL Google Ads] campaigns on the search network) What data is shown for today?

[!DNL Google Ads] campaign-level performance metrics on the search network for the current day are pulled at 08:00 and 16:00 in the advertiser's time zone.

In the [!UICONTROL Campaigns] tab in both  the [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view and the [!UICONTROL Optimization] > [!UICONTROL Portfolios] view, when you report on [!UICONTROL Today] or a custom date range that includes the current day, the data will include the most recently-pulled data.

>[!NOTE]
>
>Data for clicks, impressions, and conversions are delayed by three hours and aren't complete until the next data pull.

+++

+++([!DNL Google Ads] and [!DNL Microsoft Advertising]) Does Search, Social, & Commerce support parallel tracking for ads in [!DNL Google Ads] or [!DNL Microsoft Advertising]?

Parallel tracking sends customers directly from your ad to your final URL, and your tracking template URL (with click measurement) is loaded in the background; as a result, your landing page is loaded more quickly.

Search, Social, & Commerce supports parallel tracking for search and shopping campaigns using the ad network's click identifier (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]). Use an [account-level](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) or [campaign-level](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (called "[!DNL final URL suffix]" in the ad networks), which is appended to landing page URLs to track clicks on child ads from browsers that support parallel tracking. See the [required suffix formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) and [required suffix formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

When a user views your ad on a browser that doesn't support parallel tracking, the ad network uses sequential tracking instead: customers are first sent to your tracking template URL, which may redirect customers to intermediate tracking servers before redirecting them to the final URL. All tracking templates for an ad network account should include the same click identifier parameter that you use in the [!UICONTROL Landing Page Suffix]. See the [tracking template formats for [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) and the [tracking template formats for [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Why do tracking URLs for my ads include "`&EV_HASH={<hash>}`?"

When you upload ads using a [product inventory feed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) for an account with the Search, Social, & Commerce pixel redirect and with keyword- and creative-level tracking, then Search, Social, & Commerce adds the hash parameter and value to the ad's tracking template or destination URL to identify that it was created using the inventory feed feature.
+++

## Inventory feeds

+++(Product inventory feeds) Should I pause or deleted ads that are obsolete or are for a product whose stock level is below a specified minimum?

It depends on the advertiser's business requirements.

When you pause ads, they're reactivated if you resubmit the same ad or the stock level goes above the minimum. This allows you to retain the ad's history.

When you delete ads and resubmit them, new ads are created, and historical data will need to be accumulated. If you don't expect to resubmit deleted ads, however, having historical data isn't important.
+++

+++(Product inventory feeds) If I delete an ad template and then create a new, identical one, are missing items in the next feed file paused (when the feed file settings are configured to do so)?

If the next feed file is missing line items and you haven't previously posted those line items from the new template via a previous feed file, then the missing line items aren't recognized as "missing," so they aren't created. To avoid this, propagate the previous feed file through the new template and post the data before propagating and posting data from a new file.
+++

+++(Product inventory feeds) Can I update prices for my products without affecting an ad's quality score?

For [!DNL Google Ads] campaigns, yes: The [!DNL Google Ads] `{Param 1}` and `{Param 2}` variables allow you to dynamically insert numeric values in an ad variation without deleting and recreating the ad, and therefore without affecting the quality score.

To use a `{Param 1}` or `{Param 2}` variable for your price data, map the price column in your data file to that variable in the appropriate feed templates, and then include the variable in your ad variation templates.

For example, if the column is called "Price," then open the feed template that creates the ads, click in the input field next to **[!UICONTROL Param 1]**, and then click the **[!UICONTROL Price]** column in the [!UICONTROL Feeds/Available Columns] list, which inserts `[Price]` as the value for [!UICONTROL Param 1]. Then, in the ad variation template at the bottom of the feed template, insert `{param1:default text}`, where "default text" is text to use if the parameter column in the feed file is empty for an ad row.

When you submit data, the data fields for the [!UICONTROL Param1] and [!UICONTROL Param2] columns may include up to 25 characters, including numeric data, currency symbols and currency codes, and the following non-numeric characters: `, . % + - /`
+++

+++My campaigns generated from inventory feeds have many orphan transactions.

If the [feed data settings](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) are configured to delete ads in various situations, then any delayed conversions that occur after clicks on the ad may cause [orphan transactions](/help/search-social-commerce/glossary.md#o-p). The best practice is to pause ads instead of to delete them. If an ad still hasn't received any revenue after a long period of time, then you can delete it via a bulksheet or the ad management view.
+++
  
## Account- and campaign-related performance issues

+++Some of my campaigns are spending more or less than the campaign budgets.

* This is normal in an optimized portfolio that is configured with the "[!UICONTROL Auto-adjust campaign budget limits]" option. When this option is enabled, you may spend up to *N* times each campaign's budget, where *N* is the value of the "[!UICONTROL Multiple]" setting. This option allows the optimization capability to adjust spending for individual campaigns as necessary while steering the entire portfolio to meet its target.
* If [!DNL Google Ads] campaigns use a shared budget, then [!DNL Google Ads] adjusts spending for individual campaigns as necessary to spend the entire shared budget.
+++
