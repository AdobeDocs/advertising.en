---
title: About ad network accounts
description: Learn about ad network accounts in Search, Social, & Commerce.
exl-id: fca469f1-502c-415a-897d-03b6e6ba34e8
feature: Search Campaign Management
---
# About ad network accounts

*Agency account manager, Adobe account manager, and administrator user roles only*

Search, Social, & Commerce can track any of an advertiser's accounts on supported ad networks. To enable tracking of an account, you must create a corresponding account record. You must set up account details for any type of account, whether or not Search, Social, & Commerce synchronizes with it or optimizes bids and budgets on its ads.

## Accounts synchronized via APIs

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising] (formerly [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], and [!DNL Yandex] accounts*

Search, Social, & Commerce synchronizes (*syncs*) with supported ad network accounts so that you can track, report on, and visualize performance for your ads. For all ad networks except for [!DNL Yahoo! Display Network], you can optionally manage the campaigns for your account in Search, Social, & Commerce; [!DNL Yahoo! Display Network], campaigns are read-only. For all ad networks, you can allow the optimization capability to optimize bids on ads in managed accounts by adding them to portfolios.

To enable synchronizing of an account, the account record must contain the account access credentials and be enabled (active).

During synchronization, Search, Social, & Commerce pulls the advertiser's campaign structures and supported campaign entities, including most of their attributes that are managed or reported in Search, Social, & Commerce. It doesn't include click data, nor bids and bid modifiers entered outside Search, Social, & Commerce, which are gathered separately. Search, Social, & Commerce automatically synchronizes with your ad network accounts once a day, and also whenever it detects a new campaign on one of your ad networks. In addition, it immediately sends all changes to campaign data made from within Search, Social, & Commerce to the ad network. You can optionally request a manual sync when necessary.

For more information about creating and editing synchronized campaigns, see the chapter on "Campaign Management."

## Tracking-only accounts

*[!DNL Naver] Accounts*

Tracking campaigns allow you to track, report on, and visualize performance for the ads that you buy directly from the ad network. Search, Social, & Commerce doesn't synchronize data with the ad network, place bids for the account, nor provide any type of optimization or simulations.

To allow Search, Social, & Commerce to attribute conversions to clicks, set up tracking options in the account record and enable the account record. You can then use bulksheets to generate tracking URLs for your ads and keywords, and manually add the tracking URLs within the [!DNL Naver] ad manager.

See more information about [!DNL Naver] tracking-only campaigns, see "[Implement [!DNL Naver] tracking-only accounts](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)."

>[!MORELIKETHIS]
>
>* [Manage ad network accounts](ad-network-account-manage.md)
>* [Manage merchant center accounts](merchant-account-manage.md)
>* [Update the s\_kwcid tracking code for a [!DNL Google Ads] account](update-skwcid-google.md)
