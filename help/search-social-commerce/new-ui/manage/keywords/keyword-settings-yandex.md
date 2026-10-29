---
title: '[!DNL Yandex] keyword settings'
description: Reference the settings for [!DNL Yandex] keywords.
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
# [!DNL Yandex] keyword settings

[!DNL Yandex] keywords are used for both search and display (content) networks.

## [!UICONTROL Basic Settings]

*New keywords only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keyword phrases, including any [[!DNL Yandex] match type syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) for keywords. Each keyword can have a maximum of seven words, excluding stop words.

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* Changing a [!DNL Yandex] keyword or match type deletes the existing keyword and creates a new one.
>* Each [!DNL Yandex] ad group can include a maximum of 200 keywords.

**[!UICONTROL Status]:** The display status of the keyword: *[!UICONTROL Active]* or *[!UICONTROL Paused]*. The default for new keywords is *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

>[!NOTE]
>
>Special characters are automatically encoded in UTF-8. For example, if the associated ad has a base URL of `http://www.example.com/{param1}` and the keyword-level value of `{param1}` is `shoes/flats.html`, then the ad leads to `http://www.example.com/shoes%2Fflats.html`.

**[!UICONTROL Param1]:** The string to use as the substitution value if the base URL contains the `{param1}` dynamic substitution string for ads and sitelinks when the keyword is used to display the ad. The maximum length is 255 bytes.

**[!UICONTROL Param2]:** The string to use as the substitution value if the base URL contains the `{param2}` dynamic substitution string for ads and sitelinks when the keyword is used to display the ad. The maximum length is 255 bytes.

>[!MORELIKETHIS]
>
>* [Manage keywords](keyword-manage.md)
