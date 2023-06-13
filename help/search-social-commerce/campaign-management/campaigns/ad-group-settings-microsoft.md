---
title: '[!DNL Microsoft Advertising] ad group settings'
description: Reference the settings for [!DNL Microsoft Advertising] ad groups.
exl-id: 5dfa766d-2a42-455d-a340-e72e11a38032
---
# [!DNL Microsoft Advertising] ad group settings

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** An ad group name that is unique within the campaign. The maximum length is 128 characters.

**[!UICONTROL Status]:** The display status of the ad group: *Active* or *Paused*. The default for new ad groups is *Active*.

**[!UICONTROL Ad Language]:** The target language for ads.<!-- Which campaign types? Not there for audience image-based ad groups. -->

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** How and where to place ads within the ad group:

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* (the default): To place bids for ads on the search network.

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* To place bids for ads on syndicated partner sites.

* *[!UICONTROL Content network]:* Deprecated

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** Deprecated

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Audience ad groups) Whether to:

* *[!UICONTROL Target and Bid]:* To show ads only to users associated with target audiences who also satisfy any other targets for the ad group.

* *[!UICONTROL Bid Only]:* To show ads even to people who aren't associated with target audiences as long as they satisfy other ad group-level targets. You can increase the chances that ads are shown to specific audiences, however, by setting higher bids for those audiences.

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

For [!DNL Microsoft Advertising] ad groups in the audience network, bid modifiers for location targets aren't optimized in standard portfolios with the "[!UICONTROL Auto-optimize Bid Adjustment Values]" setting.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** (Audience ad groups; optional) Specific genders to include or exclude as targets: *[!UICONTROL Male]*, *[!UICONTROL Female]*, and *[!UICONTROL Unknown]*. By default, all genders are targeted. Exclusions always override inclusions.

* To target all values, don't select any values.

* To include a value, click the circle next to it once so that a blue checkmark (![Include](/help/search-social-commerce/assets/include.png "Include")) appears. You can optionally increase or decrease bids by a specified percentage for each gender targeted.

* To exclude a value, click the circle next to it twice so that a red checkmark (![Exclude](/help/search-social-commerce/assets/exclude.png "Exclude")) appears.

**[!UICONTROL Age]:** (Audience ad groups; optional) Specific age categories to include or exclude as targets: *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*, and *[!UICONTROL Unknown]*. By default, all ages are targeted. Exclusions always override inclusions.

* To target all values, don't select any values.

* To include a value, click the circle next to it once so that a blue checkmark (![Include](/help/search-social-commerce/assets/include.png "Include")) appears. You can optionally increase or decrease bids by a specified percentage for each age targeted.

* To exclude a value, click the circle next to it twice so that a red checkmark (![Exclude](/help/search-social-commerce/assets/exclude.png "Exclude")) appears.

**[!UICONTROL Industry]:** (Audience ad groups; optional) Specific industries to include or exclude as targets. By default, all industries are targeted. Exclusions always override inclusions.

* To target all values, don't select any values.

* To include a value, click the circle next to it once so that a blue checkmark (![Include](/help/search-social-commerce/assets/include.png "Include")) appears. You can optionally increase or decrease bids by a specified percentage for each industry targeted.

* To exclude a value, click the circle next to it twice so that a red checkmark (![Exclude](/help/search-social-commerce/assets/exclude.png "Exclude")) appears.

**[!UICONTROL Job Function Targets]:** (Audience ad groups; optional) Specific job functions to include or exclude as targets. By default, all job functions are targeted. Exclusions always override inclusions.

* To target all values, don't select any values.

* To include a value, click the circle next to it once so that a blue checkmark (![Include](/help/search-social-commerce/assets/include.png "Include")) appears. You can optionally increase or decrease bids by a specified percentage for each job functions targeted.

* To exclude a value, click the circle next to it twice so that a red checkmark (![Exclude](/help/search-social-commerce/assets/exclude.png "Exclude")) appears.

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Campaigns on the display/native network only; optional) Sites on the display network on which you don't want your ads to be displayed. Enter a valid URL, such as www.example.com. To specify multiple strings, separate them with commas or enter them on separate lines.

For information about availability, see Microsoft Advertising help on "[Prevent ads from appearing on specific websites](https://help.ads.microsoft.com/#apex/bae/en/14061/0)."

>[!MORELIKETHIS]
>
>* [Manage ad groups](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
