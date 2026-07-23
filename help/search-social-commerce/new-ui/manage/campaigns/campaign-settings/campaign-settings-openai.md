---
title: "[!DNL OpenAI Ads] campaign settings"
description: Reference the settings for [!DNL OpenAI Ads] campaigns.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
---
# [!DNL OpenAI Ads] campaign settings

<!-- EDIT ALL AS NEEDED -->

## \[Top of page]

**[!UICONTROL Campaign Name]:** A campaign name that's unique within the account.

**[!UICONTROL Status]:** The display status of the campaign: *Active* or *Paused*. The default for new ad campaigns is *Active*.

## [!UICONTROL Basic Settings] tab

*New campaigns only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign Type]:** Where to place ads: the only option is *[!UICONTROL Search Network Only]* to display text ads on the search network.

## [!UICONTROL Campaign Details] tab

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

**[!UICONTROL Budget]:** The budget, which is the amount you want to spend daily, on average. The minimum daily budget is 100 JPY.

If you assign this campaign to a portfolio for which campaign budget limits are automatically adjusted, then &mdash; depending on search conditions &mdash; you may actually spend more or less than the specified budget in any given period.

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-yahoo-japan.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-yahoo-japan.md}}

## [!UICONTROL Campaign Tracking] tab

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (For [!UICONTROL EF Redirect] only) The level at which clicks and revenue should be tracked by adding a redirect (when relevant) and append parameters to the relevant URLs:

* *[!UICONTROL Keyword]:* To track data at only the keyword level.

* *[!UICONTROL Creative]:* To track data at only the ad (creative) level.

* *[!UICONTROL Creative and Keyword]:* To track data at both the ad (creative) and keyword levels.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Adds a URL parameter to ads in the account or campaign for conversion tracking.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Manage campaigns](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
