---
title: '[!DNL Microsoft Advertising] keyword settings'
description: Reference the settings for [!DNL Microsoft Advertising] keywords.
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
# [!DNL Microsoft Advertising] keyword settings

You can create keywords for campaigns that use the search and display networks.

## [!UICONTROL Basic Settings]

*New keywords only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords, including any [!DNL Microsoft Advertising] match syntax and placeholders. The maximum length per keyword is 100 characters.

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* You can create negative keywords from the [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] tab and in the ad group and campaign settings.
>* Changing a [!DNL Microsoft Advertising] keyword deletes the existing keyword and creates a new one with a new keyword ID. Changing the match type, however, doesn't delete the existing keyword.

**[!UICONTROL Status]:** The display status of the keyword: *[!UICONTROL Active]* or *[!UICONTROL Paused]*. The default for new keywords is *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains [the `{Param1}` dynamic substitution string](https://help.bingads.microsoft.com/#apex/3/en/53079/0). The maximum length is 70 characters, but be aware of the maximum length of the ad elements in which you use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters).

**[!UICONTROL Param2]:** The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains [the `{Param2}` dynamic substitution string](https://help.bingads.microsoft.com/#apex/3/en/53079/0). The maximum length is 70 characters, but be aware of the maximum length of the ad elements in which you use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters).

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

This field can optionally include the `{Param1}` and `{Param2}` dynamic substitution variables.

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Manage keywords](keyword-manage.md)
