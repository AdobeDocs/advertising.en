---
title: '[!DNL Google Ads] keyword settings'
description: Reference the settings for [!DNL Google Ads] keywords.
exl-id: 8834e852-214b-4b2c-9a95-4b1c802e800d
feature: Search Campaign Management
---
# [!DNL Google Ads] keyword settings

You can create keywords for campaigns that use the search and display networks.

See the Google Ads help for [keyword limits per account](https://support.google.com/google-ads/answer/6372658). 

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keywords, including any [!DNL Google Ads] match syntax for keywords and placeholders. [!DNL Google Ads] accounts require keywords with the following attributes:

* The maximum length per keyword is 80 characters and no more than 10 words.
* The keyword can include only letters, digits, and the following special characters: space `# $ & _ - " [] ' + . / :`

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* You can create negative keywords from the [!UICONTROL Keywords] > [!UICONTROL Negatives] view and in the ad group and campaign settings.
>* Changing a [!DNL Google Ads] keyword or match type deletes the existing keyword and creates a new one.

**[!UICONTROL Status]:** The display status of the keyword: *Active* or *Paused*. The default for new keywords is *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Placeholders

**[!UICONTROL Param1]:** The string to use as the substitution value if the base URL or tracking template contains [the `{param1}`](https://support.google.com/google-ads/answer/6305348) dynamic substitution string.

**[!UICONTROL Param2]:** The string to use as the substitution value if the base URL or tracking template contains [the `{param2}`](https://support.google.com/google-ads/answer/6305348) dynamic substitution string.

## URL Options

<!-- **[!UICONTROL Base URl]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- **[note for Base URL field]:** -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Manage keywords](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
