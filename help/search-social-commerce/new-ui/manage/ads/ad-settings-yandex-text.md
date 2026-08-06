---
title: "[!DNL Yandex] text ad settings"
description: Reference the settings for [!DNL Yandex] text ads.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
---
# [!DNL Yandex] text ad settings

<!-- DON'T HAVE ANY CAMPAIGNS TO TEST WITH -->

## [!UICONTROL Basic Settings]

*New ads only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

## [!UICONTROL Text Ad Settings]

**[!UICONTROL Ad Title]:** The headline of the banner (ad). The maximum length is 33 characters, and a single word can't include more than 23 characters.

>[!NOTE]
>
>Changing the ad copy for a [!DNL Yandex] ad deletes the existing ad and creates a new ad with the same properties.

**[!UICONTROL Description Line 1]:** The body of the banner (ad). The maximum length is 75 characters, and a single word can't be more than 22 characters.

>[!NOTE]
>
>Changing the ad copy for a [!DNL Yandex] ad deletes the existing ad and creates a new ad with the same properties.

**[!UICONTROL Status]:** The ad status: *[!UICONTROL Active]* or *[!UICONTROL Paused]*.

## [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

>[!NOTE]
>
>The URL can also include the [`{param1}` and `{param2}`](https://yandex.com/support/direct/statistics/url-tags.html) substitution variables. When you use them, the variables are substituted with the `{param1}` and `{param2}` values defined for the keyword that's used to display the ad.

>[!MORELIKETHIS]
>
>* [Manage ads](/help/search-social-commerce/new-ui/manage/ads/ad-manage.md)
