---
title: "[!DNL Yandex] keyword settings"
description: Reference the settings for [!DNL Yandex] keywords.
---
# [!DNL Yandex] keyword settings

Yandex keywords are used for both search and display (content) networks.

<!-- Note to self: Yandex doesn't have separate website placements for display; users use keywords for the sites/parts of the content network on which they want to advertise. -->

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** The keyword phrases, including any [Yandex match type syntax](https://yandex.com/support/direct/keywords/symbols-and-operators.html) for keywords. Each keyword can have a maximum of seven words, excluding stop words.

You can enter or paste up to 2000 keywords. Separate multiple keywords with commas, or enter them on separate lines.

>[!NOTE]
>
>* Changing a [!DNL Yandex] keyword or match type deletes the existing keyword and creates a new one.
>* Each Yandex ad group can include a maximum of 200 keywords.

**[!UICONTROL Status]:** The display status of the keyword: *Active* or *Paused*. The default for new keywords is *Active*.

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## Placeholders

**[!UICONTROL Param1]** **[!UICONTROL Param2]:** The value of the `{param1}` and `{param2}` substitution variables, which are substituted for any instances of {param1} and {param2} in the base URL for ads and sitelinks when the keyword is used to display the ad. The maximum length is 255 bytes.

Special characters are automatically encoded in UTF-8. For example, if the associated ad has a base URL of "http://www.example.com/{param1} and the keyword-level value of {param1} is "shoes/flats.html," then the ad leads to http://www.example.com/shoes%2Fflats.html.

>[!MORELIKETHIS]
>
>* [Manage keywords](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
