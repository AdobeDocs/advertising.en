---
title: '[!DNL Google Ads] keyword settings'
description: Reference the settings for [!DNL Google Ads] keywords.
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# [!DNL Google Ads] keyword settings

You can create keywords for campaigns that use the search and display networks.

See the [!DNL Google Ads] help for [keyword limits per account](https://support.google.com/google-ads/answer/6372658).

## [!UICONTROL Basic Settings]

*New keywords only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign]:** The campaign.

**[!UICONTROL Ad Group]:** The ad group.

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords, including any [!DNL Google Ads] match syntax for keywords and placeholders. [!DNL Google Ads] accounts require keywords with the following attributes:

* The maximum length per keyword is 80 characters and no more than 10 words.

* The keyword can include only letters, digits, and the following special characters: space `# $ & _ - " [] ' + . / :`

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* You can create negative keywords from the [!UICONTROL Manage] > [!UICONTROL Keywords] > [!UICONTROL Negatives] tab and in the ad group and campaign settings.
>* Changing a [!DNL Google Ads] keyword or match type deletes the existing keyword and creates a new one.

**[!UICONTROL Status]:** The display status of the keyword: *[!UICONTROL Active]* or *[!UICONTROL Paused]*. The default for new keywords is *[!UICONTROL Active]*.

## [!UICONTROL Bids]

{{$include /help/_includes/bid-keyword.md}}

## [!UICONTROL Placeholders]

**[!UICONTROL Param1]:** The string to use as the substitution value if the base URL or tracking template contains [the `{param1}`](https://support.google.com/google-ads/answer/6305348) dynamic substitution string.

**[!UICONTROL Param2]:** The string to use as the substitution value if the base URL or tracking template contains [the `{param2}`](https://support.google.com/google-ads/answer/6305348) dynamic substitution string.

## [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Manage keywords](keyword-manage.md)
