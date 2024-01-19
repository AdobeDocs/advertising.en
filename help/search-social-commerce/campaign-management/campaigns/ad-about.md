---
title: Manage ads
description: Learn about ads in Search, Social, & Commerce, including the available ad types.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
---
# About ads

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex], and existing [!DNL Baidu] accounts only*

An ad can be displayed on a target web site (for content, or placement-targeted, campaigns); when a user searches for one of the keywords in the ad group (for search campaigns) or for content on your website (dynamic search ads in [!DNL Google Ads] search-only campaigns); or when a user performs a search relevant to one of the items in your [!DNL Google Merchant Center] or [!DNL Microsoft® Merchant Center] product feed (shopping ads in [!DNL Google Ads] or product ads in [!DNL Microsoft® Advertising] campaigns).

## Available ad types

You can create and manage supported ad types for ad groups within a synchronized ad network account:

* **Text ads or expanded text ads** for an ad group in a campaign that targets the search network. Text ads may include optional tracking parameters that override the ad group- or campaign-level parameters. Depending on the ad network, you may be able to create either expanded/extended text ads or standard text ads.

* Cross-device, native **audience ads** for [!DNL Microsoft® Advertising] campaigns on the [!DNL Microsoft® Audience Network]. You have two options for audience ads, based on the campaign settings:

   * If the campaign is linked to a merchant center store, then let the ad network automatically generate ads feed-based ads for the campaign, using the store's product information. You don't need to create feed-based ads for the campaign, but you must create ad groups with user targeting.
   
   * If the campaign isn't linked to a merchant center account, then create image-based audience ads using the responsive ad format, which includes multiple text and image assets. The ad network assembles the ads using the most effective combinations of ad elements and displays them on sites like [!DNL MSN], [!DNL Outlook.com], and [!DNL Microsoft® Edge].

* **Call-only ads** for [!DNL Google Ads] campaigns on the search network. Call-only ads are text ads that include a telephone number. You optionally can use a [!DNL Google Ads]-assigned forwarding number for advanced call reporting.

* **Expanded dynamic search ads** (now called just "dynamic search ads" on the ad networks) for [!DNL Google Ads] and [!DNL Microsoft® Advertising] dynamic search ad groups in search campaigns. Dynamic search ads use content from your website, instead of keywords, to decide when to show your ads. The ad network dynamically generates the headline, chooses the landing page URL and display URL, and automatically generates the final URL.

   You can define the pages in your websites whose content is used to target your dynamic search ads by setting up specific dynamic search targets for the ad group. For [!DNL Google Ads], you can create dynamic search targets in Search, Social, & Commerce; for [!DNL Microsoft® Advertising], you must create them within [!DNL Microsoft® Advertising]. In [!DNL Google Ads] campaigns, you can optionally specify a website domain and language in the campaign's "[!DNL DSA Options]" section instead of, or in addition to, creating dynamic search targets.

   When a user's search term exactly matches a keyword in one of your keyword-based campaigns, an ad from the keyword-based campaign is displayed instead of a dynamic search ad. The ad network shows a dynamic search ad instead of a keyword-targeted ad when the user's search term is a broad match or phrase match to one of your keywords and your dynamic search ad has a higher ad rank.

   For more information about dynamic search ads, see the [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2471185) and [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia ads** for [!DNL Microsoft® Advertising] search campaigns. Multimedia ads are large image ads that are shown in prominent mainline and sidebar positions, and only one multimedia ad is displayed per page. They can include multiple text and image assets, like responsive ads, and the ad network assembles the ads using the most effective combinations of ad elements. Multimedia ads don't replace your text ad placements.

* Promotion lines for **[!DNL Microsoft® Advertising] product (shopping) ads** on the shopping network. Shopping ads use products in your existing [!DNL Microsoft® Merchant Center] product feed, instead of keywords, to decide how and where to show your ads. The ad copy and landing page URLs are generated automatically from your product information in the feed, but, you can optionally set up promotion lines to include for the ad group.

   You can control which products are shown with your [!DNL Microsoft® Advertising] shopping ads by setting up separate product groups for the ad group, from the [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] view.

   For more information about the workflow for product/shopping ads, see "[Implement [!DNL Microsoft® Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)."  For additional information about product ads, see the [Microsoft® Advertising documentation](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsive search ads for [!DNL Google Ads] and [!DNL Microsoft® Advertising] campaigns on the search network. The ad network dynamically assembles text-based responsive search ads from a set of ad titles and descriptions, favoring combinations that perform well together. The ad includes up to three headlines, two descriptions, and a customizable URL from the base URL and optional path1 and path2 fields. You can optionally pin ad titles and descriptions to specific positions. 

>[!NOTE]
>
>[!DNL Google Ads] don't provide data outside of its native editors about the text combinations that were displayed as ads. For more information about reporting for each text combination, see the [Google Ads documentation](https://support.google.com/google-ads/answer/7684791).

## The [!UICONTROL Ads] view

You can create, edit, and change the status of ads from the [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] view.

## Ad-level performance data

Ad-level data is available for most ad types.

However, it isn't available for [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping, and [!DNL YouTube] campaigns. Expect discrepancies between the total ad-level data for a campaign and the total data for the campaign.

| Ad Network/Campaign/Ad Type | Data Availability |
|---|---|
| [!DNL Google Ads] dynamic search ad (DSA) | Campaign, ad group |
| [!DNL Google Ads] performance max | Campaign |
| [!DNL Google Ads] shopping, smart shopping | Campaign, ad group |
| [!DNL Google Ads] [!DNL YouTube] | Campaign, ad group |

>[!MORELIKETHIS]
>
>* [Manage ads](ad-manage.md)
