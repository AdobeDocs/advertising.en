---
title: "[!DNL Baidu] campaign settings"
description: Reference the settings for [!DNL Baidu] campaigns.
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
---
# [!DNL Baidu] campaign settings

## \[Top of page]

**[!UICONTROL Campaign Name]:** A campaign name that's unique within the account.

**[!UICONTROL Status]:** The display status of the campaign: *Active* or *Paused*. The default for new ad campaigns is *Active*.

## [!UICONTROL Basic Settings] tab

*New campaigns only*

**[!UICONTROL Network]:** The ad network.

**[!UICONTROL Account]:** The ad network account.

**[!UICONTROL Campaign Type]:** Where to place ads, and which ad types the campaign may contain. The only option is *Search Network Only*.

## [!UICONTROL Campaign Details] tab

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Applicable to campaigns that target audiences in the European Union (EU)) Whether or not the campaign contains political advertising per requirements for ads served in the European Union under EU Regulation 2024/90: *[!UICONTROL Yes]* or *[!UICONTROL No]*.

## [!UICONTROL Budget Options] tab

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** The bid strategy for the campaign:

* *[!UICONTROL Maximize Conversions]:* The ad network &mdash; not Search, Social, & Commerce &mdash; optimizes bids to maximize conversions. Optionally enter a **[!UICONTROL Target CPA]** (cost per acquisition). **Note:** Use this option for campaigns in portfolios with campaign-level optimization. In portfolios with campaign-level optimization, Search, Social, & Commerce optimizes the Target CPA.

* *[!UICONTROL Maximize Conversion Value]:* The ad network &mdash; not Search, Social, & Commerce  &mdash; optimizes bids to maximize conversion value. Optionally enter a **[!UICONTROL Target Return on Ad Spend]** (ROAS) as a percent. **Note:** Use this option for campaigns in portfolios with campaign-level optimization. In portfolios with campaign-level optimization, Search, Social, & Commerce optimizes the Target ROAS.

## [!UICONTROL Campaign Targeting] tab

**[!UICONTROL Languages]:** The language of the ad, which should match the language of the sites on which your ad can appear. The ad network determines a user's language from various signals, including the user's query, the publisher's country, and the user's language setting.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL Additional Campaign Information] tab

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### [!UICONTROL Campaign Tracking] tab

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
