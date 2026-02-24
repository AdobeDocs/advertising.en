---
title: (New UI) About ad network accounts
description: Learn about ad network accounts in the new Search, Social, & Commerce UI.
feature: Search Campaign Management
---
# (New UI) About ad network accounts

Search, Social, & Commerce can track any of an advertiser's accounts on supported ad networks. To enable tracking of an account, you must create a corresponding account record. You must set up account details for any type of account, whether or not Search, Social, & Commerce synchronizes with it or optimizes bids and budgets on its ads.

## Accounts synchronized via APIs

*[!DNL Google Ads], [!DNL Microsoft Advertising] (formerly [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex], and existing [!DNL Baidu] accounts*

Search, Social, & Commerce synchronizes (*syncs*) with supported ad network accounts so that you can track, report on, and visualize performance for your ads. For all ad networks except for [!DNL Yahoo! Display Network], you can optionally manage the campaigns for your account in Search, Social, & Commerce; [!DNL Yahoo! Display Network], campaigns are read-only. For all ad networks, you can allow the optimization capability to optimize bids, campaign budgets, and campaign bid strategy targets for campaigns in managed accounts, by adding the campaigns to portfolios.

To enable synchronizing of an account, the account record must contain the account access credentials and be enabled (active).

During synchronization, Search, Social, & Commerce pulls the advertiser's campaign structures and supported campaign entities, including most of their attributes that are managed or reported in Search, Social, & Commerce. It doesn't include click data, nor bids and bid modifiers entered outside Search, Social, & Commerce, which are gathered separately. Search, Social, & Commerce automatically synchronizes with your ad network accounts once a day, and also whenever it detects a new campaign on one of your ad networks. In addition, it immediately sends all changes to campaign data made from within Search, Social, & Commerce to the ad network. You can optionally request a manual sync when necessary.

For more information about creating and editing synchronized campaigns, see the chapter on "Campaign Management."

## Accounts for which you manually upload data

For online ad networks for which Search, Social, & Commerce doesn't provide API support, you can upload campaign content and offline cost, click, and conversion data for an account for reporting and performance simulations. Search, Social, & Commerce doesn't synchronize data with the ad network, provide automated bidding, nor provide any type of optimization, but it allows you to streamline cross-channel insights and to identify opportunities for manual optimization.

## Template-based tracking-only accounts

*Available for existing [!DNL Naver] accounts only*

Tracking campaigns allow you to track, report on, and visualize performance for the ads that you buy directly from the ad network. Search, Social, & Commerce doesn't synchronize data with the ad network, provide automated bidding, nor provide any type of optimization or simulations.

To allow Search, Social, & Commerce to attribute conversions to clicks, set up tracking options in the account record and enable the account record. You can then use bulksheets to generate tracking URLs for your ads and keywords, and manually add the tracking URLs within the [!DNL Naver] ad manager.

You can't set up new [!DNL Naver] accounts in Search, Social, & Commerce. See more information about [!DNL Naver] tracking-only campaigns, see "[Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)."

>[!MORELIKETHIS]
>
>* [Manage ad network accounts via API connection](/help/search-social-commerce/new-ui/set-up/accounts/api-account-manage.md)
>* [Manage ad network accounts for data uploads](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Manage [!DNL Naver] accounts for tracking only](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Manage merchant center accounts](merchant-account-manage.md)
