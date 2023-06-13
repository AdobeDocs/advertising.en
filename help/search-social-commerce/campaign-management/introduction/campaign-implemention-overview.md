---
title: Overview of implementing ad network accounts and campaigns
description: Learn about the tasks involved in setting up, synching, and managing your ad network accounts.
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
---
# Overview of implementing ad network accounts and campaigns

Adobe works with each advertiser to set up its ad network accounts and campaigns. This includes configuring Search, Social, & Commerce to connect and synchronize with the advertiser's accounts, creating new campaigns and campaign components as necessary, setting up tracking for the component ads, optionally adding the campaigns to portfolios to allow Search, Social, & Commerce to optimize bid on the ads, and validating the initial cost, click, and revenue data.

After a campaign is activated and optionally added to a portfolio, the Adobe account management team, the agency team, or the advertiser (depending on the terms of the service level agreement) will need to monitor each campaign and to change the relevant components and settings as necessary to meet the advertiser's goals.

This page includes information about all account types, including how to set up campaign structure for synchronized accounts. For additional instructions on setting up tracking-only accounts for [!DNL Naver], see "[Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)."

## Initial setup tasks for accounts and campaigns

[!DNL Adobe] and/or your agency will work with you do the following:

1. (New advertiser accounts) Set up administrative accounts:

   1. Set up the advertiser's account.
  
   1. (If necessary) Create user accounts for the advertiser to view and manage its campaign data and to generate reports.

1. (Some ad networks) Gain authorization for Search, Social, & Commerce to access each account using the ad network's API and the Search, Social, & Commerce user interface.

1. For each ad network account:

   1. (If necessary) Set up the account on the ad network.

   1. Integrate with the account by [creating a corresponding account record](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in Search, Social, & Commerce containing the account access credentials and tracking options, and set the account status to enabled.

      Search, Social, & Commerce then synchronizes with the ad network. If the account already contains campaign data, then the data is available in about 24 hours.
   
   1. ([Ad types you can create/edit](/help/search-social-commerce/introduction/supported-inventory.md) in Search, Social, & Commerce) If the account doesn't already contain campaign data, then create campaign structure and campaign components from within Search, Social, & Commerce by any of the following methods that are available for the ad type:
     
       * (Google Ads, Microsoft Advertising, Yahoo! Ads, and Yandex accounts only) Set up an [automated process to create dynamic ads and keywords targeted to each item in your inventory](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) according to an ad network-specific ad template you create and the contents of inventory data files you upload to an FTP location.
     
       * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, and Yandex accounts only) Upload [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) containing as much data as you want for an account and then posting them to the ad networks.
     
       * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads, and Yandex accounts only) Enter data for individual components directly into the interface. For most campaign and ad types, you can create data at the campaign level, ad group level, and individual keyword, placement, and ad levels.

       Some campaign and ad types, however, require unique workflows. See instructions for setting up [[!DNL Microsoft Advertising] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamic search ads](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] performance max campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md), and [[!DNL Google Ads] shopping campaigns](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).
   
   1. ([!DNL Naver] tracking-only accounts only) Upload [bulksheet files](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) with data to replicate the existing campaigns, ad groups and keywords in Search, Social, & Commerce without posting them to [!DNL Naver].

1. Set up tracking for all ads for which Adobe Advertising will track conversions:

   1. (Advertisers with the Adobe Advertising conversion tracking service) If necessary, [set up click tracking](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) for ads, and optionally for keywords, placements, and ad extensions by generating and uploading Search, Social, & Commerce click-tracking URLs.

      For [!DNL Google Ads] performance max campaigns, set up all tracking in the [campaign's tracking settings](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. For tracking-only campaigns, you must instead generate destination URLs using bulksheets, and then add the generated destination URLs to the relevant entities using the ad network's native editor.
   
   1. Set up conversion tracking. Depending on the implementation, this may involve adding conversion tracking tags to the advertiser's webpages and/or setting up a daily feed drop for conversion data that the advertiser has collected separately.

       If you use the Adobe Advertising conversion tracking service, you can generate conversion tracking tags [within Search, Social, & Commerce](/help/search-social-commerce/tools/conversion-tag-generate.md) or [using Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).
   
   1. Validate the data that's tracked.

   For more details about setting up tracking, see the chapter on "Tracking."

1. (Advertisers with Adobe Analytics) [Integrate Adobe Advertising and Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) so that they can exchange data.

1. (To allow Search, Social, & Commerce to optimize bids and/or campaign budgets; [supported campaign types](/help/search-social-commerce/introduction/supported-inventory.md) only) [Assign the campaign to a portfolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   If the portfolio isn't already launched (optimizing bids and/or budgets), then let the optimization capability gather enough data that it can build cost and revenue models so you can establish the baseline performance for the portfolio before you launch it.

   If the portfolio is already launched, then enable learning for the portfolio. For more information, see "Adjusting the portfolio strategies." You should expect the portfolio to be volatile after you add new campaigns, while the optimization capability gathers data on the campaign's bid units. Bidding automatically adjusts within one to three weeks.

   For more information about portfolios, see the Optimization Guide, which is available from within Search, Social, & Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. (If any new conversions will be tracked for the advertiser) [Make the conversions available](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) for reports, campaign management views, and portfolio objectives.

1. For each campaign, verify that Search, Social, & Commerce is receiving click and cost data from the ad network, and validate the revenue data shown in Search, Social, & Commerce with the advertiser's own revenue data.

1. (Optional) Automate reporting by setting up report templates, spreadsheet feeds, and FTP delivery of scheduled reports.

   For instructions, see the chapter on "Reports."

>[!MORELIKETHIS]
>
>* [About campaign management in Search, Social, & Commerce](campaign-management-about.md)
>* [Monitor and manage the performance of your ad network campaigns](monitor-performance-campaigns.md)
>* [Google Ads conversion data in Search, Social, & Commerce](google-conversion-data.md)
>* [Supported inventory](/help/search-social-commerce/introduction/supported-inventory.md)
