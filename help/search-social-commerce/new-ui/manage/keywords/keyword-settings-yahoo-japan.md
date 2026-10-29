---
title: '[!DNL LY Ads] keyword settings'
description: Reference the settings for [!DNL LY Ads] keywords.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# [!DNL LY Ads] keyword settings

## [!UICONTROL Basic Settings]

*New keywords only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords. The maximum length is 80 characters, including any [[!DNL LY Ads] match type syntax](https://ads-help.yahoo-net.jp/s/article/H000044997) for keywords.

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* You can create negative keywords from the [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] tab and in the ad group and campaign settings.
>* [!DNL LY Ads] keywords and match types are mutable, which means you can edit them without deleting the existing keyword.

**[!UICONTROL Status]:** The display status of the keyword: *[!UICONTROL Active]* or *[!UICONTROL Paused]*. The default for new keywords is *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** The string to use as the substitution value if the base URL or tracking template contains the `{param1}` [custom parameter](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

**[!UICONTROL Param2]:** The string to use as the substitution value if the base URL or tracking template contains the `{param2}` [custom parameter](https://ads-help.yahoo-net.jp/s/article/H000044803?language=en_US).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

>[!MORELIKETHIS]
>
>* [Manage keywords](keyword-manage.md)
