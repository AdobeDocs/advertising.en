---
title: '[!DNL Microsoft Advertising] keyword settings'
description: Reference the settings for [!DNL Microsoft Advertising] keywords.
exl-id: 82eee01f-db4b-4d1a-ae24-1ef65f8c6953
feature: Search Campaign Management
---
# [!DNL Microsoft Advertising] keyword settings

You can create keywords for campaigns that use the search and display networks.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords, including any [!DNL Microsoft Advertising] match syntax and placeholders. The maximum length per keyword is 100 characters.

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* You can create negative keywords from the [!UICONTROL Keywords] > [!UICONTROL Negatives] view and in the ad group and campaign settings.
>* Changing a [!DNL Microsoft Advertising] keyword deletes the existing keyword and creates a new one with a new keyword ID. Changing the match type, however, doesn't delete the existing keyword.

**[!UICONTROL Status]:** The display status of the keyword: *Active* or *Paused*. The default for new keywords is *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Placeholders

**[!UICONTROL Param2]:** The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains [the `{Param2}` dynamic substitution string](https://help.bingads.microsoft.com/#apex/3/en/53079/0). The maximum length is 70 characters, but be aware of the maximum length of the ad elements in which you use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters).

**[!UICONTROL Param3]:** The string to use as the substitution value if the keyword's base URL or the ad's title, description, or base URL contains [the `{Param3}` dynamic substitution string](https://help.bingads.microsoft.com/#apex/3/en/53079/0). The maximum length is 70 characters, but be aware of the maximum length of the ad elements in which you use it (for example, Title 1 and Title 2 combined may be a maximum of 76 characters).

## URL Options

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

This field can optionally include the `{Param2}` and `{Param3}` dynamic substitution variables.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

>[!MORELIKETHIS]
>
>* [Manage keywords](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
